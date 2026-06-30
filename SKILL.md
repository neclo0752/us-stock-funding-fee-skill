# US Stock Funding Fee

## Purpose
用于比较汇丰香港 <-> 嘉信的双向资金路径手续费与折损：
- 入金：汇丰香港 -> 嘉信（inflow）
- 出金：嘉信 -> 汇丰香港（outflow）

## Required Inputs
- `direction`（必填）：`inflow` 或 `outflow`
- `amount`（必填）
- `currency`（必填）：`USD` 或 `HKD`
- `rate`（可选）：默认 `7.8`

## Core Rules
严格按 `references/calculation-rules.md` 执行；不可混用入金/出金费率。

## Output Requirements
- 必须输出对应方向下 5 个方案（不省略）
- 输出：方案、手续费、折算、备注
- 给出最低手续费方案 + 前提
- 给出关键交叉点
- 给出稳定性/风控提示
- 附免责声明
