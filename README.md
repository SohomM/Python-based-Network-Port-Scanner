Network Port Scanner

i. Building a simple port scanner using Python (Scapy/Socket) to detect open ports on a target system.
ii. Enhance it with service detection (e.g., HTTP, FTP, SSH).

--------------------------------------------------------------------------

This script uses socket for basic port scanning and includes features like:

1.Scanning common ports or a custom range
2.Detecting open ports with service names
3.Simple multithreading for faster scans

install dependencies: pip install Ipy

Features & Customizations:
Multithreading: Scans multiple ports simultaneously for speed.
Service Detection: Maps open ports to known services (e.g., port 80 → HTTP).
Error Handling: Skips unresponsive ports gracefully.

------------------------------------------------------------------------------
Example Output:
Enter target IP or domain: scanme.nmap.org
Scan common ports (Y/n)? Y

Scanning target: 45.33.32.156
[+] Port 22 (ssh) is open
[+] Port 80 (http) is open

-------------------------------------------------------------------------------
Next-Level Enhancements:
1.Add banner grabbing to fetch service versions.
2.Integrate with Nmap (Python python-nmap library).
3.Export results to a CSV/PDF report.

----------------------------------------------------------------------------------

Key Features
Nmap Power: Uses -sV (service detection) and -O (OS fingerprinting).

Threaded Scans: Faster than sequential scanning.

Professional Reporting: Ready for client deliverables.

-------------------------------------------------------------------------------------
If you're getting ModuleNotFoundError for Nmap or path issues, here’s how to fix it and run the scanner correctly in Jupyter Notebook:
  Problem 1: Python-Nmap Not Installed
Even if nmap (the command-line tool) is installed, you need the Python wrapper:
!pip install python-nmap  # Run this in Jupyter first

  Problem 2: Nmap Not in System PATH
Ensure nmap is installed system-wide and accessible:

Windows: Download Nmap from nmap.org and check "Add to PATH" during installation.

Linux/macOS: Install via package manager:
sudo apt install nmap          # Debian/Ubuntu
brew install nmap             # macOS
------------------------------------------------------------------------
How to Run:
   Verify Nmap PATH:

If you’re on Windows, ensure nmap.exe is in your system PATH (check with !where nmap in Jupyter).

On Linux/macOS, run !which nmap to verify.

Execute the Scanner:

Paste the code into a new Jupyter cell and run it.

--------------------------------------------------------------------------
EXPECTED OUTPUT:

Enter target IP/Domain: scanme.nmap.org
Enter ports (e.g., '22,80,443' or '1-1000'): 22,80

Scanning scanme.nmap.org on ports 22,80...

Results for 45.33.32.156:
Port: 22/tcp | State: open | Service: ssh | Version: OpenSSH 6.6.1
Port: 80/tcp | State: open | Service: http | Version: Apache 2.4.7
