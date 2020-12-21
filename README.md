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
