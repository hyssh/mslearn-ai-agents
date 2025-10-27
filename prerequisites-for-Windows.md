# 🧰 Prerequisites (Windows 11)

This guide provides step-by-step instructions to set up your Windows 11 environment for building AI agents on Azure.

---

## 0. Install Required Tools

Ensure the following tools are installed on your machine:

- **Python 3.12**  
  Download: https://www.python.org/downloads/windows  
  OR  
  Download 64-bit: https://www.python.org/ftp/python/3.12.6/python-3.12.6-amd64.exe

- **Git**  
  Download: https://git-scm.com/downloads

- **Azure CLI**  
  Download: https://learn.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest

- **Visual Studio Code (VS Code)**  
  Download: https://code.visualstudio.com/Download

---

## 1. Clone the Repository

Open a terminal and run:

```bash
git clone https://github.com/ms-mfg-community/mslearn-ai-agents.git
cd mslearn-ai-agents
```

Open the project from VS Code or run the following command in the `mslearn-ai-agents` folder:

```bash
code .
```

This repository contains instructions and assets for building agents on Azure.

---

## 2. Check Python Installation

Verify Python is installed correctly:

```bash
python --version
```

---

## 3. Create Virtual Environment

Navigate to your project folder (`mslearn-ai-agents`) and run:

```bash
python -m venv .venv
```

---

## 4. Activate Virtual Environment

#### On Windows (Command Prompt):
```cmd
.venv\Scripts\activate.bat
```

#### On Windows (PowerShell):
```powershell
.venv\Scripts\Activate.ps1
```

> **Note:** You'll know it's active when your terminal prompt shows `(.venv)`.

> **PowerShell Execution Policy:** If you get an error about execution policies, run:
> ```powershell
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

---

## 5. Install Required Python Packages

```bash
pip install azure-ai-projects
pip install azure-identity
```

---

## 6. Authenticate with Azure

Use the Azure CLI to sign in to your Azure subscription:

```bash
az login
```

---

## 7. Set Environment Variables

To run the agent setup code, you’ll need:

- **Project Endpoint**: Found in the [Azure AI Foundry](https://ai.azure.com) portal under  
  `Overview` section.

- **Model Deployment Name**: Found in  
  `Models + Endpoints` in the left navigation menu of the Azure AI Foundry portal.

Set these as environment variables:

#### On Windows (Command Prompt):
```cmd
set PROJECT_ENDPOINT=https://<your-project-endpoint>
set MODEL_DEPLOYMENT_NAME=<your-model-deployment-name>
```

#### On Windows (PowerShell):
```powershell
$env:PROJECT_ENDPOINT="https://<your-project-endpoint>"
$env:MODEL_DEPLOYMENT_NAME="<your-model-deployment-name>"
```

> **Note:** Replace `<your-project-endpoint>` and `<your-model-deployment-name>` with your actual values from Azure AI Foundry.

---

## 8. Run Agent Setup Test

Now you're ready to run the agent setup code:
```bash
python Labfiles/ai_foundry_access_test.py
```

**Expected Result:**  
![dev_con_terminal](Instructions/Media/dev_container_run_test_code.png)

---

## ✅ Verification Checklist

- [ ] Python 3.12 installed
- [ ] Git installed
- [ ] Azure CLI installed
- [ ] VS Code installed
- [ ] Repository cloned
- [ ] Virtual environment created and activated
- [ ] Python packages installed
- [ ] Azure CLI authenticated
- [ ] Environment variables set
- [ ] Test script runs successfully

