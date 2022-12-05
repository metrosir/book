## 标签（label）

### 给节点打上标签
kubectl label nodes m1 node=master 

### 查看node上的标签
kubectl get node --show-labels

### 将pod部署到指定标签的node上
...
spec
  nodeSelector:
    node: app-mesh
...

# 日志类
journalctl -xefu kubelet

# kubectl -h
## 生成yaml
kubectl create deployment my-dep --image=nginx --replicas=3 --dry-run='client' -o yaml 

## 查看api相关命令
kubectl explain ingress

## 设置默认sc
kubectl patch storageclass openebs-hostpath -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'
kubectl patch storageclass local-path -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'

# 标签类
## 查看node标签
kubectl  get nodes --show-labels=true

## 添加node标签
kubectl label nodes k8s-node1 worker=true

## 删除node标签
kubectl label nodes k8s-node1 worker-

## 覆盖之前node标签
kubectl label nodes k8s-node1 worker=false --overwrite

## 添加pod标签，和node语法一样
kubectl label pods web version=1.0

# 污点类

## 添加污点
kubectl taint node k8s-node1 kubeedge="":NoExecute
kubectl taint node k8s-node1 kubeedge="":NoSchedule

## 删除污点
kubectl taint node k8s-node1 kubeedge-

# 删除类

###########删除类###########
## 强制删除pod
kubectl delete pod [pod name] --force --grace-period=0 -n [namespace]

## 删除命名空间下所有资源（cm、secrets、rbac相关除外）
kubectl delete all --all -n cattle-prometheus

## 删除NAMESPACE
kubectl delete namespace NAMESPACENAME --force --grace-period=0
###########删除类###########

# 日志类

## 具体到pod中某个容器
kubectl logs -n [namespace] [pod name] -c  [container name] -f

# 资源使用情况

kubectl top node
kubectl top pod
kubectl api-resources
kubectl api-versions
kubectl config view
## 查看节点使用情况
kubectl describe node k8s-node1


# 更新回滚类

## 检查整个deployment部署的历史记录
kubectl rollout history deploy [deploy name] -n [namespace]
## 查看某个指定历史版本
kubectl rollout history deploy [deploy name] -n [namespace] --revision=2


## 查看 rollout 的状态
kubectl rollout status deploy [deploy name] -n [namespace]

## 重启某个资源
kubectl rollout restart deploy [deploy name] -n [namespace]

## 撤销本次发布回滚到上一个部署版本
kubectl rollout undo deploy [deploy name] -n [namespace]
## 回滚到指定版本
kubectl rollout undo deploy [deploy name] -n [namespace] --to-revision=2


## 暂停deployment的更新：
kubectl rollout pause deploy [deploy name] -n [namespace]


# 更新回滚类

## 检查整个deployment部署的历史记录
kubectl rollout history deploy [deploy name] -n [namespace]
## 查看某个指定历史版本
kubectl rollout history deploy [deploy name] -n [namespace] --revision=2


## 查看 rollout 的状态
kubectl rollout status deploy [deploy name] -n [namespace]

## 重启某个资源
kubectl rollout restart deploy [deploy name] -n [namespace]

## 撤销本次发布回滚到上一个部署版本
kubectl rollout undo deploy [deploy name] -n [namespace]
## 回滚到指定版本
kubectl rollout undo deploy [deploy name] -n [namespace] --to-revision=2


## 暂停deployment的更新：
kubectl rollout pause deploy [deploy name] -n [namespace]
