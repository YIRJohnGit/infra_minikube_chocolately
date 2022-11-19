# Instalatoin of Chocolatey
- STart the Windows Power as  Administrator
  - Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
  - [choco # Verify the Installation](https://user-images.githubusercontent.com/111234771/202818467-22a26a41-ab84-4e91-8b5b-441c172b4479.png)
    - choco install minikube

# Starting Minikube Master Node using Default Docker Driver and Runtime with Docker
- minikube status # Get the Status of the Minikube Installed
- minikube start # It will download and install Minikube
- kubectl get nodes # Get the List of Running Nodes
- kubectl get pods # Get the list of running PODS
- kubectl get all # will display 

# Working with Multi Nodes (Minikube) (Profile / Cluster) Default Docker Driver and Runtime with Docker
- minikube start -p multinode-demo --nodes 3 # Creating 3 Nodes Cluster name called 'multinode-demo' 1 Master + 2 Worker
- \#If it throws error then use on screen instruction : minikube start -p multinode-demo --nodes 3 --extra-config=kubelet.cgroup-driver=systemd 
- minikube profile list # get list of all the profiles
- ![image](https://user-images.githubusercontent.com/111234771/202845310-8fb236f9-27a0-400c-a12b-3d8f07185dfd.png)
- minikube profile # Get the Current Profile Name
- minikube profile minikube # switch to different profile name, example minikube is the default profile name
- minikube status # Get the Status of the Minikube Installed
- ![image](https://user-images.githubusercontent.com/111234771/202845359-4680966d-3636-41d1-8f11-2ae6da6a081e.png)
- minikube delete -p multinode-demo # Deleting Profile called multinode-demo

# Creating Multiple Clusters using Virtual Machine Driver and Runtime with Docker
- minikube start --vm-driver=virtualbox -p dev # Will Create Virtual Machine Called dev
- minikube start --vm-driver=virtualbox -p test # Will Create Virtual Machine Called test
- minikube start --vm-driver=virtualbox -p prod # Will Create Virtual Machine Called prod
- minikube start --vm-driver=virtualbox -p prod --nodes 3 # Create prodcluster with 3 Nodes 
- minikube profile list # get list of all the profiles
