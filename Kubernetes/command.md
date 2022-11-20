## 标签（label） 

### 给节点打上标签
kubectl label nodes m1 node=master 

### 查看node上的标签
kubectl get node --show-label

### 将pod部署到指定标签的node上
...
spec
  nodeSelector:
    node: master
...
