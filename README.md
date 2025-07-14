# LLM_Gen_TestCase_v2

## 项目简介

LLM_Gen_TestCase是一个基于大语言模型（LLM）的自动化测试用例生成工具。该项目通过解析需求文档，结合大语言模型能力，自动生成高质量的测试用例，提升测试效率，降低人工成本。

## 主要功能
- 需求文档解析：支持多种格式（如 txt、docx、pdf）需求文档的解析。
- 测试用例自动生成：调用大语言模型，根据需求文档内容自动生成测试用例。
- 测试用例导出：支持将生成的测试用例导出为 Excel 等常用格式。

## 目录结构
```
├── config.ini                  # 配置文件
├── document_integration.py     # 文档整合与处理模块
├── document_parser.py          # 文档解析模块
├── llms.py                     # 大语言模型接口模块
├── page.py                     # 页面相关处理模块
├── processed_需求文档示例.txt   # 处理后的需求文档示例
├── requirements.txt            # Python 依赖包列表
├── run.py                      # 主程序入口
├── run.spec                    # PyInstaller 打包配置
├── TESTCASE_READER_SYSTEM_MESSAGE.txt  # 测试用例读取系统消息模板
├── TESTCASE_WRITER_SYSTEM_MESSAGE.txt  # 测试用例生成系统消息模板
├── testfile/                   # 测试文件夹，存放需求文档及生成的测试用例
│   ├── 书店系统测试用例.xlsx
│   ├── 书店系统产品需求文档.docx
│   ├── 书店系统产品需求文档.pdf
│   ├── 书店系统产品需求文档.txt
│   └── parsetest1.docx
└── __pycache__/                # Python 编译缓存
```

## 安装依赖

建议使用 Python 3.8 及以上版本。

```bash
pip install -r requirements.txt
```

## 使用方法

1. 准备需求文档，放入 `testfile/` 目录。
2. 配置 `config.ini`（如需修改默认参数）。
3. 运行主程序：

```bash
python run.py
```

4. 生成的测试用例将输出到 `testfile/` 目录下。

## 依赖说明

- openai
- python-docx
- PyPDF2
- pandas
- 其他依赖详见 `requirements.txt`

## 贡献

欢迎提交 issue 和 pull request 以改进本项目。

## 许可证

本项目采用 MIT License。
