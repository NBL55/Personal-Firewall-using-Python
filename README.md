# Personal-Firewall-using-Python
This project implements a basic Personal Firewall using Python and the Scapy library. It monitors real-time network traffic and blocks packets based on user-defined rules for IP addresses and TCP ports. The firewall logs all blocked activity for review.
Project Summary
This project implements a basic **Personal Firewall** using Python and the Scapy library. It monitors real-time network traffic and blocks packets based on user-defined rules for IP addresses and TCP ports. The firewall logs all blocked activity for review.

## 🛠 Features
- ✅ Real-time network traffic monitoring  
- ✅ Blocks packets from/to specific IPs  
- ✅ Blocks packets from/to specific TCP ports (e.g., 80, 443)  
- ✅ Logs all blocked packets with timestamp and reason  

## 📂 Folder Structure
D:/Personal Firewall using Python/
├── firewall.py
├── firewall_logs.txt
├── screenshots/
│ ├── terminal_output.png
│ └── log_file.png
└── README.md

markdown
Copy
Edit

## 🚀 How It Works
1. Uses `scapy.sniff()` to monitor live packets  
2. Filters traffic using two lists:  
   - `BLOCKED_IPS = ["192.168.1.10"]`  
   - `BLOCKED_PORTS = [80, 443]`  
3. Flags and logs blocked packets to `firewall_logs.txt`  
4. Allows all other packets and displays `[ALLOWED]` in the terminal  

## 📄 Sample Log Format
[2025-07-27 14:05:32.123456] BLOCKED: Port Block | IP / TCP 172.217.160.78:443 > 192.168.1.5:55600

markdown
Copy
Edit

## 🔧 Setup Instructions

### 📌 Requirements
- Python 3.10 or newer  
- [Scapy library](https://scapy.net)

### 📥 Install Scapy
```bash
pip install scapy
🔐 Run as Administrator
You must run this with elevated privileges:

Windows: Right-click VS Code or Terminal → Run as Administrator

Linux/macOS: Use sudo python firewall.py

🏁 Start the Firewall
bash
Copy
Edit
cd "D:/Personal Firewall using Python"
python firewall.py
🖥 Output
Live terminal view showing allowed/blocked packets

Log file automatically created at:

vbnet
Copy
Edit
D:/Personal Firewall using Python/firewall_logs.txt
📸 Screenshots
Terminal Output:

Log File Example:

⚙️ Limitations
Packet detection only (does not drop packets at kernel level)

Not a replacement for system firewalls (like Windows Defender or iptables)

No GUI — CLI only

🔮 Possible Extensions
Add Tkinter GUI for rule editing

Use psutil to map traffic to processes

Convert logs to JSON/CSV for advanced analysis

📚 Use Cases
Mini project for cybersecurity students

Internship demonstration tool

Packet filtering logic simulation

👨‍💻 Author
Nabeel Basheer M

📅 Date
27 July 2025

