# deploy-app-eks
Deploy a sample node app to eks with github actions

# Create EKS cluster using (teraform/CFT/EKS CTL)
In this case we will be deploying the EKS cluster via EKSCTL using the command mentioned below:-

eksctl create cluster --name test-app --region us-east-2 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2