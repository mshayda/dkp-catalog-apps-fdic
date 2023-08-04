# dkp-catalog-apps
dkp-catalog-apps

```
kubectl apply -f - <<EOF
apiVersion: source.toolkit.fluxcd.io/v1beta1
kind: GitRepository
metadata:
  name: thaad-dkp-applications
  namespace: kommander-default-workspace
  labels:
    kommander.d2iq.io/gitapps-gitrepository-type: catalog
    kommander.d2iq.io/gitrepository-type: catalog
spec:
  interval: 1m0s
  ref:
    branch: main
  timeout: 20s
  url: https://github.com/sburnsd2/dkp-catalog-apps
EOF
```