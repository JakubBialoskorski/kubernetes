`kubectl create namespace pihole`

`kubectl apply -f pvc.yaml`

`helm install pihole --values values.yaml -n pihole mojo2600/pihole`