🔐 Log Analyzer

A simple Python cybersecurity tool that analyzes login logs and detects IP addresses with repeated failed login attempts.

📌 Features
Analyze a log file selected by the user
Count total log entries
Count successful login attempts
Count failed login attempts
Track failed attempts by IP address
Set a custom failed-login limit
Display warnings for IPs that exceed the limit
Detect invalid log entries
Handle missing files and permission errors
Validate user input
🛠️ Requirements
Python 3.x

No external Python libraries are required.

📂 Project Structure
Log-Analyzer/
│
├── log_analyzer.py
├── logs.txt
└── README.md
📝 Log Format

The analyzer expects logs in this format:

YYYY-MM-DD HH:MM:SS IP STATUS

Example:

2026-09-27 18:01:22 192.168.1.10 LOGIN_SUCCESS
2026-09-27 18:02:15 192.168.1.15 LOGIN_FAILED
2026-09-27 18:03:41 192.168.1.10 LOGIN_SUCCESS
2026-09-27 18:04:03 192.168.1.15 LOGIN_FAILED
▶️ Usage

Run the program:

python log_analyzer.py

The program will ask for the log file path:

Enter log file path: logs.txt

Then enter the number of failed attempts that should trigger a warning:

Enter failed login limit: 3
📊 Example Output
========================================
           LOG ANALYZER
========================================
Total Logs: 8
Successful Logins: 4
Failed Logins: 4
Invalid Logs: 0

Failed Login Attempts by IP:
----------------------------------------
192.168.1.15 -> 4 failed attempts
[!] WARNING: 192.168.1.15 exceeded the limit!
========================================
🎯 Purpose

This project was created as a cybersecurity learning project to practice:

Python file handling
Loops
Conditional statements
Dictionaries
Exception handling
String processing
Basic security log analysis

It demonstrates how a simple Python script can process authentication logs and identify repeated failed login attempts.

⚠️ Note

logs.txt contains sample data for testing.

Only analyze log files that you own or have permission to access.

🚀 Future Improvements

Possible future improvements include:

Support for Apache and Nginx logs
Exporting analysis reports
Date and time filtering
More authentication event types
Command-line arguments
Improved log format detection
👨‍💻 Author

Aarif
