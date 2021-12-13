# Quake 3 Arena on K3s
Original article: https://johansiebens.dev/posts/2020/11/quake-iii-arena-k3s-and-a-raspberry-pi/

### How to run
`kubectl create namespace quake`

`kubectl apply -f quake.yaml`

### Gotchas
I've removed `inlets-operator` as I run it through MetalLB, I also use plain HTTP for local LAN parties.