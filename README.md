# Helm
This repository contains the Helm charts

# How to install it?

<pre>
 helm repo add Helm https://sajil143pb.github.io/Helm/
 helm repo update
</pre>


🌐 Installing the AWS Load Balancer Controller (Ingress Controller)

# Add the EKS Helm repository and update
helm repo add eks https://aws.github.io/eks-charts
helm repo update

# Install or upgrade the AWS Load Balancer Controller into kube-system
helm upgrade --install aws-load-balancer-controller eks/aws-load-balancer-controller \
  -n kube-system \
  --set clusterName=java-eks \
  --set serviceAccount.create=false \
  --set serviceAccount.name=aws-load-balancer-controller

