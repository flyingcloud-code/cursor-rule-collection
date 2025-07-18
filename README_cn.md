# RIPER 规则

## 概述
RIPER 通过五种不同的操作模式提供了一种系统化的软件开发方法：

- **研究 (R)**：收集信息并理解现有代码
- **创新 (I)**：头脑风暴，探索潜在方法和解决方案
- **计划 (P)**：制定详细的技术规格
- **执行 (E)**：精确实施批准的计划
- **审查 (R)**：验证实施结果是否符合计划

## 关键优势
- 仅需单一规则
- 无需内存库
- 无需复杂的项目规则
- 适用于 cursor、windsurf、augment、trae、GitHub Copilot 等工具

### 来源
源自 cursor 论坛文章：[我创建了一个名为"RIPER-5 模式"的惊艳模式，大幅修复了 Claude 3.7！](https://forum.cursor.com/t/i-created-an-amazing-mode-called-riper-5-mode-fixes-claude-3-7-drastically/65516)

## RIPER-5 01 版本
可查看 **[RIPER-5 01 规则](RIPER/RIPER-5-01-version.md)**

## RIPER-5 高级版本
### [RIPER-5_多维思考_代理执行协议](RIPER/RIPER-5_MULTIDIMENSIONAL_THINKING-AGENT_EXECUTION_PROTOCOL.md)  
源自 cursor 论坛中的修订版链接：[修订版本](https://forum.cursor.com/t/i-created-an-amazing-mode-called-riper-5-mode-fixes-claude-3-7-drastically/65516/97)

### 新协议关键特性

新协议（RIPER-5 + 多维思考 + 代理执行协议）相较旧协议（RIPER-5：严格操作协议）引入了显著改进。

**自动模式转换**：无需显式"ENTER [MODE]"指令，AI 可在 RESEARCH、INNOVATE、PLAN、EXECUTE 和 REVIEW 模式间无缝切换。根据用户请求语义智能选择起始模式，默认 RESEARCH，提升效率。

**多维思考**：融入系统思考、辩证思考、创新思考和批判性思考原则，贯穿所有模式，确保分析全面、解决方案优化且具创造性。

**任务文件模板**：引入标准化模板，记录任务详情、分析、解决方案、计划、进度和审查。AI 动态更新，确保全流程可追溯。

**代码处理规范**：定义统一的代码块结构，包含文件路径、语言标识和上下文注释。禁止未验证依赖或无关修改，提升代码质量。

**执行模式改进**：允许处理"微小偏差"（如拼写错误修复），需提前报告。每步后更新进度，记录变更、原因和用户确认状态，并请求反馈。若反馈显示问题，自动返回 PLAN 模式。

**语言与性能**：模式声明和代码使用英语，其余交互默认中文（可配置）。目标响应延迟≤30秒，复杂任务提供中间状态更新。

### 与旧协议的改进对比

旧协议的僵硬手动模式切换增加用户负担，缺乏思考原则导致机械输出，无统一任务文档，代码规范松散，执行模式要求完全遵循计划，缺乏灵活性。新协议通过自动模式转换提升灵活性，多维思考改进分析，任务模板确保可追溯性。严格的代码规范和容错执行（带用户反馈）减少错误。响应时间目标和中间更新优化性能，使新协议更适合复杂软件开发，兼顾严格性和用户友好性。

### [RIPER-5_TDD-AGILE-SOLID-KISS_EXECUTION_PROTOCOL](RIPER/RIPER-5_TDD-KISS-SOLID_EXECUTION_PROPOCOL.md)

### RIPER-5 与 TDD-Agile + SOLID/KISS 协议关键特性

该协议在多维思考协议的基础上，引入了更严格和全面的开发实践：

**核心开发原则**:
- **测试驱动开发 (TDD)**: 强制 Red-Green-Refactor 循环，强调先写测试，使用真实接口，并明确错误报告。
- **敏捷方法论**: 强调增量开发、迭代和小步快跑。
- **SOLID 原则**: 在所有设计和实现中严格遵循单一职责、开闭原则、里氏替换、接口隔离和依赖倒置。
- **KISS (Keep It Simple, Stupid)**: 始终优先选择最简单的解决方案。
- **YAGNI (You Aren't Gonna Need It)**: 平衡产品质量与过度设计/测试。

**强制文档流程**:
- 引入 `001-dev-doc` 目录，包含 `00-index.md` (索引), `01-prd.md` (产品需求), `02-design.md` (设计文档), `03-dev_progress.md` (开发进度) 等结构化文档，确保全流程可追溯和规范化。

**精细化模式切换与控制**:
- RESEARCH 和 INNOVATE 模式可自动启动和切换。
- **创新 (INNOVATE) 模式完成后，必须等待用户审查和批准才能进入计划 (PLAN) 模式**，确保关键决策得到用户认可。
- 一旦进入计划 (PLAN) 模式，将自动执行所有后续步骤，无需额外指令。
- **禁止未经用户批准直接跳过计划 (PLAN) 模式进入执行 (EXECUTE) 模式**。

**增强的核心思考原则**:
- 在多维思考的基础上，额外强调 **测试驱动思考**、**聚焦简洁设计** 和 **SOLID 架构规划**。

**模式职责深度细化**:
- **研究 (RESEARCH) 模式**: 扩展至负责创建/更新项目文档，并主动识别、评估和记录测试需求及测试覆盖率。
- **创新 (INNOVATE) 模式**: 在提出解决方案时，必须基于 SOLID 和 KISS 原则进行架构设计，并详细评估方案的可测试性。
- **计划 (PLAN) 模式**: **强制在代码实现前，详细制定测试用例 (TDD)**，包括单元测试、集成测试和功能测试，并明确断言、预期结果、真实接口使用和错误处理方式。将整个计划转换为详细的、原子级的编号执行清单。
- **执行 (EXECUTE) 模式**: **严格遵循 TDD 的 Red-Green-Refactor 循环**。允许报告并执行"微小偏差"，每一步骤完成后强制更新详细的开发进度，并请求用户确认。若用户反馈问题，将自动返回计划 (PLAN) 模式。
- **审查 (REVIEW) 模式**: 强制进行**严格的功能验证矩阵**比对，**全面评估测试质量**（包括验证所有测试是否使用真实接口以及错误处理的明确性），并深度评估最终实现对 SOLID 和 KISS 原则的遵循情况。

**更严格的代码处理规范**:
- 统一的代码块结构，明确要求包含文件路径和语言标识符。
- 详细的编辑指导，禁止使用未经验证的依赖、不完整的代码、未经测试的代码，以及修改不相关的代码。

## RIPER 协议版本比较与推荐

### 表格 1：协议核心概览

| 协议版本                      | 核心理念                                                                                              | 模式切换                                           | 思考原则                                                               | 文档管理                                            |
| :---------------------------- | :---------------------------------------------------------------------------------------------------- | :------------------------------------------------- | :----------------------------------------------------- | :-------------------------------------------------- |
| RIPER-5 01 版本               | RIPER 五个模式的初步概念。                                                                            | 手动且严格，需要明确指令。                         | 基础的流程导向。                                       | 无明确强制性文档要求。                              |
| RIPER-5 多维思考 + 代理执行协议 | 在 RIPER 基础上引入多维思考（系统、辩证、创新、批判）和代理执行。                                       | 自动模式转换，AI 智能选择起始模式。                | 强调系统思考、辩证思考、创新思考、批判性思考。         | 引入任务文件模板，确保可追溯性。                    |
| RIPER-5 TDD-Agile + SOLID/KISS 协议 | 深度集成 TDD、敏捷、SOLID 和 KISS 原则，注重质量、简洁和可维护性。                                      | RESEARCH 和 INNOVATE 自动切换，INNOVATE 后强制用户批准才能进入 PLAN，PLAN 后自动执行所有后续模式，禁止跳过 PLAN 直接执行。 | 额外强调测试驱动思考、聚焦简洁设计和 SOLID 架构规划。  | 强制所有结构化文档（001-dev-doc 目录），并明确各模式下的文档更新职责。 |

### 表格 2：协议效果与应用

| 协议版本                      | 测试集成                                             | 代码规范                                                 | 优点                                                                                                                  | 缺点                                                                                                                      | 推荐场景                                                                                        |
| :---------------------------- | :--------------------------------------------------- | :------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------ |
| RIPER-5 01 版本               | 无明确测试要求。                                     | 无明确代码处理规范。                                     | 简单易懂，入门快，适用于非常简单或个人项目。                                                                            | 过于简化，缺乏灵活性、智能性和质量保障，易出错，不适合复杂项目。                                                          | 学习 RIPER 流程的初学者；极小型、非关键性项目。         |
| RIPER-5 多维思考 + 代理执行协议 | 无明确强制性 TDD 或测试用例编写要求，但执行模式会更新进度并请求反馈。 | 定义统一代码块结构，禁止未验证依赖或无关修改。           | 提升效率，分析更全面，解决方案更优化和具创造性，增强了可追溯性和代码质量。                                                | 缺乏 TDD 的严格质量保障，测试要求不如最新版明确。                                                                         | 需要 AI 智能辅助、项目复杂度适中，对规范性有一定要求，但对 TDD 严格性要求不高的团队。 |
| RIPER-5 TDD-Agile + SOLID/KISS 协议 | 强制 TDD Red-Green-Refactor 循环，先写测试（要求真实接口），PLAN 模式下强制详细制定测试用例，EXECUTE 模式严格执行 TDD 流程，REVIEW 模式强制进行功能验证矩阵和测试质量评估。 | 更严格的统一代码块结构、详细编辑指南和禁止行为。           | 极大地提升了软件质量、可维护性和稳定性；流程严谨，可追溯性极强；确保了最佳实践的应用。                                    | 学习曲线较陡峭，流程较为复杂和严格，可能在小型或快速原型项目中引入额外开销。                                                | 高质量要求、复杂、长期维护的项目；团队具备 TDD 和 SOLID 经验；需要严格规范和可追溯性的企业级开发。 |