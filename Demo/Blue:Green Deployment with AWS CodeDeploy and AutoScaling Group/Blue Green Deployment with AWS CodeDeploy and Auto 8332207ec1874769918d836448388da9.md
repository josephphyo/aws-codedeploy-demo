# Blue/Green Deployment with AWS CodeDeploy and AutoScaling Group

Demo Repo Link ⇒ [https://github.com/josephphyo/codedeploy-sample](https://github.com/josephphyo/codedeploy-sample)

## System Design

![Blue%20Green%20Deployment%20with%20AWS%20CodeDeploy%20and%20Auto%208332207ec1874769918d836448388da9/Green_Deployment_with_AWS_CodeDeploy_and_ASG.png](Blue%20Green%20Deployment%20with%20AWS%20CodeDeploy%20and%20Auto%208332207ec1874769918d836448388da9/Green_Deployment_with_AWS_CodeDeploy_and_ASG.png)

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

![Blue%20Green%20Deployment%20with%20AWS%20CodeDeploy%20and%20Auto%208332207ec1874769918d836448388da9/Screen_Shot_2021-07-08_at_5.18.35_PM.png](Blue%20Green%20Deployment%20with%20AWS%20CodeDeploy%20and%20Auto%208332207ec1874769918d836448388da9/Screen_Shot_2021-07-08_at_5.18.35_PM.png)

---