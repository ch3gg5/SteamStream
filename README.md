# SteamStream

**Elevate your couch experience!** SteamStream is a single, convenient website that aggregates links to all your favorite streaming services (Netflix, YouTube, Hulu, Disney+, Prime Video, HBO Max, etc.).

Instead of adding *each* service individually as a separate "Non-Steam Game", you only need to add **SteamStream once**. From there, you can access all your services directly within Steam's Big Picture mode.

**Live Demo/Website:** [ch3gg5.github.io/SteamStream/](https://ch3gg5.github.io/SteamStream/)

## 🧰 How to Add SteamStream to Steam Big Picture Mode

These instructions guide you through adding the *SteamStream website* as a single "Non-Steam Game". This one entry gives you access to all linked services via the SteamStream interface.

### 🪟 Windows

#### 1. Add SteamStream as a Non-Steam Game

1.  Open **Steam**.
2.  Navigate to your **Library**.
3.  Click **Games** at the top left, then select **Add a Non-Steam Game**.
4.  Click **Browse...**.
5.  Locate and select your preferred browser's executable:
    *   **Chrome:** `C:\Program Files\Google\Chrome\Application\chrome.exe`
    *   **Firefox:** `C:\Program Files\Mozilla Firefox\firefox.exe`
    *   **Edge:** `C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe`

#### 2. Configure Launch Options

1.  In the **Add a Non-Steam Game** window, select the browser you just added.
2.  Click **Properties** (or right-click and select Properties).
3.  In the **Launch Options** field, enter one of the following commands to launch SteamStream in fullscreen mode:

    *   **Fullscreen Kiosk Mode (Recommended):**
        ```
        --kiosk "https://ch3gg5.github.io/SteamStream/"
        ```
    *   **Alternative Fullscreen:**
        ```
        --start-fullscreen "https://ch3gg5.github.io/SteamStream/"
        ```

4.  (Optional) Add browser-specific flags for a cleaner experience:
    *   For Chrome/Edge: `--disable-infobars --no-first-run`
    *   *Example for Chrome:*
        ```
        "C:\Program Files\Google\Chrome\Application\chrome.exe" --kiosk "https://ch3gg5.github.io/SteamStream/" --disable-infobars --no-first-run
        ```

### 🐧 Linux

#### 1. Add SteamStream as a Non-Steam Game

1.  Open **Steam**.
2.  Navigate to your **Library**.
3.  Click **Games** at the top left, then select **Add a Non-Steam Game**.
4.  Click **Browse...**.
5.  Navigate to your preferred browser's executable:
    *   **Chrome:** `/usr/bin/google-chrome` or `/usr/bin/google-chrome-stable`
    *   **Chromium:** `/usr/bin/chromium` or `/usr/bin/chromium-browser`
    *   **Firefox:** `/usr/bin/firefox`
    *   **Brave:** `/usr/bin/brave-browser`

#### 2. Configure Launch Options

1.  In the **Add a Non-Steam Game** window, select the browser you just added.
2.  Click **Properties**.
3.  In the **Launch Options** field, enter the command for your browser to launch SteamStream in fullscreen mode:

    *   **Chrome/Chromium/Brave:**
        ```
        --kiosk "https://ch3gg5.github.io/SteamStream/"
        ```
    *   **Firefox:**
        ```
        --kiosk "https://ch3gg5.github.io/SteamStream/"
        ```

4.  (Optional) Add flags for better compatibility:
    *   For Chrome/Chromium: `--disable-gpu-sandbox`
    *   *Example for Firefox:*
        ```
        /usr/bin/firefox --kiosk "https://ch3gg5.github.io/SteamStream/"
        ```

### 💡 Tips & Tricks

#### 🔧 Linux

*   **Find Browser Paths:** Use the terminal to locate your browser if the path isn't standard:
    ```bash
    which google-chrome firefox chromium brave-browser
    # Or check common directories:
    ls /usr/bin/*chrome* /usr/bin/firefox*
    ```
*   **Controller Support:** Enhance controller navigation by setting up custom Steam Input configurations for your browser.
*   **GPU Issues:** If you encounter graphical glitches, try adding `--disable-gpu` or `--disable-gpu-sandbox`.

#### 🪟 Windows

*   **Clean UI:** Add `--disable-infobars` and `--no-first-run` to minimize browser pop-ups.
*   **Edge Quirks:** Sometimes adding `--no-startup-window` helps Edge launch correctly in kiosk mode.

### 📋 Example Configurations

*   **Windows - Chrome - SteamStream:**
    ```
    "C:\Program Files\Google\Chrome\Application\chrome.exe" --kiosk "https://ch3gg5.github.io/SteamStream/" --disable-infobars --no-first-run
    ```
*   **Linux - Firefox - SteamStream:**
    ```
    /usr/bin/firefox --kiosk "https://ch3gg5.github.io/SteamStream/"
    ```
*   **Linux - Chrome - SteamStream:**
    ```
    /usr/bin/google-chrome-stable --kiosk "https://ch3gg5.github.io/SteamStream/" --disable-gpu-sandbox
    ```
