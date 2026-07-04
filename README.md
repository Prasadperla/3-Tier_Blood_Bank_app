# 3-Tier_Blood_Bank_app
Code and Manifest files for a 3 tier blood bank application

# Install kubectl
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
mv kubectl /usr/local/bin/

# Install kops
curl -Lo kops https://github.com/kubernetes/kops/releases/download/$(curl -s https://api.github.com/repos/kubernetes/kops/releases/latest | grep tag_name | cut -d '"' -f 4)/kops-linux-amd64
chmod +x kops
sudo mv kops /usr/local/bin/kops

# Attach IAM role (EC2_Access) to the EC2 instance 
# export KOPS_STATE_STORE=<s3_bucket_name>
# kops create cluster
