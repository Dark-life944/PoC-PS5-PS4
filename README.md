### CVE-2022-23088 - FreeBSD Wi-Fi Stack Heap Overflow Exploit 

##  Proof-of-Concept (PoC) for exploiting a heap overflow in the FreeBSD Wi-Fi stack 


----------------------------

## 📌 Overview

CVE-2022-23088 is a heap overflow vulnerability in the Wi-Fi stack of FreeBSD, which can be exploited by sending specially crafted Wi-Fi frames.

✅ Work on FreeBSD 13.0=<
✅ Can be modified for PS4/PS5 with jailbreak ??

----------------------------

## 📂 Files Included

exploit.py → The main exploit script

shellcode.bin → Shellcode to be injected into memory

x86.py → Helper functions for calculating memory addresses

README.md → This documentation

LICENSE → License information



-----------------------------

## 🛠️ Requirements

🔹 Wi-Fi card that supports Monitor Mode
🔹 Linux environment (for running the exploit)
🔹 Python dependencies (pip)
```
pip install pyelftools
```

-----------------------------
## Usage :

🚀 How to Run

1️⃣ Running the Exploit on PS5/PS4

First, ensure you have a Wi-Fi card that supports Monitor Mode.
Then, run the exploit:

sudo python3 exploit.py wlan0 kernel.bin

wlan0 → Your Wi-Fi network interface (check with ifconfig)

kernel.bin → A kernel dump for analysis


If you have already patched the kernel and just want to send the crafted packets:

sudo python3 exploit.py wlan0 kernel.bin --already-patched
