## markdown file on system installation steps
(1) create a github account using the link......https://github.com/signup

(2) install choco package manager that allows you install other tools using the link........ https://chocolatey.org/install

open powershell as admin and run the command........Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

(3) install windows terminal using this link....https://apps.microsoft.com/home?hl=en-US&gl=US.

then open store and search for windows terminal, click on get

(4) install vs code using this link......https://code.visualstudio.com/download... and add all necessary extensions

(5) create a workspace folder on your local machine.

(6) To install ssh, use the commands below to install ssh client and server respectively

Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0

(7) to setup the key pairs

ssh-keygen -t ed25519..... it generates the public and private keys for you

(8) To setup ssh agent. run the command

Get-Service ssh-agent

Start-Service ssh-agent    
ssh-add ~\.ssh\id_ed25519  
ssh-add -l ...... The key is shown in the diagram attached

(9) then copy public key over to github

(10) Then lastly, crweate a repo in github, clone the repo to the client machine and i created the markdown file named system-install-course listing out steps to installing the tools
