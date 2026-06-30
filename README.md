# us-stock-funding-fee

用于比较“汇丰香港 <-> 嘉信”双向路径的手续费与折损，支持一键给出 5 方案成本、最低成本方案、关键交叉点和风险提示。

## 1) 支持场景

- `inflow`：汇丰香港入金嘉信
- `outflow`：嘉信出金汇丰香港

## 2) 你需要提供什么

最少 3 个参数：
- `direction`：`inflow` 或 `outflow`
- `amount`：金额（数字）
- `currency`：`USD` 或 `HKD`

可选参数：
- `rate`：USDHKD 汇率（不传默认 `7.8`）

建议输入习惯：
- 金额尽量写纯数字，比如 `10000`，不要写 `1w`、`十万`
- 若是港币金额，明确标注 `currency=HKD`
- 如果你有自己的实时汇率，请主动给 `rate`

## 3) 怎么提问（可直接复制）

### A. 最标准话术

```text
请按 us-stock-funding-fee 计算：
direction=outflow
amount=10000
currency=USD
rate=7.82
请输出5个方案成本、最低成本方案、交叉点和风险提示。