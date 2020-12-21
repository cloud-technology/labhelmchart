# labhelmchart

## Publish flow
```bash
# first create your chart template.
$ helm create yourchart

# after make some need to modify, package them.
$ helm package yourchart

# move your chart.tgz to 
$ mv yourchart-0.1.0.tgz stable

# update index.yaml to helm search repo
$ helm repo index docs --url https://cloud-technology.github.io/labhelmchart/stable

$ git add .
$ git commit -a -m "publish new version"

$ git push origin main
```

## To use and install chart
```bash
# add hekm chart repo
$ helm repo add labhelmchart https://cloud-technology.github.io/labhelmchart/stable

# update repo info
$ helm repo update

# search repo
$ helm search repo labhelmchart
NAME                	CHART VERSION	APP VERSION	DESCRIPTION                
labhelmchart/pychart	0.1.0        	1.16.0     	A Helm chart for Kubernetes

# to install chart
helm install py labhelmchart/pychart -n default
```
