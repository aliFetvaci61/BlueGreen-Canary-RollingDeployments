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

## Canary Deployment
Unlike the normal deployment, Canary Deployment follows the strategy that releases the feature or new versions into the target servers incrementally to the subset of users. This deployment will happen in incremental phases. And the subset of users will act as the Testers/validators who will verify the release.

![image](https://user-images.githubusercontent.com/16122994/150844505-2c938393-5e35-4de7-9e51-3701cc2456e2.png)

The above image assumes the application is in Version V1.0 and the new release or the deployment deploys V2.0. This deployment happens in four phases. In phase 1, the Release will happen in 25% of the nodes in the cluster and that will be tested by the Set of users. Then, in Phase 2, 50% of nodes will receive the V2.0 and Phase 3- 75%, and finally in phase 4- 100% of nodes will receive the new version. This is how Canary Deployment works.

### Pros of Canary Deployment
#### Canary Deployment allows real users or acting real users of the Production environment to test the New Features.
#### No Downtime while updating or releasing the new feature.
#### Cheaper in terms of Infrastructural resources.
#### Rollback to the older version made it very easy.
### Cons of Canary Deployment
#### When limiting the number of nodes for the end-user might impact the overall performance.
#### Canary Deployment Mechanism is complex.
#### User verification and testing may take time and make the process slower.
#### The monitoring and feedback system for the infrastructure should be modified to monitor the canary deployment separately.


## Rolling Deployment.
Rolling Deployment is like Canary Deployment. But the difference is, in the rolling deployment, we update the newer version into a single/defended number of instances.

![image](https://user-images.githubusercontent.com/16122994/150844830-2f5b4155-76cb-493a-acb4-bd3596e37e9e.png)


As mentioned in the above image, Rolling Deployment releases the update in one by one process. Which means, the Deployment is happening in the first two instance and then, incrementally next two instance vice versa. So, testing will be carried out in each batch of release.

### Pros of Rolling Deployment
#### The rollback process is very easy as we are deploying an Instance by instance.
#### Easy and Simple to implement the Deployment mechanism
#### Cost-effective as the effort and infrastructure utilization is highly less.
### Cons of Rolling Deployment
#### Since the Number of release batches is increased, the Testing and Verification process is very lengthy and slow.
#### We need to make sure of the Artifact availability till the deployment process finishes with Nth Bach.
#### How to choose a Deployment Strategies.
#### After analyzing the working mechanism of the above deployment strategies, Canary Deployment will be suitable for mission-critical Web applications. Blue-Green Deployment can be done for the customer base where they have less business impact. Rolling deployment is useful for the cluster which is having a smaller number of nodes.

## Conclusion
In this article, we discussed some strategies for Continuous Delivery. Especially, Canary vs Blue-Green vs Rolling Deployment with Pros and Cons of each Deployment strategies. 

