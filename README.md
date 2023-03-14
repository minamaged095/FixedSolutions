# FixedSolutions

## Selection of services and infrastructure

1. Single Availability Zone was chosen
2. K8s was hosted on an aws instance running minikube as EKS is not included in free tier and k8s was a requirement so we can not use ECS
3. For a CICD circleci was chosen based on cost criteria alone
4. Route 53 is not included in free tier so Route 53 and cloudfront were not used
5. Since we only have 1 ec2 instance pipeline will not provision any new infrastructure, instead it will deploy new pods in a test namespace and if tests pass will rollout the new deployment and delete pods from the test namespace

