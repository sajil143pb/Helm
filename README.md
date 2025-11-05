# Helm
This repository contains the Helm charts

How to install it?
 helm repo add Helm https://sajil143pb.github.io/Helm/
 helm repo update

How to create a page in Github to store the Heml chart?

we need to keep a structure " charts and docs " 

helm package charts/<> --destination docs/
helm repo index docs/ --url https://<your-github-username>.github.io/<repo-name>
git add docs/
git commit -m "Add packaged chart and index.yaml"
git push origin main


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

