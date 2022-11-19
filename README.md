# Instalatoin of Chocolatey
- STart the Windows Power as  Administrator
  - Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
  - [choco # Verify the Installation](https://user-images.githubusercontent.com/111234771/202818467-22a26a41-ab84-4e91-8b5b-441c172b4479.png)
    - choco install minikube

# Starting Minikube Master Node
- minikube status # Get the Status of the Minikube Installed
- minikube start # It will download and install Minikube
- kubectl get nodes # Get the List of Running Nodes
- kubectl get pods # Get the list of running PODS
- kubectl get all # will display 

# Adding Minikube with Multi Nodes
- minikube start --nodes 2 -p multinode-demo # will create additional node with name called 'multinode-demo1'
- \#If it throws error then use on screen instruction : minikube start --nodes 2 -p multinode-demo --extra-config=kubelet.cgroup-driver=systemd 
- 
