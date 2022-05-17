Project page is [here](https://longhorn.io/) .

I highly recommend reading [this](https://rpi4cluster.com/k3s/k3s-storage-setting/) article, as you may use formatted pendrives with Raspberry Pi's for Longhorn (this needs to be set up before initialising storage controller).

`git clone -b v1.2.4 https://github.com/longhorn/longhorn.git`

Edit the chart (set UI from ClusterIP to LoadBalancer) then:

`helm install longhorn ./longhorn/chart/ --namespace longhorn-system --set defaultSettings.defaultDataPath="/storage"`

### Secrets
You need AWS key/secret to use S3 backups. Create a file named `secret.yaml` and apply it by running `kubectl apply -f secret.yaml` .
To encode secret string use:

`echo -n 'whatever_string' | base64`

To decode secrets use:

`kubectl get secret secret -o yaml -n longhorn-system`

`echo 'whatever_string' | base64 --decode`