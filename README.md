# HW10 — JSON Mode & Tool Calling (LiteLLM)

Tho parts:

**- Schema-validated extractor**

**- Currency mini-agent (simulated)**

---

## 1) Schema-Validated Extractor  
>Nested JSON with a strict schema.  

**Input:** order text → **Output:** structured JSON  
messages = [
  {"role": "system", "content": "Return ONLY a JSON object matching the schema."},
  {"role": "user", "content": "Order A-1029 by Sarah Johnson : 2x Water Bottle ($12.50 each), 1x Carrying Pouch ($5). Total $30."}
]

response_format={"type": "json_schema", "json_schema": schema},
)

Result:  

![Schema Result](screenshots/schema_result.png)

---

## 2) Currency Mini-Agent  
>Tool calling with mock exchange rates.  

We tested 5 cases:


### Case 1 — 100 USD → THB  

Result: 
![USD to THB](screenshots/USD_THB.png)


### Case 2 — 250 baht → EUR  

Result: 
![THB to EUR](screenshots/THB_EUR.png)


### Case 3 — 50 pesos → USD *(unsupported → list options)*  

Result: 
![Pesos to USD](screenshots/PESOS_USD.png)


### Case 4 — 10 EUR → USD  

Result: 
![EUR to USD](screenshots/EUR_USD.png)


### Case 5 — 500 USD → USD  

Result: 
![USD to USD](screenshots/USD_USD.png)


---

## P.S.
- Using 'temperature=0.2' for stable tool selection  
