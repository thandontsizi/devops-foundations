# JSON Fundamentals Tests:
## 1. Concept Check:
### Question:
- What is JSON, and what problem does it solve?

---

## 2. Objects vs Arrays:
- Consider:
```bash
{
	"name": "Thando",
	"age": 23
}
```
- and:
```bash
[
	"SQL",
	"Python",
	"Linux"
]
```

### Questions:
1. What does the object represent?
2. What does the array represent?
3. Why would an object be more appropriate for representing one customer than an array?

---

## 3. Key/Value Pairs:
- Given:
```bash
{
	"name": "Thando Ntsizi",
	"age": 23,
	"active": true
}
```
- Identify:
1. The keys.
2. The values.
3. The data type of each value.

---

## 4. JSON Value Types:
- Identify the JSON value type of each:
```bash
1. "Thando":
2. 23:
3. 23.5:
4. true:
5. false:
6. null:
7. [1, 2, 3]:
8. {"name": "Thando"}:
```

---

## 5. Nested Structure:
- Consider:
```bash
{
	"name": "Thando",
	"orders": [
		{
			"order_id": 1001,
			"total": 450
		},
		{
			"order_id": 1002,
			"total": 275
		}
	]
}
```
### Questions:
1. What is the outermost structure?
2. What is the data type of the orders value?
3. What does each element inside orders represent?
4. Why are the individual orders objects rather than simple values?

---

## 6. Valid or Invalid?
- Determine whether each example is valid JSON. If **invalid**, explain why.

### A.
```bash
{
	"name": "Thando",
	"age": 23
}
```
### B.
```bash
{
	"name": "Thando",
	"age": 23,
}
```
### C.
```bash
{
	"name": "Thando",
	"active": True
}
```
### D.
```bash
{
	"name": "Thando",
	"active": true
}
```
### E.
```bash
{
	name: "Thando"
}
```

---

## 7. Data Type Reasoning:
- Consider:
```bash
{
	"age": 23
	"age_as_text": "23"
}
```

### Question:
- What is the difference between these two values, and why might that difference matter to a system consuming the JSON?

---

## 8. Null vs Missing vs Empty:
- Consider these three examples:

#### A.
```bash
{
	"middle_name": null
}
```
#### B.
```bash
{
	"middle_name": ""
}
```
#### C.
```bash
{
	"name": "Thando"
}
```

### Question:
- What is different about the meaning and structure of these three cases?

---

## 9. Investigation Scenario:
- You receive the following API response:
```bash
{
	"customer_id": 1847,
	"name": "Thando Ntsizi",
	"status": 3
}
```
- You know that "customer_id" identifies the customer.
- You do not know what "status: 3" means.

### Questions:
1. What can you state as an observation?
2. What would be an assumption?
3. What evidence would you look for to determine what "3" means?
4. What would you investigate next?

---

## 10. Investigation Scenario:
- An API normally returns:
```bash
{
	"customers": [
		{
			"customer_id": 1847,
			"name": "Thando Ntsizi"
		}
	]
}
```
- Today it returns:
```bash
{
	"customers": []
}
```

### Questions:
1. What do you know from the response?
2. What can you not conclude yet?
3. Give at least three possible explanations for the empty array.
4. What would you investigate first?

---

## Test Approach:
- These tests should be answered by reasoning through the structure and meaning of the data rather than relying on syntax memorisation.
- When investigating JSON, distinguish between:
```bash
		Observation 
			↓ 
		Evidence 
			↓
		Hypothesis 
			↓ 
		  Test 
			↓ 
		 Result 
			↓ 
		Conclusion
```
