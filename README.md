# Development Environment Setup

A Windows Desired State Configuration (DSC) project using WinGet to automate the setup of a development environment.

## Prerequisites

1. **Windows 10/11** with WinGet installed
2. **Upgrade WinGet** to the latest version: https://github.com/microsoft/winget-cli/releases
3. **PowerShell 5.1+** (Windows PowerShell or PowerShell 7)

## Installation

Open **Windows PowerShell as Administrator** and run:

```powershell
# Install required PowerShell modules
Install-Module Microsoft.WinGet.Client -Scope AllUsers -Force
Install-Module Microsoft.WinGet.DSC -Scope AllUsers -Force
```

## Usage

Apply configurations in order from the `configs/` directory:

```powershell
# 1. Install development tools
dsc config set -f devtools.dsc.config.yaml
```
