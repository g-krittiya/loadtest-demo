# 🔐 Security Testing Guide (Basic Demo)

## 📌 Overview

This guide demonstrates a **basic security testing concept** using simple techniques.

The goal is to understand:

* How vulnerabilities happen
* Why input validation is important
* How attackers exploit weak systems

---

## 🎯 Objective

* Understand common security vulnerabilities
* Simulate unsafe input
* Learn how systems should defend against attacks

---

## ⚠️ Important Notice

* This demo is for **educational purposes only**
* Do NOT test real production systems
* Use only safe/demo environments

---

# 🧪 Demo 1: Input Injection (Concept Simulation)

## Scenario

A system accepts user input (e.g., login or search)

---

## Step 1: Normal Input

Example:

```id="n1"
username=student
password=1234
```

👉 System behaves normally

---

## Step 2: Malicious Input

Try:

```id="n2"
' OR '1'='1
```

👉 Explain:

* This input manipulates backend logic
* It may bypass authentication

---

## 🧠 What Happens Behind the Scene

### Normal query:

```id="n3"
SELECT * FROM users WHERE username='student'
```

### Injected query:

```id="n4"
SELECT * FROM users WHERE username='' OR '1'='1'
```

👉 Always true → returns all users

---

# 💥 Key Insight

> Systems that trust user input are vulnerable

---

# 🛡️ Prevention Techniques

## Fix:

* Use **input validation**
* Use **parameterized queries**
* Avoid dynamic SQL

---

# 🧪 Demo 2: API Security Check (JMeter)

## Objective

Test how API handles unexpected or invalid input

---

## ⚙️ Steps in JMeter

### 1. Add HTTP Request

* Method: POST
* URL:

```id="n5"
https://httpbin.org/post
```

---

### 2. Add JSON Body

```json id="n6"
{
  "username": "admin",
  "password": "' OR '1'='1"
}
```

---

### 3. Add Header

| Name         | Value            |
| ------------ | ---------------- |
| Content-Type | application/json |

---

### 4. Run Test

👉 Observe response

---

## 🔍 What to Check

* Does system reject invalid input?
* Does it return proper error?
* Does it expose sensitive data?

---

# 💡 What Good Systems Should Do

* Reject malicious input
* Return safe error messages
* Log suspicious activity

---

# 🔗 Architecture Insight

Security is an **architecture characteristic**

It must be:

* Designed early
* Tested continuously
* Enforced in production

---

# 🎓 Key Takeaways

* Never trust user input
* Security must be tested, not assumed
* Small input can break big systems

---

# 🏁 Final Thought

> “Security is not about preventing all attacks —
> it’s about reducing risk and handling them safely.”

---
