# ⚙️ Pre-Setup: Install Apache JMeter (Windows & macOS)

## 📌 Overview

This guide explains how to install **Apache JMeter**, a tool used for load and stress testing.

---

## 🛠️ Prerequisites

Before installing JMeter, you must install:

### ☕ Java (Required)

JMeter requires Java (JDK 8 or higher)

### Check if Java is installed:

```id="checkjava"
java -version
```

If not installed, download from:

* https://adoptium.net/

---

# 🪟 Installation on Windows

## Step 1: Download JMeter

* Go to: https://jmeter.apache.org/download_jmeter.cgi
* Download the **.zip file (Binary)**

---

## Step 2: Extract Files

* Right click the `.zip` file
* Extract to a folder (e.g., `C:\jmeter`)

---

## Step 3: Run JMeter

* Open folder: `bin`
* Double click:

```id="winrun"
jmeter.bat
```

👉 JMeter GUI will launch

---

# 🍎 Installation on macOS

## Option 1: Using Homebrew (Recommended)

### Step 1: Install Homebrew (if not installed)

```id="brewinstall"
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Step 2: Install JMeter

```id="brewjmeter"
brew install jmeter
```

### Step 3: Run JMeter

```id="runjmeter"
jmeter
```

---

## Option 2: Manual Installation

### Step 1: Download JMeter

* https://jmeter.apache.org/download_jmeter.cgi

### Step 2: Extract the file

### Step 3: Run JMeter

```id="macrun"
cd apache-jmeter/bin
./jmeter
```

---

# ✅ Verify Installation

When JMeter opens, you should see:

* Test Plan (main screen)
* Menu bar (File, Edit, Run, etc.)

👉 If GUI opens successfully = installation complete 🎉

---

# ⚠️ Troubleshooting

## Java not found

* Install JDK and restart terminal

## JMeter won’t open

* Check Java version
* Ensure correct folder (`bin`) is used

---

# 🎓 Ready for Next Step

Now you are ready to:

* Run Load Testing
* Run Stress Testing
* Explore system performance

👉 Continue to:

* [Load Testing Guide](01-load-test.md)

---
