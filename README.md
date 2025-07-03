# Helm
This repository contains the Helm charts

How to create a page in Github to store the Heml chart?

we need to keep a structure " charts and docs " 

helm package charts/<> --destination docs/
helm repo index docs/ --url https://<your-github-username>.github.io/<repo-name>
git add docs/
git commit -m "Add packaged chart and index.yaml"
git push origin main
