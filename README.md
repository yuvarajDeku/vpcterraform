# <H1><u>TERRAFORM </u></H1>


Blue-Green Deployments--> current service state is BLUE DEPLOYMENT,
when the release is to update we create servicesand version in the GREEN, after verifying the GREEN deployment succeed we redirect the blue traffic to Green by 100%

![image](https://user-images.githubusercontent.com/108336310/236104665-7d4b0e42-e728-457d-bc88-95b37885a985.png)


<H2><u>CANARY TEST </u> </H2>
 Canary tests and rolling deployments release the new version of the service to a small group of users, reducing the blast radius in the event of failure.  After the initial canary test, traffic to the green environment is split evenly with the blue environment (50/50). Finally, all traffic is directed to the green environment.rolling-deployment

![image](https://user-images.githubusercontent.com/108336310/236104750-bd48b52a-944e-4005-ab1f-480edde0d62d.png)


AWS's application load balancer (ALB) lets you define rules that route traffic at the application layer.Define an ALB's listeners (rules) and target groups to dynamically route traffic to multiple services. These rules let you run canary tests on and incrementally promote the green environment.
