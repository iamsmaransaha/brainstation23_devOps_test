# brainstation23_devOps_test

task 2 & task3 Readme.md is inside the task folders

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

## deploy my laravel application in kubernetes by following these easy steps

```
$ minikube start
$ git clone "https://github.com/iamsmaransaha/brainstation23_devOps_test.git"
$ cd brainstation23_devOps_test
$ cd Task1/app1/deploy
$ kubectl apply -f .
$    cd ..
$    cd ..
$ cd app2/deploy
$   kubectl apply -f .
$   kubectl get pods
```

## Deployment process screenshot and output for reference:
<img width="1440" alt="Screenshot 2022-05-11 at 4 42 14 PM" src="https://user-images.githubusercontent.com/105348672/167831627-940ef983-a143-463d-be5e-f6effe095c74.png">

## after deployment we can get url by this command:
```
$ minikube service   --url --all
```
**Output:**

shoronsaha@Shorons-MacBook-Pro ~ % minikube service   --url --all

😿  service default/kubernetes has no node port

|-----------|-------------|--------------|---------------------------|
| NAMESPACE |    NAME     | TARGET PORT  |            URL            |
|-----------|-------------|--------------|---------------------------|
| default   | kubernetes  | No node port |
| default   | laravelapp1 |           80 | http://192.168.64.2:30100 |
| default   | laravelapp2 |           80 | http://192.168.64.2:30200 |
|-----------|-------------|--------------|---------------------------|

## URL Output:

**App1:**
<img width="1440" alt="Screenshot 2022-05-11 at 4 33 51 PM" src="https://user-images.githubusercontent.com/105348672/167830298-a6ab09fb-9332-4924-9f2e-4aad22004e07.png">


**APP2:**
<img width="1440" alt="Screenshot 2022-05-11 at 4 33 55 PM" src="https://user-images.githubusercontent.com/105348672/167830602-b2512476-1513-43eb-a5d1-a213ac92f41f.png">

**Minikube Dashboard:**
<img width="1040" alt="Screenshot 2022-05-11 at 4 55 59 PM" src="https://user-images.githubusercontent.com/105348672/167833734-2c53d805-28cf-402d-b90b-1a03890f3d90.png">









