# johnsonLAB

## 1. Install k3s
```bash
curl -sfL https://get.k3s.io | sh -
```
## 2. Copy the kubeconfig file to home directory
```bash
mkdir ~/.kube
sudo cp /etc/rancher/k3s/k3s.yaml $HOME/.kube/config
sudo chown $USER $HOME/.kube/config
sudo chmod 600 $HOME/.kube/config
export KUBECONFIG=$HOME/.kube/config
````

## 3. Install Kustomize

## 3.1 Install Kustomize CLI

```bash
yay -S flux-bin
```
## 3.2 Create Github Personal Access Token
` Settings -> Developer settings -> Personal access tokens -> Tokens (classic)`

```bash
export GITHUB_TOKEN=<your-token>
export GITHUB_USER=<your-username>
```

## 3.3 Check Flux Installation

`flux check --pre`

Project structure
```bash
project
├── apps
│   ├── base
│   ├── production 
│   └── staging
├── infrastructure
│   ├── base
│   ├── production 
│   └── staging
└── clusters
    ├── production
    └── staging
