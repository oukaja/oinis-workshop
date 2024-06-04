## Install Chocolatey CLI with PowerShell.exe

With PowerShell, there is an additional step. You must ensure `Get-ExecutionPolicy` is not `Restricted`. We suggest using `Bypass` to bypass the policy to get things installed or `AllSigned` for quite a bit more security.
Run `Get-ExecutionPolicy`. If it returns `Restricted`, then run `Set-ExecutionPolicy AllSigned` or `Set-ExecutionPolicy Bypass -Scope Process`.
### Now run the following command:
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

## Install VirtualBox with choco
```powershell
choco install virtualbox
```

## Install Minikube with choco
```powershell
choco install minikube
```

## Start minikube with virtualbox as driver
### To make virtualbox the default driver:
```powershell
minikube config set driver virtualbox
```
### Start a cluster
#### using the virtualbox driver:
```powershell
minikube start --driver=virtualbox
```
#### using the Hyper-V driver:
```powershell
minikube start --driver=hyperv
```
#### enable the dashboard add-on, and open the proxy in the default web browser.
```powershell
minikube dashboard
```
