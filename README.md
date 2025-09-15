# hw10 — Structured Outputs (JSON Mode) & Tool Calling (LiteLLM)

Two parts:
1) **Schema-validated extractor (nested JSON)**
2) **Currency mini-agent (simulated) using tool calling**


## json_mode_schema.py
messages = [
  {"role":"user","content":"Order A-1029 by Sarah Johnson : WB-500; 2x Water Bottle ($12.50 each), CP-010; 1x Carrying Pouch ($5). Total $30. sj@example.com. "}
]
![Schema](screenshots/schema_result.png)
## tc_complete_currency.py
ex.run("Convert 100 USD to THB")
![USD to THB](screenshots/USD_THB.png)
ex.run("Convert 250 baht to euros")
![THB to EUR](screenshots/THB_EUR.png)
ex.run("Convert 50 PESOS to USD")
![PESOS to USD](screenshots/PESOS_USD.png)
ex.run("Convert 10 euros to yens")
![EUR to USD](screenshots/EUR_USD.png)
ex.run("Convert 500 dollars to rupees")
![USD to USD](screenshots/USD_USD.png)
