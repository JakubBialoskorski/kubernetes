# uptime-kuma on k3s
Original project can be [found here](https://github.com/louislam/uptime-kuma). There is a [separate branch for kubernetes](https://github.com/louislam/uptime-kuma/tree/k8s-unofficial), which I've adjusted to suit my needs.

### How to run
`kubectl create namespace uptime-kuma`

`kubectl apply -f pvc.yaml`

`kubectl apply -f service.yaml`

`kubectl apply -f deployment.yaml`