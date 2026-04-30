---
title: Download and install .Net Desktop Runtime for AI Desktop Actions
description: Reduce setup time and prevent installation errors by downloading and installing .Net Desktop Runtime following the instructions.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-02-03"
reading_time_minutes: 1
breadcrumb: [Configure, AI Desktop Actions, Enable AI experiences]
---

# Download and install .Net Desktop Runtime for AI Desktop Actions

Reduce setup time and prevent installation errors by downloading and installing .Net Desktop Runtime following the instructions.

## Before you begin

Ensure that you have installed the AI Desktop Actions MSI. For more information, see [Download AI Desktop Actions installer](download-agentic-desktop-installer.md).

Role required: admin

## About this task

The AI Desktop Actions installer guides you through installation of .NET Desktop Runtime during the setup.

## Procedure

1.  Copy the following script to your clipboard.

    ```
    Write-Host "--- Initializing Agentic Environment Setup ---" -ForegroundColor Cyan
    $ErrorActionPreference = "Stop"
    
    $downloadUrl = "https://dot.net/v1/dotnet-install.ps1"
    $workingDir = $PSScriptRoot
    $scriptPath = Join-Path $workingDir "dotnet-install.ps1"
    
    try {
        Write-Host "[1/3] Downloading official Microsoft installer..." -ForegroundColor Yellow
        Invoke-WebRequest -Uri $downloadUrl -OutFile $scriptPath
    
        Write-Host "[2/3] Installing .NET 9.0.10..." -ForegroundColor Yellow
        Set-Location $workingDir
    
        & .\dotnet-install.ps1 `
            -Architecture x64 `
            -InstallDir "C:\Program Files\dotnet\" `
            -Runtime windowsdesktop `
            -Version 9.0.10
    
        & .\dotnet-install.ps1 `
            -Architecture x64 `
            -InstallDir "C:\Program Files\dotnet\" `
            -Runtime dotnet `
            -Version 9.0.10
    
        Write-Host ""
        Write-Host "--- SUCCESS: System is ready for Agentic Desktop ---" -ForegroundColor Green
    }
    catch {
        Write-Host ""
        Write-Host "--- ERROR: Installation failed ---" -ForegroundColor Red
        Write-Host $_.Exception.Message -ForegroundColor Red
    }
    
    Write-Host ""
    Write-Host "Press any key to exit..."
    $null = $Host.UI.RawUI.ReadKey("NoEcho,IncludeKeyDown")
     
    ```

2.  Paste the script in any text editor.

3.  Save the file with a `.ps1` extension.

    1.  Select **File** &gt; **Save As**.

    2.  In the **File name** field, enter a name and save the file with a `.ps1` extension.

        Example: `myscript.ps1`

    3.  Set **Save as type** to **All Files \(.\)**.

    4.  Choose a location such as Documents or Desktop.

    5.  Select **Save**.

4.  Run the script in Windows PowerShell.

    1.  Select **Start**.

    2.  Search for **Windows PowerShell**.

    3.  Select **Run as administrator**.

    4.  Use the `cd` command to move to the folder where you saved the script.

        Example:

        ```
        cd C:\Users\YourName\Documents
        ```

    5.  Run the script by entering the following command.

        Example:

        ```
        .\myscript.ps1
        ```


## Result

.NET Desktop Runtime is downloaded and installed on your system.

## What to do next

Use AI Desktop Actions to design desktop actions. For more information, see [Desktop actions in AI Desktop Actions](../concept/desktop-actions-designer-workspace-ad.md).

