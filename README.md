## ⚙️ Installation

1. **Clone or download the repository**

   ```bash
   git clone https://github.com/your-username/network-interactive-tool.git
   cd network-interactive-tool
   ```

2. **Install required Python version**
   This project is built with **Python 3.8+**.
   Verify your Python version:

   ```bash
   python3 --version
   ```

3. **Install dependencies**
   The project mostly uses standard libraries (`re`, `sys`, `time`, `socket`, `os`, `signal`), so no external packages are needed.

   However, you need to make sure your **custom modules** are available:

   * `tcpscan` → for TCP port scanning
   * `psping` → for TCP "ping" connectivity check
   * `urlReqHeader` → for public IP detection & HTTP header fetching

   Place these files (`tcpscan.py`, `psping.py`, `urlReqHeader.py`) inside the project directory (same folder as your main script).
   Your structure should look like:

   ```
   network-interactive-tool/
   ├── main.py
   ├── tcpscan.py
   ├── psping.py
   ├── urlReqHeader.py
   ```

   > If you prefer, you can also install them as proper Python packages using `pip install -e .` after creating a `setup.py`.

4. **Run the program**

   ```bash
   python3 main.py
   ```

---

## ▶️ Usage Examples

* **Check your public IP**

  ```
  You: what is my ip
  IP: 203.0.113.25
  ```

* **Scan single or multiple ports**

  ```
  You: scan port 80,443,20 of google.com server
  ✅ Port 80 is OPEN
  ❌ Port 20 is CLOSED
  ```

* **Scan a port range**

  ```
  You: scan port range 80-100 of google.com server
  ```

* **TCP ping**

  ```
  You: connect port 443 to google.com server
  ✅ Connected to google.com:443 ...
  ```

* **Fetch HTTP headers (in development)**

  ```
  You: https://example.com
  [Response headers...]
  ```

* **Exit gracefully**

  ```
  You: bye
  See you again!!!!
  ```
