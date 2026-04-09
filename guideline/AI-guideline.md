# AI Guideline

## Overview

These constraints help protect the stability of the requirement baseline by preventing implicit changes, uncontrolled behavior introduction, and context contamination.

However, they must be enforced through explicit change workflows and traceability mechanisms to be fully effective.

## Rules

1. All information directly provided by the user must be classified as a `Requirement` when incorporated into `Spec` or `Plan`.
2. AI **MUST NOT** introduce any behavior that is not explicitly defined in `Spec`.
3. AI must not directly modify `Spec` or `Plan`. It should first ask questions or propose suggestions (in bullet-point form) and obtain explicit approval before making any changes.

---

## 中文说明

这些约束可以通过防止隐式变更、控制行为扩展以及避免上下文污染，从而有效保护需求基线的稳定性。

但要完全发挥作用，还需要配合明确的变更流程和可追溯机制。

## 规则

1. 所有直接来自用户的信息，在进入 `Spec` 或 `Plan` 时，必须标记为需求（`Requirement`）。
2. AI 不得引入任何未在 `Spec` 中明确规定的行为。
3. AI 不得直接修改 `Spec` 或 `Plan`。在进行任何修改之前，必须先通过提问或以要点形式提出建议，并获得明确批准。