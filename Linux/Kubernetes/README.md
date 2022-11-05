# Kubernetes

## Bash completion for kubectl with specific alias and kubeconfig

```bash 
# Enable bash completion 
kubectl completion bash | sudo tee /etc/bash_completion.d/kubectl > /dev/null

# Install specific bash completion
sudo su
curl https://raw.githubusercontent.com/cykerway/complete-alias/master/complete_alias > /etc/bash_completion.d/complete_alias

# Open .bashrc and add the below lines

alias kubectlprod='kubectl --kubeconfig /mohammad/snapp/kubeconfig.MohammadDehnavi.config'
complete -F _complete_alias kubectlprod
```