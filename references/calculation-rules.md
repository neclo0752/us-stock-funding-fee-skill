# Calculation Rules

## Variables
- `A`: 输入金额
- `C`: `USD`/`HKD`
- `R`: USDHKD，默认 `7.8`
- `D`: `inflow`/`outflow`

若 `C=USD`：`A_usd=A`，`A_hkd=A*R`
若 `C=HKD`：`A_hkd=A`，`A_usd=A/R`

## D = inflow（汇丰香港 -> 嘉信）
1. 方案一：`fee1_usd = A_usd * 0.0016`
2. 方案二：`fee2_usd = 21.88`
3. 方案三：`fee3_usd = A_usd * 0.004`
4. 方案四：`fee4_hkd = 10`（`fee4_usd = 10 / R`）
5. 方案五：`fee5_usd = 0`

交叉点（方案一 vs 二）：`13,675 USD`（约 `106,665 HKD`）

## D = outflow（嘉信 -> 汇丰香港）
1. 方案一：`15~50 USD`
2. 方案二：`9.57 USD`
3. 方案三：`A_usd * 0.003`
4. 方案四：`0`（需 HSBC US）
5. 方案五：`2 USD`（IBKR 换汇费）

交叉点（方案二 vs 三）：
`9.57 / 0.003 = 3190 USD`
- `A_usd > 3190`：通常方案二更低
- `A_usd < 3190`：通常方案三更低
