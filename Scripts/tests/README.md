# 测试脚本说明

本目录包含用于执行项目测试的脚本。

## 可用脚本

### 1. `run_all_tests.py` - 完整测试执行器

**功能：**
- 运行所有测试文件
- 提供详细的测试报告
- 支持单个测试文件执行
- 包含超时保护

**使用方法：**
```bash
# 运行所有测试
python Scripts/tests/run_all_tests.py

# 运行指定测试文件
python Scripts/tests/run_all_tests.py tests/core/strategy/test_rule_parser.py
```

### 2. `quick_test.py` - 快速测试脚本

**功能：**
- 快速运行所有测试
- 简洁的输出格式
- 适合日常开发使用

**使用方法：**
```bash
# 快速运行所有测试
python Scripts/tests/quick_test.py

# 运行指定测试文件
python Scripts/tests/quick_test.py tests/core/strategy/test_rule_parser.py
```

## 测试文件列表

当前包含的测试文件：

1. **`tests/core/strategy/test_rule_parser.py`**
   - 测试规则解析器功能
   - 包括边界条件、性能测试等

2. **`tests/archive/test_martingale.py`**
   - 测试Martingale策略规则

3. **`tests/archive/test_simple.py`**
   - 测试简单表达式生成

4. **`tests/core/data/test_market_data_source.py`**
   - 测试市场数据源功能

## 依赖要求

确保已安装以下依赖：
```bash
pip install pytest pandas numpy
```

## 测试结果说明

- ✅ 通过：测试成功
- ❌ 失败：测试失败
- ⏰ 超时：测试执行超时
- 💥 错误：测试执行过程中出现错误
- ⏭️ 跳过：测试文件不存在

## 注意事项

1. 确保数据库连接配置正确
2. 测试可能需要访问外部数据源
3. 部分测试可能耗时较长，已设置超时保护
4. 如果测试失败，请查看详细错误信息进行调试