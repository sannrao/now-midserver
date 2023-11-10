# Running Mid Server


```
helm repo add nowmidserver https://sannrao.github.io/now-midserver/

helm install demomidserver1 nowmidserver/midserver --set midEnv.MID_INSTANCE_URL=https://my.service-now.com --set midEnv.MID_INSTANCE_USERNAME=mid  --set midEnv.MID_INSTANCE_PASSWORD=$MID_PASSWORD
```

## Publising the chart

### Check for any issues

```
helm lint helm
```

### Create Package

```
helm package helm
```

### Create index

```
helm repo index --url https://sannrao.github.io/now-midserver/ .
```
