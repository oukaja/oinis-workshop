## Install Chocolatey CLI with PowerShell.exe

With PowerShell, there is an additional step. You must ensure `Get-ExecutionPolicy` is not `Restricted`. We suggest using `Bypass` to bypass the policy to get things installed or `AllSigned` for quite a bit more security.

Run `Get-ExecutionPolicy`. If it returns `Restricted`, then run `Set-ExecutionPolicy AllSigned` or `Set-ExecutionPolicy Bypass -Scope Process`.

Now run the following command:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

## Install VirtualBox with choco
```powershell
choco install virtualbox

## Install Minikube with choco
```powershell
choco install minikube
