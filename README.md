# RIPER rules
## Overview
RIPER provides a systematic approach to software development through five distinct operational modes:

Research(R): Information gathering and understanding existing code
Innovate(I): Brainstorming potential approaches and solutions
Plan(P): Creating detailed technical specifications
Execute(E): Implementing approved plans with precision
Review(R): Validating implementation against plans

## key advantage
- single rule consumed
- no memory bank required.
- no complex project rules required
- can be used for cursor, windsurf, augment, trae, github copilot, etc.

### Source
started from cursor forum article [I created an AMAZING MODE called "RIPER-5 Mode" Fixes Claude 3.7 Drastically!](https://forum.cursor.com/t/i-created-an-amazing-mode-called-riper-5-mode-fixes-claude-3-7-drastically/65516)

## RIPER-5 01 version
You can check **[RIPER-5 01 rule](RIPER/RIPER-5-01-version.md)**

## RIPER-5 advanced version
### [RIPER-5_MULTIDIMENSIONAL_THINKING-AGENT_EXECUTION_PROTOCOL](RIPER/RIPER-5_MULTIDIMENSIONAL_THINKING-AGENT_EXECUTION_PROTOCOL.md) started from the original link in cursor forum [revised version](https://forum.cursor.com/t/i-created-an-amazing-mode-called-riper-5-mode-fixes-claude-3-7-drastically/65516/97)

### New Protocol Key Features

The new protocol (RIPER-5 + Multidimensional Thinking + Agent Execution Protocol) introduces significant enhancements over the old protocol (RIPER-5: Strict Operational Protocol).

**Automatic Mode Switching**: Eliminates explicit "ENTER [MODE]" commands, enabling seamless transitions between RESEARCH, INNOVATE, PLAN, EXECUTE, and REVIEW modes. AI intelligently selects the starting mode based on user request semantics, defaulting to RESEARCH, improving efficiency.

**Multidimensional Thinking**: Integrates systems, dialectical, innovative, and critical thinking principles across all modes, ensuring comprehensive analysis and optimized, creative solutions.

**Task File Template**: Introduces a standardized template to record task details, analysis, solutions, plans, progress, and reviews. AI dynamically updates it, ensuring full traceability.

**Code Handling Standards**: Defines unified code block structures with file paths, language identifiers, and contextual comments. Prohibits unverified dependencies or unrelated changes, enhancing code quality.

**Execution Mode Improvements**: Allows handling minor deviations (e.g., typo fixes) with prior reporting. After each step, AI updates progress, logs changes, and requests user feedback. If feedback indicates issues, it reverts to PLAN mode.

**Language and Performance**: Uses English for mode declarations and code, with Chinese for other interactions (user-configurable). Targets ≤30-second response latency, with interim updates for complex tasks.

### Improvements Over Old Protocol

The old protocol's rigid, manual mode switching increased user effort, while its lack of thinking principles led to mechanical outputs. It had no unified task documentation, loose code standards, and inflexible execution requiring 100% plan adherence. The new protocol enhances flexibility with automatic mode switching, improves analysis with multidimensional thinking, and ensures traceability via task templates. Strict code standards and fault-tolerant execution with user feedback reduce errors. Response time targets and interim updates optimize performance, making the new protocol ideal for complex software development, balancing strictness with user-friendly intelligence.

### [RIPER-5_TDD-AGILE-SOLID-KISS_EXECUTION_PROTOCOL](RIPER/RIPER-5_TDD-KISS-SOLID_EXECUTION_PROPOCOL.md)

### RIPER-5 with TDD-Agile + SOLID/KISS Protocol Key Features

This protocol, building upon the Multidimensional Thinking Protocol, introduces stricter and more comprehensive development practices:

**Core Development Principles**:
- **Test-Driven Development (TDD)**: Enforces the Red-Green-Refactor cycle, prioritizing writing tests first, using real interfaces, and clear error reporting.
- **Agile Methodology**: Emphasizes incremental development, iterative changes, and continuous feedback.
- **SOLID Principles**: Strictly adheres to Single Responsibility, Open-Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion in all designs and implementations.
- **KISS (Keep It Simple, Stupid)**: Always prioritizes the simplest solution.
- **YAGNI (You Aren't Gonna Need It)**: Balances product quality with avoiding over-design and over-testing.

**Mandatory Documentation Workflow**:
- Introduces the `001-dev-doc` directory containing structured documentation: `00-index.md` (index), `01-prd.md` (product requirements), `02-design.md` (design document), `03-dev_progress.md` (development progress), ensuring full traceability and standardization throughout the process.

**Refined Mode Switching and Control**:
- RESEARCH and INNOVATE modes can start and transition automatically.
- **Upon completion of the INNOVATE mode, user review and approval are mandatory before proceeding to the PLAN mode**, ensuring critical decisions are validated by the user.
- Once the PLAN mode is entered, all subsequent steps execute automatically without further explicit commands.
- **Directly skipping the PLAN mode and entering the EXECUTE mode without user approval is prohibited**.

**Enhanced Core Thinking Principles**:
- Beyond multidimensional thinking, explicitly emphasizes **Test-Driven Thinking**, **Simplicity-Focused Design**, and **SOLID Architectural Planning**.

**Deeply Detailed Mode Responsibilities**:
- **RESEARCH Mode**: Expanded to include creating/updating project documentation and proactively identifying, evaluating, and documenting testing requirements and coverage gaps.
- **INNOVATE Mode**: When proposing solutions, strictly requires architectural design based on SOLID and KISS principles, along with detailed assessment of solution testability.
- **PLAN Mode**: **Mandates the detailed formulation of test cases (TDD)**, including unit, integration, and functional tests, with clear assertions, expected outcomes, real interface usage, and error handling, before any code implementation. The entire plan is converted into a detailed, atomic, numbered execution checklist.
- **EXECUTE Mode**: **Strictly adheres to the TDD Red-Green-Refactor cycle**. Allows reporting and execution of "minor deviations." After each step, it mandates updating detailed development progress and requesting user confirmation. If user feedback indicates issues, it automatically reverts to the PLAN mode.
- **REVIEW Mode**: Enforces **rigorous Feature Verification Matrix** comparison, **comprehensive Test Quality Assessment** (including verification that all tests use real interfaces and explicit error handling), and in-depth evaluation of the final implementation's adherence to SOLID and KISS principles.

**Stricter Code Handling Standards**:
- Standardized code block structure explicitly requiring file paths and language identifiers.
- Detailed editing guidelines prohibiting the use of unverified dependencies, incomplete code, untested code, and modifications of unrelated code.

## RIPER Protocol Version Comparison and Recommendation

### Table 1: Protocol Core Overview

| Protocol Version | Core Philosophy | Mode Switching | Thinking Principles | Documentation Management |
| :---------------------------- | :---------------------------------------------------------------------------------------------------- | :------------------------------------------------- | :----------------------------------------------------- | :-------------------------------------------------- |
| RIPER-5 01 Version | Preliminary concept of RIPER's five modes. | Manual and strict, requires explicit commands. | Basic process-oriented. | No explicit mandatory documentation requirements. |
| RIPER-5 Multidimensional Thinking + Agent Execution Protocol | Introduces multidimensional thinking (systems, dialectical, innovative, critical) and agent execution on top of RIPER. | Automatic mode switching, AI intelligently selects starting mode. | Emphasizes systems, dialectical, innovative, and critical thinking. | Introduces task file templates, ensuring traceability. |
| RIPER-5 TDD-Agile + SOLID/KISS Protocol | Deeply integrates TDD, Agile, SOLID, and KISS principles, focusing on quality, simplicity, and maintainability. | RESEARCH and INNOVATE switch automatically, but **user approval is mandatory after INNOVATE before entering PLAN**; all subsequent modes execute automatically after PLAN, but **skipping PLAN directly to EXECUTE is prohibited**. | Additionally emphasizes test-driven thinking, simplicity-focused design, and SOLID architectural planning. | Mandates all structured documentation (`001-dev-doc` directory), and clarifies documentation update responsibilities in each mode. |

### Table 2: Protocol Effects & Applications

| Protocol Version | Testing Integration | Code Standards | Pros | Cons | Recommended Scenarios |
| :---------------------------- | :--------------------------------------------------- | :------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------ |
| RIPER-5 01 Version | No explicit testing requirements. | No explicit code handling standards. | Simple and easy to understand, quick to get started, suitable for very simple or personal projects. | Too simplified, lacks flexibility, intelligence, and quality assurance, prone to errors, not suitable for complex projects. | Beginners learning RIPER process; extremely small, non-critical projects. |
| RIPER-5 Multidimensional Thinking + Agent Execution Protocol | No explicit mandatory TDD or test case writing requirements, but execution mode updates progress and requests feedback. | Defines unified code block structure, prohibits unverified dependencies or irrelevant changes. | Improves efficiency, more comprehensive analysis, optimized and creative solutions, enhanced traceability and code quality. | Lacks strict quality assurance of TDD, testing requirements are less explicit than the latest version. | Teams requiring AI intelligent assistance, moderate project complexity, certain standardization requirements, but not strict TDD requirements. |
| RIPER-5 TDD-Agile + SOLID/KISS Protocol | Enforces TDD Red-Green-Refactor cycle, writes tests first (requires real interfaces, clear error reporting), PLAN mode mandates detailed test case formulation, EXECUTE mode strictly follows TDD, REVIEW mode mandates feature verification matrix and test quality assessment. | Stricter unified code block structure, detailed editing guidelines and prohibited behaviors. | Greatly improves software quality, maintainability, and stability; rigorous process, extremely strong traceability; ensures application of best practices. | Steeper learning curve, more complex and strict process, may introduce overhead in small or rapid prototyping projects. | High-quality requirements, complex, long-term maintenance projects; teams with TDD and SOLID experience; enterprise-level development requiring strict standardization and traceability. |

