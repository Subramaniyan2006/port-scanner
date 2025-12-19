## 📄 Description

This project is a **TCP Port Scanner built using Python** that allows users to **manually enter an IP address or hostname** and scan a specified range of ports on that target system.

The scanner validates user input, resolves hostnames to IP addresses, and safely scans ports using **multi-threading** for speed. It clearly displays:

* Total ports scanned
* Number of open ports
* Number of closed ports
* A separate list of **only open ports**

The program is designed to be **stable, beginner-friendly, and crash-resistant**, even when invalid inputs are provided.

## ✨ Features

* 🔹 Manual user input for **IP address or hostname**
* 🔹 Automatic **hostname → IP resolution (DNS)**
* 🔹 Custom **port range scanning** (example: `1-1024`)
* 🔹 Fast scanning using **ThreadPoolExecutor**
* 🔹 Safe thread limits to avoid crashes
* 🔹 Input validation for:

  * Invalid IP addresses
  * Invalid hostnames
  * Invalid port ranges
* 🔹 Displays:

  * Total ports scanned
  * Number of open ports
  * Number of closed ports
  * **Only open ports separately**
* 🔹 Works on Windows, Linux, and macOS
* 🔹 No external libraries required
  
## 🛠 Technologies Used

* **Python 3**
* **socket** – for TCP connections and port scanning
* **ipaddress** – for IP address validation
* **re (Regular Expressions)** – for hostname validation
* **concurrent.futures.ThreadPoolExecutor** – for multi-threaded scanning
* **os** – to calculate safe thread limits based on CPU
  
## ▶ How to Run the Program

### 1️⃣ Prerequisites

* Python **3.8 or higher**
* No additional packages required

### 2️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/tcp-port-scanner.git
cd tcp-port-scanner
```

### 3️⃣ Run the Program

```bash
python port_scanner.py
```

### 4️⃣ Example Input

```text
Enter IP address or Hostname: localhost
Enter port range (default 1-1024): 1-100
```

### 5️⃣ Example Output

```text
===== SCAN SUMMARY =====
Total ports scanned : 100
Open ports          : 2
Closed ports        : 98

===== OPEN PORTS =====
Port 22 is OPEN
Port 80 is OPEN
```

