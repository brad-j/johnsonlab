# johnsonLAB

1. Install k3s
```bash
curl -sfL https://get.k3s.io | sh -
```
2. Copy the kubeconfig file to home directory
```bash
mkdir ~/.kube
sudo cp /etc/rancher/k3s/k3s.yaml $HOME/.kube/config
sudo chown $USER $HOME/.kube/config
sudo chmod 600 $HOME/.kube/config
export KUBECONFIG=$HOME/.kube/config
````

Test
