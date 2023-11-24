# deploy-app-eks
Deploy a sample node app to eks with github actions

# Create EKS cluster using (teraform/CFT/EKS CTL)

1. In this case we will be deploying the EKS cluster via EKSCTL using the command mentioned below:-

eksctl create cluster --name test-app --region us-east-2 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2

2. On ECR create repository -> node-app

3. Github Repo with app code (server.js, package.json, package-lock.json), github workflow(github-actions-ci.yml), k8 deployment config(service.yaml, deployment.yaml)

4. set github repository secrets for AWS access/secret key

5. commit code to github to trigger your pipeline

6. In order to check the deployment RUN
kubectl get nodes
kubectl get service (corresponding to the Load Balancer is the endpoint to reach the applications)


