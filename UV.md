# UV Module Installation Guide

This guide will walk you through installing the UV module on macOS and Windows, including setting up Python using UV, using a virtual environment, and managing dependencies with `requirements.txt`.

## Prerequisites
- Scoop for Windows
- brew for macOs

---

## Step 1: Install the UV Module

### macOS & Windows
1. Open Terminal (macOS) or Command Prompt (Windows).
2. Install UV using a package manager:
   - **macOS (Homebrew):**
     ```sh
     brew install uv
     ```
     - **Alternatively, use `curl` to download the script and execute it:**
     ```sh
     curl -LsSf https://astral.sh/uv/install.sh | sh
     ```
     - **If your system doesn't have `curl`, use `wget`:**
     ```sh
     wget -qO- https://astral.sh/uv/install.sh | sh
     ```
     - **To request a specific version, include it in the URL:**
     ```sh
     curl -LsSf https://astral.sh/uv/0.5.25/install.sh | sh
     ```
    
   - **Windows (Scoop):**
     ```sh
     scoop install uv
     ```
     - **Use irm to download the script and execute it with iex:**
     
     ```sh
     powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
     ```
     - **To request a specific version, include it in the URL:**
     ```sh
     powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/0.5.25/install.ps1 | iex"
     ```
     
3. Verify the installation:
   ```sh
   uv --version
   ```

---

## Step 2: Install Python using UV

Once UV is installed, use it to install Python:
```sh
uv venv venv
```
This command will create a virtual environment with Python installed.

Activate the virtual environment:
- **macOS/Linux:**
  ```sh
  source venv/bin/activate
  ```
- **Windows:**
  ```sh
  venv\Scripts\activate
  ```

---

## Step 3: Managing Dependencies with `requirements.txt`

### Creating `requirements.txt`
To freeze the installed packages and save them in `requirements.txt`:
```sh
pip freeze > requirements.txt
```

### Installing from `requirements.txt`
To install dependencies from an existing `requirements.txt`:
```sh
pip install -r requirements.txt
```

---

## Step 4: Deactivating the Virtual Environment
To exit the virtual environment, simply run:
```sh
deactivate
```

---

## Step 5: Uninstalling the UV Module
To remove the UV module:
```sh
pip uninstall uv
```

---
## Additional Useful Commands

### Check Python installation details
```sh
python -m site
```

### Upgrade pip inside the virtual environment
```sh
uv pip install --upgrade pip
```

### Remove all installed packages
```sh
uv pip freeze | xargs uv pip uninstall -y
```

### Show the path of the virtual environment
```sh
which python
```
(For Windows, use `where python` instead.)

---

## Troubleshooting
- If activation fails on Windows, try running Command Prompt as Administrator.
- If `uv` is not found, make sure it is installed in the correct path.

---
