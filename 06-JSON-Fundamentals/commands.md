# JSON Commands & Reference:

## 1. JSON Objects:
- Objects use curly braces "{}" to group related key/value pairs.
```bash
{
	"name": "Thando Ntsizi",
	"age": 23,
	"country": "South Africa"
}
```

## Key/Value Pairs:
- A key identifies what a value represents.
```bash
	"name": "Thando Ntsizi"
```
- **"name"**: key.
- **"Thando Ntsizi"**: value.
- **:**: separates the key from the value.

- **Multiple key/value pairs are separated by commas:**
```bash
{
	"name": "Thando Ntsizi",
	"age": 23,
	"active": true
}
```
---

## JSON Arrays:
- Arrays use square brackets "[]" to represent an ordered collection of values.
```bash
[
	"SQL",
	"Python",
	"Linux"
]
```
## Array of Objects:
- An array can contain different JSON value types, including objects and other arrays.
```bash
[
	{
		"name": "Thando",
		"age": 23
	},
	{
		"name": "Alex",
		"age": 24
	}
]
```

---

## 3. JSON Value Types:
- JSON supports six fundamental value types:
```bash
		Type		Example
	____________|_______________
		String	|	"Thando"
		Number	|	23
		Boolean	|	true
		Null	|	null
		Object	|{"name": "Thando"}
		Array	|["SQL", "Python"]
```
#### String:
- Text enclosed in double quotes.
- Example: "Thando Ntsizi"

#### Number:
- A numeric value.
- **Examples:** 23, 149.99, -4.5

#### Boolean:
- One of two values: true/false.
- Boolean values are not enclosed in quotation marks.

#### Null:
- Represents the absence of a value: null.
- For example:
```bash
{
	 "middle_name": null
}
```
- null is different from an empty string:
```bash
{
	"middle_name": ""
}
- It is also different from the key being absent entirely.

---

## 4. Nested JSON:
- JSON objects and arrays can contain other JSON values.

### Object Inside An Object:
```bash
{
	"name": "Thando",
	"address": {
		"city": "Cape Town",
		"country": "South Africa"
	}
}
```

### Array Inside An Object:
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
- This can be understood structurally as:
```bash
	Customer (Object) 
	├── name 
	└── orders (Array) 
		├── Order (Object) 
		└── Order (Object)
```

### Nested Arrays:
- Arrays can also contain other arrays.
```bash
[
	[1, 2],
	[3, 4],
	[5, 6]
]
```

---

## 5. JSON Syntax Rules:
- **Keys must use double quotes.**
- **Valid:**
```bash
{
	"name": "Thando"
}
```
- **Invalid:**
```bash
{
	name: "Thando"
}
```

- **Use a colon between a key and value:**
```bash
	"name": "Thando"
```

- **Separate multiple items with commas:**
```bash
{
	"name": "Thando",
	"age": 23,
	"active": true
}
```

- **Do not use trailing commas.**
- Valid:
```bash
{
	"name": "Thando",
	"age": 23
}
```
- Invalid:
```bash
{
	"name": "Thando",
	"age": 23,
}
```

- **JSON uses lowercase Boolean and null values:**
- Valid:
```bash
{
	"active": true,
	"verified": false,
	"middle_name": null
}
- Invalid:
```bash
{
	"active": True,
	"verified": False,
	"middle_name": None
}

---

## 6. Complete Nested Example:
```bash
{
	"customers": [
		{
			"customer_id": 1847,
			"name": "Thando Ntsizi",
			"age": 23,
			"country": "South Africa",
			"active": true,
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
		},
		{
			"customer_id": 3921,
			"name": "Alex Smith",
			"age": 24,
			"country": "South Africa",
			"active": false,
			"orders": []
		}
	]
}
```
- Structural interpretation:
```bash
Root Object 
└── customers (Array) 
	│ 
	├── Customer Object 
	│ 	├── customer_id 
	│ 	├── name 
	│ 	├── age 
	│ 	├── country 
	│ 	├── active 
	│ 	└── orders (Array) 
	│ 		├── Order Object 
	│ 		└── Order Object 
	│ 
	└── Customer Object 
		├── customer_id 
		├── name 
		├── age 
		├── country 
		├── active 
		└── orders (Array)
```

---

## 7. Working With JSON From the Terminal:
- JSON files can be inspected directly from the Linux command line.
- **Display a JSON File**:
```bash
	cat data.json
```
- **Search a JSON File**:
```bash
	grep "customer_id" data.json
```
- **Check Whether jq Is Installed**:
```bash
	jq --version
```
- **Format JSON For Easier Reading**:
```bash
	jq . data.json
```
- **jq** is a command-line JSON processor. It becomes particularly useful when working with API responses and large JSON documents.

---

## 8. Common JSON Investigation Checks:
- When given an unfamiliar JSON document, inspect it systematically.

#### 8.1 Identify The Outermost Structure:
- Ask: "Is the root an object or an array?"

#### 8.2 Identify The Keys:
- Determine what information is being represented.

#### 8.3 Identify Value Types:
- For each important value, determine whether it is:
	- String.
	- Number.
	- Boolean.
	- Null.
	- Object.
	- Array.

#### 8.4 Look For Nesting:
- Determine whether objects or arrays contain additional structures.

#### 8.5 Look For Collections:
- Identify arrays containing multiple records or values.

#### 8.6 Look For Missing Or null values:
- Determine whether a value is:
	- present,
	- null,
	- empty,
	- or absent.

#### 8.7 Do Not Assume Semantic Meaning:
- JSON describes structures and values, but the consuming system determines what those values mean.
- For example:
```bash
{
	"status": 3

}
```
- The JSON tells us that "status" has the number "3".
- It does not tell us what "3" means in the application.
- That meaning must be established using evidence such as documentation, system behaviour, database mappings, or application logic.
