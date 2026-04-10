# AI Guideline

## Overview

These constraints help protect the stability of the requirement baseline by preventing implicit changes, uncontrolled behavior introduction, and context contamination.

However, they must be enforced through explicit change workflows and traceability mechanisms to be fully effective.

## Rules

1. All information directly provided by the user must be classified as a `Requirement` when incorporated into `Spec` or `Plan`.
2. AI **MUST NOT** introduce any behavior that is not explicitly defined in `Spec`.
3. AI must not directly modify `Spec` or `Plan`. It should first ask questions or propose suggestions (in bullet-point form) and obtain explicit approval before making any changes.

## Working Modes

### 1. Requirement Mode

Used when the current task is requirement clarification, scope definition, schema/spec drafting, or rule review.

In this mode, AI:
- may整理需求、补充问题、生成 `Requirement` / `Plan` / `Schema` / `Spec` 草稿
- may review consistency, identify gaps, and propose options
- **must not modify production code, test code, or runtime configuration**
- **must not implement features or fix bugs directly**

### 2. Development Mode

Used only after requirements and spec constraints are sufficiently明确 and implementation is explicitly requested or approved.

In this mode, AI:
- may modify code, tests, and supporting configuration
- must implement changes under approved `Spec` constraints
- must keep implementation traceable to requirement and spec decisions

---

## 中文说明

这些约束可以通过防止隐式变更、控制行为扩展以及避免上下文污染，从而有效保护需求基线的稳定性。

但要完全发挥作用，还需要配合明确的变更流程和可追溯机制。

## 规则

1. 所有直接来自用户的信息，在进入 `Spec` 或 `Plan` 时，必须标记为需求（`Requirement`）。
2. AI 不得引入任何未在 `Spec` 中明确规定的行为。
3. AI 不得直接修改 `Spec` 或 `Plan`。在进行任何修改之前，必须先通过提问或以要点形式提出建议，并获得明确批准。

## 工作模式

### 1. 需求模式（Requirement Mode）

当任务处于需求整理、范围界定、`Schema` / `Spec` 起草、规则评审阶段时，应进入需求模式。

在该模式下，AI：
- 可以整理需求、提出问题、补充方案、生成 `Requirement` / `Plan` / `Schema` / `Spec` 草稿
- 可以做一致性检查、边界分析和差距识别
- **不得修改生产代码、测试代码或运行时配置**
- **不得直接实现功能或修复缺陷**

### 2. 开发模式（Development Mode）

仅当需求和规范已经足够明确，且用户已明确要求或批准进入实现阶段时，才进入开发模式。

在该模式下，AI：
- 可以修改代码、测试和配套配置
- 必须在已确认的 `Spec` 约束下实施修改
- 必须保证实现可追溯到需求和规范决策
