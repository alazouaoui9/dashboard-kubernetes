kubectl create -f CreateClusterRoleBinding.yaml 

kubectl create -f CreateServiceAccount.yaml 

kubectl create -f kubernetes-dashboard.yaml 

kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')
