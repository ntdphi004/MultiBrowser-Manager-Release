# MultiBrowser Manager — Professional Anti-Detect Browser & Automation Engine

<p align="center">
  <img src="https://raw.githubusercontent.com/ntdphi004/MultiBrowser-Manager-Release/main/assets/banner.png" alt="MultiBrowser Manager" width="800" onerror="this.style.display='none'"/>
</p>

<p align="center">
  <b>Next-Generation Anti-Detect Browser Powered by Native C++ Blink-Patched Chromium Core</b><br>
  100% TLS JA3/JA4 Fingerprint Alignment · Bypasses CreepJS, Pixelscan, BrowserLeaks, Cloudflare Turnstile · Ultra-Optimized Performance
</p>

<p align="center">
  <a href="https://github.com/ntdphi004/MultiBrowser-Manager-Release/releases/latest"><img src="https://img.shields.io/github/v/release/ntdphi004/MultiBrowser-Manager-Release?color=blue&label=Latest%20Version" alt="Latest Release"></a>
  <img src="https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20(64--bit)-success" alt="Platform">
  <img src="https://img.shields.io/badge/Engine-Chromium%20Native%20Patched%20C%2B%2B-blueviolet" alt="Chromium Native">
  <img src="https://img.shields.io/badge/Security-Local%20First%20%7C%20Zero%20Telemetry-green" alt="Security">
  <a href="README_VI.md"><img src="https://img.shields.io/badge/Language-Ti%E1%BA%BFng%20Vi%E1%BB%87t-informational" alt="Tiếng Việt"></a>
</p>

> [!NOTE]
> **Looking for Vietnamese documentation?**  
> Vui lòng xem tài liệu hướng dẫn tiếng Việt tại [README_VI.md](README_VI.md).

---

## 🌟 1. Key Advantages of MultiBrowser Manager

Unlike conventional account management tools that rely on JavaScript runtime injection (which are easily detected by modern anti-fraud systems), **MultiBrowser Manager** is re-engineered directly at the Chromium kernel level:

| Technical Feature | MultiBrowser Manager (Native C++) | Conventional Anti-Detect Browsers (JS Injection) |
|---|:---:|:---:|
| **Fingerprint Spoofing Method** | **Native C++ Blink Level** (Directly compiled into the Chromium engine) | Injects JavaScript overrides (`navigator`, `WebGLRenderingContext`) |
| **Advanced Bot Detection Bypass** | **100% Pass Rate** on CreepJS, Pixelscan, Incolumitas, BrowserLeaks | Readily exposes modified prototype descriptors (`toString()`, `getOwnPropertyDescriptor`) |
| **TLS / SSL Fingerprint (JA3 / JA4)** | **100% Match** with genuine Google Chrome network packets | Frequently deviates in Cipher Suites, Extension Orders, or HTTP/2 settings |
| **Resource Consumption (RAM / CPU)** | **Ultra-Lightweight**, runs natively on Windows without virtual machines | Resource-heavy, consumes substantial RAM when running multiple profiles |
| **Data Privacy & Security** | **100% Local-First**: SQLite database, cookies, and tokens stored locally on your machine | Many tools covertly sync sensitive user data to third-party cloud servers |
| **Automation Support** | High-speed Native CDP controller with full Puppeteer / Playwright support | Prone to freezing, lag, or pipe disconnection under high profile concurrency |

### Highlighted Features:

1. **Complete Hardware & Environment Isolation:**
   - **Canvas & WebGL:** Smart noise generation algorithm providing consistent hashing per profile without graphical distortion.
   - **WebGPU & Hardware Concurrency:** Authentic emulation of CPU core counts, RAM capacity, GPU Vendor, and Renderer (NVIDIA, AMD, Intel, Apple Silicon).
   - **AudioContext & SpeechSynthesis:** Realistic audio sample frequencies and OS-specific speech synthesis voice lists.
   - **Font Fingerprinting:** Whitelisted font sets aligned with the target operating system (Windows, macOS, or Linux).
   - **WebRTC & Geolocation:** Strict WebRTC leak protection (zero real IP leaks), with automatic synchronization of Timezone (`Intl.DateTimeFormat`), Accept-Language headers, and geolocation coordinates matching your Proxy IP.

