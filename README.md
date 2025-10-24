# Serverless-Function
AWS Lambda serverless function deployment.

# Task 4: Deploy a Serverless Function to the Cloud

---

## Objective
The goal of this task is to understand **serverless computing** by creating and deploying a simple **cloud function (FaaS)** that runs automatically when triggered — without managing servers.  
This task demonstrates **event-driven computing**, **resource optimization**, and **cost-effective cloud deployment**.

---

## Tools Used
- **Cloud Platform:** AWS Lambda (Free Tier)  
- **Language:** Python 3.x  
- **Testing:** Web browser (Function URL)

---

## Deliverables
1. **Source Code:** `lambda_function.py`  
2. **Screenshots:**  
   - Code deployed in AWS Lambda  
   - Function URL configuration  
   - Function output in browser  
3. **Function URL:** `<paste-your-function-url-here>`  
4. **Short Explanation**

---

## Source Code (`lambda_function.py`)
```python
import json

def lambda_handler(event, context):
    params = event.get("queryStringParameters") or {}
    name = params.get("name") or "Guest"
    return {
        "statusCode": 200,
        "headers": {"Content-Type": "text/plain"},
        "body": f"Hello, {name}! Welcome to my cloud function."
    }

## How It Works
- This AWS Lambda function is **serverless**, triggered via an HTTP Function URL.  
- It reads an optional `name` parameter from the request URL and returns a greeting message.  
- If no `name` is provided, it defaults to `"Guest"`.  
- Demonstrates **event-driven architecture** and **FaaS (Function-as-a-Service)** in AWS.

---

## Testing
1. Open the Function URL in a browser:  
https://<your-function-url>/

vbnet
Copy code
Output: `Hello, Guest! Welcome to my cloud function.`

2. Test with query parameter `name`:  
https://<your-function-url>?name=Aishwarya

yaml
Copy code
Output: `Hello, Aishwarya! Welcome to my cloud function.`

---

## Screenshots
- **Code deployed in Lambda** → `code_deployed.png`  
- **Function URL** → `function_url.png`  
- **Function output** → `function_output.png`  

---

## What I Learned
- Understood **serverless computing** and **FaaS (Function-as-a-Service)**.  
- Learned how to deploy a cloud function on **AWS Lambda** without managing servers.  
- Learned to use **HTTP triggers / Function URL** to execute the function on demand.  
- Learned to accept query parameters and return **dynamic responses**.  
- Gained hands-on experience with **event-driven architecture**, **cloud function testing**, and **free-tier deployment**.  

---

## Outcome
- Built confidence in deploying serverless functions and testing them.  
- Gained practical knowledge of **cloud automation** and **event-based execution**.
