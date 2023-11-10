## Installing Mid Server

```
    kubectl create namespace servicenow
```

```
kubectl create secret docker-registry regcred --docker-server=registry.k8s.sndevops.xyz --docker-username=<> --docker-password=<> --docker-email=registry@sndevops.xyz
```

helm template demomidserver1 ./ --set midEnv.MID_INSTANCE_URL=https://empsnrao1.service-now.com --set midEnv.MID_INSTANCE_USERNAME=mid  --set midEnv.MID_INSTANCE_PASSWORD=$MID_PASSWORD --set midEnv.MID_SERVER_NAME=demomidserver1