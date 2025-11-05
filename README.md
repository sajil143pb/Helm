# Helm
This repository contains the Helm charts

# How to install it?

<pre>
 helm repo add Helm https://sajil143pb.github.io/Helm/
 helm repo update
</pre>

# Install or upgrade the AWS Load Balancer Controller into kube-system
<pre>
helm repo add eks https://aws.github.io/eks-charts
helm repo update
</pre>

Installation

<pre>
helm upgrade --install aws-load-balancer-controller eks/aws-load-balancer-controller \
  -n kube-system \
  --set clusterName=java-eks \
  --set serviceAccount.create=false \
  --set serviceAccount.name=aws-load-balancer-controller
</pre>

