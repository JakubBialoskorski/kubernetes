#### `git clone -b v1.1.0 https://github.com/longhorn/longhorn.git`

Edit the chart (set UI from ClusterIP to LoadBalancer) then:

`helm install longhorn ./longhorn/chart/ --namespace longhorn-system --set defaultSettings.defaultDataPath="/storage"`

### Secrets
#### You need AWS key/secret to use S3 backups. Create a file named `secret.yaml` and apply it by running `kubectl apply -f secret.yaml` .
To encode secret string use:

`echo -n 'whatever_string' | base64`

To decode secrets use:

`kubectl get secret secret -o yaml -n longhorn-system`

`echo 'whatever_string' | base64 --decode`