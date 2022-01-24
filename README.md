# BlueGreen-Canary-RollingDeployments

Every organization follows their unique way of deploying the application to the Production. Mostly their concerns are about Deploying the bug free code. In this article, we will discuss the difference and pros and cons of the various Deployment Strategies which are followed by various organizations. Also, from the end of this Canary vs Blue-Green vs Rolling Deployment comparison, you will know which one is most suitable for your Organization.

Before all, let’s see how normal deployment happens.

When you deploy the new version or feature on the target environment. It might get success or fail in terms of Feature functionality, Security, or durability.

![image](https://user-images.githubusercontent.com/16122994/150843484-d40d39da-2dbd-4daf-99a9-edbbdc852627.png)

The Above image shows that the cluster of servers is receiving the new package in the new deployment altogether. In this event, either all the nodes will succeed or fail. Also, we cannot avoid downtime. So, Some of the Standard deployment or release strategies are been followed by the organization. We will discuss what are the major deployment method or strategies are followed by the organization and the pros and cons of the Blue-Green vs Canary vs Rolling Deployment and compare each other.


## Blue-Green Deployment
We have already discussed about the Blue-Green Deployment in our previous article. However, here is a simple explanation of what is blue-green deployment. Blue and Green mean two identical Production environments. Which mean, we will have two identical production environment. One is Blue or staging environment, and another is Green or Production environment, and among those, one will serve the end-user at a time.

![image](https://user-images.githubusercontent.com/16122994/150843919-cb4179e7-3c90-48b6-b95a-ba3d56c59f34.png)

In the above image, we have two identical clusters and on which Green one will act as Production and Blue one will act as a Staging environment. The new feature will be released on the Green environment first and then after testing succeeds, the Blue environment will be pointed to Public and the Green environment will receive the same Update.

### Pros of Blue-Green Deployment
#### Rollback is easy as we have a whole set of Production environments.
#### This is not Risky in terms of sending the defective feature as we are testing it in the Production alike Staging environment.
#### Deployment is fast and simple compared to other Deployment Strategies.
### Cons of Blue-Green Deployment.
#### Since we have an Identical Two production environment, the cost of the infrastructure is very High.
#### The effort of managing/maintaining the Production is increased.
#### Creating Delivery Pipeline is difficult as we have two environments to maintain.
#### Interactive Reporting or Dashboard is required to Manage the Deployment.
