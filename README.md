# BlueGreen-Canary-RollingDeployments

Every organization follows their unique way of deploying the application to the Production. Mostly their concerns are about Deploying the bug free code. In this article, we will discuss the difference and pros and cons of the various Deployment Strategies which are followed by various organizations. Also, from the end of this Canary vs Blue-Green vs Rolling Deployment comparison, you will know which one is most suitable for your Organization.

Before all, let’s see how normal deployment happens.

When you deploy the new version or feature on the target environment. It might get success or fail in terms of Feature functionality, Security, or durability.

![image](https://user-images.githubusercontent.com/16122994/150843484-d40d39da-2dbd-4daf-99a9-edbbdc852627.png)

The Above image shows that the cluster of servers is receiving the new package in the new deployment altogether. In this event, either all the nodes will succeed or fail. Also, we cannot avoid downtime. So, Some of the Standard deployment or release strategies are been followed by the organization. We will discuss what are the major deployment method or strategies are followed by the organization and the pros and cons of the Canary vs Blue-Green vs Rolling Deployment and compare each other.
