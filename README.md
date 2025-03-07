🔍 Automated Port Scanner

🔥 Multi-threaded Python Port Scanner for Fast Network Reconnaissance

This Python-based scanner quickly identifies open ports on a target machine. It's fast, lightweight, and supports hostname resolution.

📦 Installation

Clone from GitHub

git clone https://github.com/yourusername/port-scanner.git
cd port-scanner
python3 port_scanner.py

Run without cloning

curl -O https://raw.githubusercontent.com/yourusername/port-scanner/main/port_scanner.py
python3 port_scanner.py

🛠 Features

 -🚀 Multi-threaded scanning for faster results

 -🌐 Hostname resolution support

 -📜 Customizable scan ranges


🚀 Usage Example

python3 port_scanner.py
Enter target IP: 192.168.1.1
Scanning 192.168.1.1...
[+] Port 22 is open
[+] Port 80 is open
Scan complete!

🔥 Potential Improvements

 -🏗 Service detection (using socket.getservbyport(port)).

 -📄 Logging support for output storage.

- 📊 GUI interface for ease of use.

- 🔗 Nmap Integration for advanced scanning features.
