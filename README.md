# 🧠 remote_function_stomping

💥 **Windows Shellcode Loader** using **RC4 encryption** and **Remote Function Stomping** to inject and execute payloads via native WinAPI.

---

## 🔍 Overview

This project demonstrates a custom shellcode loader written in C for Windows.  
It leverages **RC4 encryption** to protect the payload and performs **Remote Function Stomping** by overwriting a legitimate Windows API function (e.g., `CharToOemA` from `user32.dll`) with shellcode. The payload is then executed using `CreateRemoteThread`.

---

## ⚙️ Key Features

- 🔐 **RC4 Encrypted Shellcode**
- 🧬 **Function Stomping** via `user32.dll!CharToOemA`
- 🚀 **Remote Process Injection**
- 🛠 **WinAPI Only** – no external dependencies
- 🧠 Built for **Red Teaming**, **malware simulation**, and **bypass techniques**

---

## 🖥️ How it works

1. 📦 Load a common DLL (e.g., `user32.dll`)
2. 🧩 Get the address of a known exported function (e.g., `CharToOemA`)
3. 🔓 Decrypt the shellcode using `SystemFunction032` (RC4)
4. ✍️ Overwrite the function in a remote process (e.g., `notepad.exe`)
5. 🧵 Execute it with `CreateRemoteThread`

---

## ⚠️ Disclaimer

> This tool is intended **strictly for educational and research purposes**.  
> Use it responsibly and **do not** deploy it against systems you don’t own or have permission to test.

---

## 📌 Tags

`#redteam` `#winapi` `#malwaredev` `#shellcode` `#functionstomping` `#rc4` `#cprogramming` `#offensivesecurity`

