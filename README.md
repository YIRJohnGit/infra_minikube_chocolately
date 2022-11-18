# Instalatoin of Chocolatey
- STart the Windows Power as  Administrator
  - Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
  - [choco # Verify the Installation](https://user-images.githubusercontent.com/111234771/202818467-22a26a41-ab84-4e91-8b5b-441c172b4479.png)
    - choco install minikube
