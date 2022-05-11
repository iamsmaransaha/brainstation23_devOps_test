# brainstation23_devOps_test Task2

## Installing Vagrant

* in mac OS to install vagrant we need virtualbox too,  command is: 

```
$ brew install virtualbox

$ brew install vagrant

```
* after that we have to install ansible

```
$ brew install ansible
```

after completing the installation process 

```
vagrant up
```

* now change the  vm network ip to your own virtual box ip range

* then again use vagrant up command

now when the vagrant is up and running

```
$ vagrant ssh kube-master-node
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.3.1/aio/deploy/recommended.yaml
kubectl proxy --url
```

then the kubernetes dashboard will be visible








