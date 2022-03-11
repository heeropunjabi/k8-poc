### Build docker image locally

```bash
 docker build -t nextjs-docker .
```

### run the build image locally ( container)

```bash
 docker run -p 3000:3000 nextjs-docker
```

### Deploy to K8 

### install minikube locally ( K8 tool )

```bash
 brew install minikube
```

### install hyperkit locally ( expose minikube to local through docker darwin driver. )

```bash
 brew install hyperkit
```

### start cluster  ( mater node and worker node are running with docker container )

```bash
 minikube start --driver=hyperkit
```

### deploy service and deployment having 1 pod for nexjs-k8 docker image

```bash
 kubectl apply -f ./webapp.yaml
```


### get the expose URL for nexjs app

```bash
 minikube service --url webapp-service
```


