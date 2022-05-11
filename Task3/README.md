# Task3: Design a highly available microservices architecture deployment solution.

If we want to design a highly available microservices we can use:

   1. docker for containerization
   2. kubernetes for orchestration
   3. ansible for server configuration
   4. git lab  CI/CD

 we can use docker swarm also instead of kubernetes, because it is easy to manage all the application and it has auto load balancer. 
 
 * first of all, we have to configuration the server and install the necessary dependencies by ansible,
 it can caonfigure the server very easily.
 
* then , we need one or more database based on the application.
 if we deploy database viya kubernetes we have to deploy it by stateful deployment, otherwise there will be no data synchronization
 
 * we need to setup a private docker repository in the server, as docker hub can give one private image repository for free,
 if we dont create private repository then we have to buy subscription  for storing private image in the server.
 
 * we can setup gitlab in the server, and manage ci/cd with gitlab

 * if we use kubernetes for deployment we have to create a master node and one or two worker node based on application demand  by the help of ansible. my this way all the deployed pods are highly scalable & replicated in multiple nodes.
 
 * we have to set  ingress , load balancing & proxies to manage deployed services ip and port in kubernetes

* Applications deployed through kubernetes are internally connected through service, so we dont have to expose database ports ro the internet. so that, by using kubernetes we can deploy our applications securely.

## by following these architechture we can deploy microservices to the cloud or on premises, securely 
 
 
 
 





