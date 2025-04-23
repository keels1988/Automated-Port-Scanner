# 🚀 Simple Port Scanner

A lightweight, easy-to-understand port scanner script written in Python. Ideal for cybersecurity students, hobbyists, and penetration testers who want to understand the basics of socket programming and host enumeration.

---

## 📊 Features

- Scans for open TCP ports on a given target IP or hostname
- Accepts a port range (e.g., 1-1024)
- Provides clean console output
- Written in under 50 lines of code

---

## 📁 Project Structure

```bash
.
├── port_scanner.py
└── README.md
```

---

## 📝 Usage

### 1. Clone the repo
```bash
git clone https://github.com/your-username/simple-port-scanner.git
cd simple-port-scanner
```

### 2. Run the scanner
```bash
python3 port_scanner.py
```

### 3. Example Output
```
Target: 192.168.1.1
Scanning ports 20 to 1024...
[+] Port 22 is open
[+] Port 80 is open
[+] Port 443 is open
Scan completed.
```

---

## 📄 Code Overview

<details>
<summary>Click to view code</summary>

```python
import socket
from datetime import datetime

# Target input
target = input("Enter target IP or hostname: ")
start_port = int(input("Enter start port: "))
end_port = int(input("Enter end port: "))

print(f"\nTarget: {target}")
print(f"Scanning ports {start_port} to {end_port}...")
print("Scan started at:", datetime.now())

try:
    for port in range(start_port, end_port + 1):
        s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        s.settimeout(0.5)
        result = s.connect_ex((target, port))
        if result == 0:
            print(f"[+] Port {port} is open")
        s.close()
except KeyboardInterrupt:
    print("\nScan interrupted by user.")
except socket.gaierror:
    print("Hostname could not be resolved.")
except socket.error:
    print("Could not connect to server.")

print("Scan completed.")
```

</details>

---

## 🪨 Legal Disclaimer

This tool is for **educational purposes only.** Scanning systems you do not own or have explicit permission to test is illegal and unethical.

---

## 🛠️ Contribute

Want to add support for UDP scanning, multithreading, or banners? PRs are welcome!

---

## 🌟 Star the project if it helped you, and share it with fellow cybersecurity learners!

