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

1️⃣ Running the Exploit on linux :

First, ensure you have a Wi-Fi card that supports Monitor Mode.


wifi0 → Your Wi-Fi network interface (check with ifconfig)

# 1
```
git clone https://github.com/Dark-life944/PoC-PS5-PS4.git && cd PoC-PS5-PS4 && cd CVE-2022-23088
```
# 2
```
sudo ifconfig wifi0 down && sudo iwconfig wifi0 mode monitor && sudo ifconfig wifi0 up
```
# 3 
```

```
