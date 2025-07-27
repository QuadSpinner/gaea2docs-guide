---
icon: network-wired
---

# Mass Deployment

Gaea can be deployed to a large number of workstations in multiple ways.

{% hint style="danger" %}
When installing to a network drive, it must be installed on a network share hosted as a drive and not a UNC path. Gaea may not work properly on UNC paths.
{% endhint %}

## Unattended Installation

The easiest way to install and activate Gaea is to run the following script / batch file. Replace the path and activation key as required.

The `%ACTIVATION_KEY%` can either be a License Key such as `AAA-BBBB-CCCC-DDDD` or a fully qualified path to a `XYZ1234.lic` offline license file.

```batch
@echo off
SET INSTALLER=Gaea-2.0.3.0.exe
SET ACTIVATION_KEY=your_activation_key_here

:: Install Gaea silently
"%~dp0%INSTALLER%" /VERYSILENT /SUPPRESSMSGBOXES /NORESTART /SP-

:: Wait for the installation to finish
timeout /t 5 /nobreak > NUL

:: Change directory to the installation path (Adjust the path as necessary)
cd "C:\Program Files\QuadSpinner\Gaea 2"

:: Activate Gaea
Gaea.exe -activate %ACTIVATION_KEY%

echo Installation and activation completed.
pause
```

{% hint style="danger" %}
Administrator privileges will be required!
{% endhint %}

## 7-Zip based Deployment

We provide 7z versions of each release so you can create your own installer if needed, or create direct deployments.

Ensure you have 7-zip installed and added to PATH.

```batch
@echo off
SET ARCHIVE=Gaea-2.0.3.0.7z
SET ACTIVATION_KEY=your_activation_key_here
SET INSTALL_PATH=C:\Path\To\Desired\Installation\Location

:: Ensure 7-Zip is installed and available in the PATH
where 7z >nul 2>&1
if %ERRORLEVEL% neq 0 (
    echo 7-Zip not found. Please install it and add to the system PATH.
    exit /b 1
)

:: Create installation directory if it does not exist
if not exist "%INSTALL_PATH%" mkdir "%INSTALL_PATH%"

:: Extract the archive to the installation path
7z x "%~dp0%ARCHIVE%" -o"%INSTALL_PATH%" -y

:: Change directory to the installation path
cd "%INSTALL_PATH%"

:: Activate Gaea
Gaea.exe -activate %ACTIVATION_KEY%

echo Installation and activation completed.
pause
```

### Zip File

Alternatively, if 7-zip is not acceptable in your network environment, you can convert it to a zip file and deploy it with this alternate script:

```batch
@echo off
SET ZIP_FILE=Gaea-2.0.3.0.zip
SET ACTIVATION_KEY=your_activation_key_here
SET INSTALL_PATH=C:\Path\To\Desired\Installation\Location

:: Ensure PowerShell is available
powershell -command "exit" >nul 2>&1
if %ERRORLEVEL% neq 0 (
    echo PowerShell is required but not available.
    exit /b 1
)

:: Create installation directory if it does not exist
if not exist "%INSTALL_PATH%" mkdir "%INSTALL_PATH%"

:: Extract the ZIP file using PowerShell
powershell -command "Expand-Archive -Path '%~dp0%ZIP_FILE%' -DestinationPath '%INSTALL_PATH%' -Force"

:: Change directory to the installation path
cd "%INSTALL_PATH%"

:: Activate Gaea
Gaea.exe -activate %ACTIVATION_KEY%

echo Installation and activation completed.
pause

```