2. **Smart Proxy Management:**
   - Full protocol support: **HTTP, HTTPS, SOCKS5** (with or without username/password authentication).
   - Real-time proxy health checks (IP address, country, ping latency) before launching any browser profile.

3. **Convenient Account & Cookie Management:**
   - Import and Export cookies in JSON and Netscape formats.
   - Automated AES-256 encryption for stored passwords and tokens.

---

## 🚀 2. Download & Installation Guide

### System Requirements
- **Operating System:** Windows 10 / Windows 11 (64-bit) *(Linux / macOS supported via Docker / source build)*.
- **RAM:** Minimum 4 GB (8 GB or more recommended for concurrent profiles).
- **Storage:** Minimum 1 GB available disk space.

### Method 1: Fresh Full Package Install (For New Users)
1. Visit the official release page: 👉 **[Download Latest Release Here](https://github.com/ntdphi004/MultiBrowser-Manager-Release/releases/latest)**
2. Download the installation archive (e.g., `MultiBrowser-Manager-vX.Y.Z-customer-full.zip`).
3. Extract the `.zip` archive into any folder (e.g., `D:\MultiBrowser-Manager`).
4. Double-click **`MultiBrowser.exe`** (or `CAI_TAT_CA.bat` to automatically set up the entire environment).
5. The application will start and automatically open the management dashboard in your browser at: `http://127.0.0.1:8080`.

### Method 2: 1-Click Fast Update (For Existing Users)
- **Method A (Via Web Dashboard):** When a new version is available, an update banner appears on the Dashboard -> Click **"Update Now"** -> **"Restart & Apply"**.
- **Method B (Windows System Tray):** Right-click the MultiBrowser icon in the Windows notification area -> Select **"Check for updates..."**.
- **Method C (1-Click Batch File):** Double-click **`CAP_NHAT.bat`** (or `UPDATE.bat`) in the application root folder. The script downloads a lightweight patch (~15-25 MB), creates a backup, and updates within seconds **without losing any profile data or settings**.

### Method 3: Docker Deployment (Self-Hosted Server / Linux)
```bash
git clone https://github.com/ntdphi004/MultiBrowser-Manager.git
cd MultiBrowser-Manager
docker compose up --build -d
```
Access the dashboard at `http://localhost:8080`.

---

## 📖 3. Basic Usage Guide

### Step 1: Create a New Browser Profile
1. Click the **"+ New Profile"** button.
2. Enter a profile name (e.g., `Facebook_Acc_01`, `Amazon_Store_02`).
3. Select the emulated Operating System (Windows / macOS / Linux) and browser version.
4. Fingerprint Configuration: The system automatically generates an optimal, realistic randomized fingerprint. You can customize Canvas, WebGL, or Audio settings if advanced tweaking is needed.

### Step 2: Assign a Proxy to the Profile
1. In the **Proxy Configuration** section, select your proxy protocol (HTTP / HTTPS / SOCKS5).
2. Enter the proxy string: `IP:PORT` or `IP:PORT:USERNAME:PASSWORD`.
3. Click **"Check Proxy"** to verify that the IP is active and the country is correctly detected.

### Step 3: Launch the Profile
1. Click **"Launch"** (Open Profile).
2. The anti-detect browser will open with the configured fingerprint parameters and proxy routing.
3. Verify profile integrity and stealth on platforms such as [browserleaks.com](https://browserleaks.com), [creepjs](https://abrahamjuliot.github.io/creepjs/), [pixelscan.net](https://pixelscan.net), or [iphey.com](https://iphey.com).

---

## 🤖 4. Automation & Developer API (CDP / Playwright / Puppeteer)

MultiBrowser Manager provides full Chrome DevTools Protocol (CDP) connectivity and a REST API:

### Playwright Python Example
```python
import asyncio
import httpx
from playwright.async_api import async_playwright

MB_BASE_URL = "http://127.0.0.1:8080"
PROFILE_ID = "your-profile-id"

async def main():
    # 1. Launch profile via MultiBrowser REST API
    async with httpx.AsyncClient() as client:
        res = await client.post(f"{MB_BASE_URL}/api/profiles/{PROFILE_ID}/launch")
        cdp_endpoint = res.json()["cdp_endpoint"]

    # 2. Connect Playwright over CDP
    async with async_playwright() as p:
        browser = await p.chromium.connect_over_cdp(cdp_endpoint)
        context = browser.contexts[0]
        page = context.pages[0] if context.pages else await context.new_page()

        # 3. Perform automation
        await page.goto("https://pixelscan.net")
        print("Page Title:", await page.title())
        await browser.close()

if __name__ == "__main__":
    asyncio.run(main())
```

### REST API Endpoints
- **Create Profile:** `POST http://127.0.0.1:8080/api/profiles`
- **Launch Profile:** `POST http://127.0.0.1:8080/api/profiles/{id}/launch`
- **Stop Profile:** `POST http://127.0.0.1:8080/api/profiles/{id}/stop`
- **API Documentation:** Visit `http://127.0.0.1:8080/docs` (Swagger UI).

---

## 🛠️ 5. Frequently Asked Questions & Troubleshooting

### ❓ Issue 1: Windows Defender / Antivirus warns or blocks `.exe` / `.bat` files
- **Cause:** MultiBrowser Manager is compiled with AOT Native C++ and does not yet use an expensive commercial Microsoft Code Signing Certificate, which may prompt Windows SmartScreen (*"Windows protected your PC"*).
- **Resolution:**
  1. When the blue Windows SmartScreen popup appears, click **"More info"** -> Click **"Run anyway"**.
  2. To avoid false-positive scans during operation, add the MultiBrowser Manager installation folder to your Antivirus / Windows Security **Exclusion list**.

### ❓ Issue 2: Proxy connection failure or page load timeout
- **Cause:** 
  - Proxy is inactive, incorrect port, or wrong username/password.
  - Rotating proxies may take several seconds to assign a new active IP.
- **Resolution:**
  1. Verify the format: Ensure there are no leading or trailing whitespace characters.
  2. Try switching between HTTP and SOCKS5 protocols.
  3. Click **"Check Proxy"** in the profile settings to inspect the detailed status code.

### ❓ Issue 3: Cannot open dashboard at `http://127.0.0.1:8080` (Port 8080 Conflict)
- **Cause:** Port 8080 is already occupied by another application (e.g., local server, accounting software, Docker).
- **Resolution:**
  1. Open the `.env` file in the installation root directory with Notepad.
  2. Locate the line `MB_PORT=8080` and change it to another port (e.g., `MB_PORT=8090` or `MB_PORT=8888`).
  3. Restart `MultiBrowser.exe` and access the new port in your browser.

### ❓ Issue 4: "File is locked by another process" during update
- **Cause:** A previous browser instance or `MultiBrowser.exe` process is still running in the background when attempting to overwrite files.
- **Resolution:**
  1. Double-click **`CAP_NHAT.bat`**.
  2. The update script automatically finds and gracefully terminates associated processes before extracting the patch.
  3. If the issue persists, open *Task Manager* (Ctrl+Shift+Esc), terminate any remaining `MultiBrowser.exe` or `chrome.exe` processes, and rerun `CAP_NHAT.bat`.

### ❓ Issue 5: How to back up all Profile data?
- All account profiles, browser cookies, history, and local settings are stored in:
  `%USERPROFILE%\.multibrowser-manager\` (typically `C:\Users\<Your_Username>\.multibrowser-manager\`).
- To back up or transfer your data to another machine, simply copy and safely archive this directory.

---

## 🔒 6. Security & Privacy Policy

- **Zero Telemetry:** The application collects zero browsing history, cookies, credentials, or personal telemetry.
- **Local Storage:** SQLite databases and encryption keys reside 100% locally on your machine.
- **Safe Updates:** Update patches contain only pre-compiled binaries and frontend UI assets, verified via **SHA-256** checksums before being applied.

---

## 📞 7. Support & Community

If you encounter any difficulties during installation or operation, feel free to reach out:
- **GitHub Issues:** [Submit Bug Report / Feature Request](https://github.com/ntdphi004/MultiBrowser-Manager-Release/issues)
- **Telegram Bot:** [@MultiBrowser_Bot](https://t.me/MultiBrowser_Bot)

---

<p align="center">
  <i>MultiBrowser Manager — The ultimate solution for digital identity protection and secure multi-account operations.</i>
</p>
