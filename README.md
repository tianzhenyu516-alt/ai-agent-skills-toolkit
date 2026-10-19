# AI Agent Skills Toolkit

面向 AI 助手的 17 个可单独安装的技能，覆盖嵌入式开发、代码审查、数据分析与任务流程。每个技能都有独立目录、`SKILL.md`、说明和许可证；按需取用即可。

Search keywords: AI agent skills, embedded systems, STM32, ESP32, MSPM0, K230, OpenMV, Python data science, code review.

## 按领域浏览 / Browse by topic

### 嵌入式与硬件视觉 / Embedded systems and hardware vision

| Skill | Use it for |
| --- | --- |
| [Embedded systems](embedded/embedded-systems/) | General STM32, ESP32, and RTOS engineering workflow |
| [Arduino firmware](embedded/arduino-firmware/) | Arduino board-aware firmware development |
| [CCS MSPM0](embedded/ccs-mspm0/) | Code Composer Studio and MSPM0 projects |
| [ESP32-S3 ESP-IDF](embedded/esp32-s3-esp-idf/) | ESP32-S3 firmware with ESP-IDF |
| [Hi3861 OpenHarmony](embedded/hi3861-openharmony/) | Hi3861 and OpenHarmony development |
| [IAR Embedded](embedded/iar-embedded/) | IAR Embedded Workbench projects |
| [K230 vision](embedded/k230-vision/) | K230 camera, model deployment, and edge vision |
| [Keil µVision 5 STM32](embedded/keil-uv5-stm32/) | Keil and STM32 firmware projects |
| [OpenMV vision](embedded/openmv-vision/) | OpenMV camera and machine vision |
| [PlatformIO ESP-IDF](embedded/platformio-esp-idf/) | PlatformIO and ESP-IDF integration |
| [RT-Thread](embedded/rt-thread/) | RT-Thread RTOS firmware |

### 代码质量 / Code quality

| Skill | Use it for |
| --- | --- |
| [Code review](code-quality/code-review/) | Evidence-based review of code changes |
| [Request code review](code-quality/request-code-review/) | Preparing a clear review request |
| [Review feedback](code-quality/review-feedback/) | Verifying and addressing reviewer feedback |

### 数据分析 / Data science

| Skill | Use it for |
| --- | --- |
| [Jupyter Notebook](data-science/jupyter-notebook/) | Reproducible notebook work |
| [Python data science](data-science/python-data-science/) | Python data cleaning, analysis, and validation |

### 工作流 / Workflow

| Skill | Use it for |
| --- | --- |
| [Autopilot workflow](workflow/autopilot-workflow/) | Carrying a scoped software task through implementation and verification |

## 安装单个技能 / Install one skill

打开对应目录，先看该技能的 README 和 `SKILL.md`，再把**整个技能目录**复制到 AI 助手的技能目录。若目录中有 `references/`，请一并保留。技能是操作说明，不会自动安装硬件 SDK 或提供外部服务。

使用硬件类技能时，请先说明**芯片完整型号、开发板/模组型号与版本**，并提供数据手册、原理图或引脚表的链接或本地路径，再要求具体引脚分配。

## 在 GitHub 查找 / Find a skill

上面的链接是“领域 → 技能”的两级目录。GitHub Code Search 能搜索文件名、内容和路径。例如，输入 `repo:tianzhenyu516-alt/ai-agent-skills-toolkit path:embedded/k230-vision` 可以定位 K230 技能；也可以在本仓库搜索 `OpenMV`。刚发布的文件可能需要等待搜索索引更新。

K230 和 OpenMV 技能针对的是**硬件视觉**。

## 来源与许可 / Provenance and licenses

这 17 个技能从原先公开的独立仓库汇总而来。每个目录保留自己的 README 和 `LICENSE`；具体许可范围、参考来源以该目录文件为准。第三方产品名称仅用于说明兼容的工具或硬件。本库不包含 API 密钥和个人配置文件。
