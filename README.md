# 🛠️ Shell-Audit

> **Shell-Audit V1.0.0** — A quick system, environment, programming runtime, and security tooling audit utility for Kali Linux and Debian-based systems.

Developed by **DeadmanXXXII** (Blu Corbel).

---

## 🚀 Quick Install (via APT)

You can install `shell-audit` directly using `apt` via this repository hosted on GitHub Pages:

```bash
# 1. Add the APT repository source
echo "deb [trusted=yes] [https://DeadmanXXXII.github.io/shell-audit](https://DeadmanXXXII.github.io/shell-audit) ./" | sudo tee /etc/apt/sources.list.d/shell-audit.list

# 2. Update package lists
sudo apt update

# 3. Install shell-audit
sudo apt install shell-audit
```

💻 Usage
Once installed, simply run:

```
shell-audit
```

📋 Features & What it Audits
System Information: OS version, Kernel info, Hostname, Current user, Default shell, Architecture, System date.
Hardware & Storage: Memory utilization (free -h), Root disk usage (df -h /), and cache directory summary (.cache, .cargo, .npm, .local, go).
Programming Runtimes: Checks version outputs for Ruby, Gem, Go, Cargo, Rustc, Node.js, GCC, Make, Git, Python, Python3, Pip, and NPM.
Security Tooling Audit: Scans binary paths for 50+ common penetration testing and security assessment tools (e.g., nmap, metasploit, burpsuite, sqlmap, john, hydra, aircrack-ng, wireshark, bloodhound, impacket, etc.).
Ecosystem Tool Managers:
Go: GOBIN pathing, binary list, cache stats, and total binary count.
Python: Active pip list, pipx installed binaries, site-packages pathing, and package totals.
Ruby: Active gem list and gem totals.
Cargo: Rust crate binary listing and cargo home paths.
APT Security Packages: Query count of security-related APT packages installed on the system via dpkg.
Summary Metrics: Execution runtime and totals for installed vs. missing languages, security tools, and package counts.
⚙️ Manual Build (.deb)
If you wish to build the .deb package yourself from source:

bash```
# Clone repository
git clone git@github.com:DeadmanXXXII/shell-audit.git
cd shell-audit

# Build Debian Package
chmod 755 shell-audit_1.0.0-1/DEBIAN
dpkg-deb --build shell-audit_1.0.0-1

# Install Locally
sudo apt install ./shell-audit_1.0.0-1.deb
```

📬 Author & Contact
Developer: DeadmanXXXII aka Blu Corbel
Email: blucorbel35@gmail.com
License: MIT
