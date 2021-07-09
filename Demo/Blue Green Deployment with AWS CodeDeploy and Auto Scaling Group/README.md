# Blue/Green Deployment with AWS CodeDeploy and Amazon EC2 Auto Scaling

Demo Github Repo Link ⇒ [https://github.com/josephphyo/aws-codedeploy-demo](https://github.com/josephphyo/aws-codedeploy-demo)

## System Design

![Blue%20Green%20Deployment%20with%20AWS%20CodeDeploy%20and%20Amaz%202708cd1606fc412388b595fad0bb16fe/Blue_Green_Deployment_with_AWS_CodeDeploy_and_ASG.png](Blue%20Green%20Deployment%20with%20AWS%20CodeDeploy%20and%20Amaz%202708cd1606fc412388b595fad0bb16fe/Blue_Green_Deployment_with_AWS_CodeDeploy_and_ASG.png)

## **Requirements**

1. AWS Account 
2. AWS CodeDeploy 
3. Amazon EC2 Auto Scaling
4. AWS Application Load Balancer (ALB) 

## Steps (Manual)

1. Create IAM Service Role for EC2 (EC2CodeDeploy_Role)
2. Create Application LoadBalancer
3. Create AutoScaling Group 
    1. Create Launch Configuration (Attached with IAM Role & codedeploy agent install userdata)
    2. Create AutoScaling Group (With existing loadbalancer)
4. Create CodeDeploy Application 
    1. Create IAM Service Role For Code Deploy (CodeDeployService_Role)
    2. Choose Blue/Green Deployment with automatically copy ASG Group.
    3. Create Deployment with Source Github Repo.
    4. Go Deploy!!
5. Configure/Create CodePipeline for Automatically deploy and trigger.

![Blue%20Green%20Deployment%20with%20AWS%20CodeDeploy%20and%20Amaz%202708cd1606fc412388b595fad0bb16fe/Screen_Shot_2021-07-08_at_5.18.35_PM.png](Blue%20Green%20Deployment%20with%20AWS%20CodeDeploy%20and%20Amaz%202708cd1606fc412388b595fad0bb16fe/Screen_Shot_2021-07-08_at_5.18.35_PM.png)

---