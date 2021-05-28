`kubectl create namespace homeassistant`

`kubectl apply -f pvc.yaml`

`helm install home-assistant k8s-at-home/home-assistant -f values.yaml -n homeassistant`

---
To apply custom configuration / automations, get the pod name and run:

`kubectl exec home-assistant-6cfc9767f6-wlk7q -n homeassistant -- ls`

`kubectl exec home-assistant-6cfc9767f6-wlk7q -n homeassistant -- pwd`

`kubectl cp configuration.yaml home-assistant-6cfc9767f6-wlk7q:/config -n homeassistant`

`kubectl cp automations.yaml home-assistant-6cfc9767f6-wlk7q:/config -n homeassistant`