# PostgreSQL Installation Guide for Windows

This guide provides step-by-step instructions to install PostgreSQL on a Windows system.

---

## Prerequisites
- A Windows PC with administrative privileges.
- Internet connection to download the installer.

---

## Step 1: Download PostgreSQL Installer
1. Visit the official PostgreSQL download page:  
   [https://www.postgresql.org/download/windows/](https://www.postgresql.org/download/windows/)
2. Download the installer for the latest version of PostgreSQL.

---

## Step 2: Run the Installer
1. Locate the downloaded `.exe` file (e.g., `postgresql-15.x-windows-x64.exe`).
2. Double-click the file to launch the installer.
3. Allow permissions if prompted by User Account Control (UAC).

---

## Step 3: Installation Steps
1. **Choose Installation Directory:**  
   Default: `C:\Program Files\PostgreSQL\<version>`  
   (You can change this if needed.)
   
2. **Select Components:**  
   Leave all options selected:  
   - PostgreSQL Server  
   - pgAdmin 4  
   - Command Line Tools  
   - Stack Builder (optional)

3. **Set a Password for `postgres`:**  
   During the installation, set a password for the default PostgreSQL superuser (`postgres`).  
   **Remember this password for later use.**

4. **Choose a Port Number:**  
   Default: `5432`. Leave as is unless it conflicts with another application.

5. **Advanced Options (Optional):**  
   Use the default locale settings unless you have specific requirements.

6. **Start Installation:**  
   Click **Next** to install PostgreSQL. This may take a few minutes.

---

## Step 4: Verify Installation
1. **Check PostgreSQL Service:**
   - Press `Win + R`, type `services.msc`, and press Enter.
   - Locate the `postgresql-x64-<version>` service and ensure it is **Running**.

2. **Open pgAdmin 4:**
   - Launch pgAdmin 4 from the Start menu.
   - Connect to the PostgreSQL server:
     - Right-click the server and select **Connect Server**.
     - Enter the password set during installation.

---

## Step 5: Use PostgreSQL from the Command Line
1. Open the Command Prompt (`cmd`).
2. Navigate to the PostgreSQL `bin` directory (if not in PATH):
   ```cmd
   cd "C:\Program Files\PostgreSQL\<version>\bin"
