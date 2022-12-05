## 用户指南
- [参考](https://docs.aws.amazon.com/zh_cn/eks/latest/userguide/getting-started.html)

## 更新EKS kubeconfig 文件
aws eks update-kubeconfig --region us-east-2 --name k8s --role-arn arn:aws:iam::553524721138:role/eks

aws eks update-kubeconfig --name k8s

aws eks update-kubeconfig --region us-east-2 --name k8s --role-arn arn:aws:iam::553524721138:role/eksClusterRole

aws eks update-kubeconfig --region us-east-2 --name k8s --role-arn arn:aws:iam::553524721138:role/eks-node-iam

aws eks update-kubeconfig --region us-east-1 --name k8s --role-arn arn:aws:iam::553524721138:role/eks-node-iam


- [参考](https://docs.aws.amazon.com/zh_cn/eks/latest/userguide/create-kubeconfig.html)

## EKS 授权问题
aws eks update-kubeconfig \
    --region us-east-2 \
    --name k8s \
    --role-arn arn:aws:iam::553524721138:role/eks
- [参考](https://docs.aws.amazon.com/zh_cn/eks/latest/userguide/troubleshooting.html#unauthorized)


### 让 IAM 用户和角色有权访问您的集群
- [参考](https://docs.aws.amazon.com/zh_cn/eks/latest/userguide/add-user-role.html)

## aws configure
- [参考](https://blog.csdn.net/weixin_47872288/article/details/125109209)


## 登录
ssh -i /Users/zhengqilin/My/aws_service/aws-eks-password.pem  ec2-user@ec2-3-17-133-47.us-east-2.compute.amazonaws.com
