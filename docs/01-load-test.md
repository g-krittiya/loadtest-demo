# 🧪 Load Testing Guide (JMeter)

## 📌 Overview

This guide demonstrates how to perform a **basic load test** using Apache JMeter.

Load testing helps evaluate how a system performs under **expected user traffic**.

---

## 🎯 Objective

* Simulate multiple users accessing a system
* Measure performance metrics
* Observe how the system behaves under load

---

## 🛠️ Requirements

* Apache JMeter installed
* Internet connection
* Test URL:

```
https://httpbin.org/get
```

---

## ⚙️ Step-by-Step Instructions

### 1. Create Test Plan

* Open Apache JMeter
* Use the default **Test Plan**

---

### 2. Add Thread Group (Users)

Right click:

```
Test Plan → Add → Threads → Thread Group
```

Set the following:

* Number of Threads (Users): **50**
* Ramp-up Period: **10 seconds**
* Loop Count: **1**

👉 This simulates 50 users accessing the system

---

### 3. Add HTTP Request

Right click:

```
Thread Group → Add → Sampler → HTTP Request
```

Set:

* Method: **GET**
* Server Name: **httpbin.org**
* Path: **/get**

---

### 4. Add Listener (Results)

Right click:

```
Thread Group → Add → Listener → Summary Report
```

(Optional)

```
Add → Listener → View Results Tree
```

---

### 5. Run the Test

* Click **Start (▶️)**
* Observe the results

---

## 📊 Key Metrics

* **Response Time** → How fast the system responds
* **Throughput** → Requests per second
* **Error Rate** → Percentage of failed requests

📎 See real example and interpretation:
👉 [Example Results](example-results.md)


---

## 🔥 Experiment

### Step 1: Normal Load

* Run test with **50 users**

### Step 2: Increased Load

* Change users to **200**
* Run again

---

## 📈 What to Observe

* Does response time increase?
* Does throughput change?
* Are there any errors?

👉 Compare results between 50 and 200 users

---

## 💡 Key Insight

* Performance depends on load
* Systems behave differently under higher traffic
* Testing is required to validate system performance

---

## ⚠️ Important Notes

* Do NOT test real production systems
* Use safe or test environments only
* Keep tests simple for learning

---

## 🎓 Conclusion

Load testing allows us to:

* Validate performance requirements
* Identify bottlenecks
* Make better architecture decisions

> “If you don’t test your system under load, you are just guessing.”

---
