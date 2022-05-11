# brainstation23_devOps_test

## Task1

### for Task 1 , i have created two laravel project: 

location: Task1/app1/SRC & Task2/app2/SRC

>Dockerfile is included in the project

>vhost.conf also included in the project

**i have built the docker images & pushed to the docker hub by following these methods:**

```
cd Task1/app1/SRC
docker image build -t <docker_id>/<image_name>:<tag> .
docker push <docker_id>/<image_name>:<tag>

cd Task2/app2/SRC
docker image build -t <docker_id>/<image_name>:<tag> .
docker push <docker_id>/<image_name>:<tag>
```

**kubernetes configmap,service & deployment file is  on the deploy folder**

location: Task1/app1/deploy & Task2/app2/deploy

> i have used minikube to deploy these services to kubernetes






