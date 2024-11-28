# configmap-test

k8s上で configmap を volume mount し Podに反映させるテストです。

## How to Use

```
# setup
cd deploy
kubectl apply -f service.yaml
kubectl apply -f configmap-1.yaml
kubectl apply -f deployment.yaml

# check
curl localhost:30000

# A few later
kubectl apply -f configmap-2.yaml

```

nginxのpodの中では、/usr/share/nginx/html/index.html を configmapの中に定義したhtmlファイルで置き換えて表示しています。
