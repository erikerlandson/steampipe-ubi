# steampipe-ubi
container image for steampipe installed onto UBI

run the container interactively
```sh
$ oc run -i -t --serviceaccount=steampipe steampipe --image=quay.io/erikerlandson/steampipe:latest --command -- /bin/bash
```

add "anyuid" to steampipe SA:
```sh
oc adm policy add-scc-to-user anyuid -z steampipe --as system:admin
```
