This Ansible playbook will perform the following tasks:


1. Update the apt cache
2. Install required system packages
3. Add Kubernetes GPG key and repository
4. Install Kubernetes packages (kubelet, kubeadm, and kubectl)
5. Prevent Kubernetes packages from being automatically updated
6. Restart and enable Docker service
7. Enable and start kubelet service

To use this playbook:

1. Save it to a file, for example, kubernetes_install.yml
2. Make sure you have Ansible installed on your control node
3. Update your Ansible inventory file with the target Ubuntu 22.04 servers
4. Run the playbook with the command: ansible-playbook -i your_inventory_file kubernetes_install.yml


Note that this playbook installs the necessary components but does not configure a Kubernetes cluster. After running this playbook, you'll need to initialize your Kubernetes cluster using kubeadm init on the master node and join worker nodes to the cluster.
