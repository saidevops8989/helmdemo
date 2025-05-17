#install helm on cetnos9###
curl -O https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3

#bash ./get-helm-3

#helm version

#git clone https://github.com/saidevops8989/helmdemo.git

#cd helmdemo

#kubectl create ns helmtest
namespace/helmtest created

#helm install newrelease helmtest
W0516 21:58:50.045914   28009 warnings.go:70] spec.template.spec.imagePullSecrets[0].name: invalid empty name ""
NAME: newrelease
LAST DEPLOYED: Fri May 16 21:58:49 2025
NAMESPACE: default
STATUS: deployed
REVISION: 1

#helm list
NAME      	NAMESPACE	REVISION	UPDATED                               	STATUS  	CHART         	APP VERSION
newrelease	default  	1       	2025-05-16 21:58:49.87134097 -0400 EDT	deployed	helmtest-0.1.0	1.16.0  

#helm history newrelease
REVISION	UPDATED                 	STATUS  	CHART         	APP VERSION	DESCRIPTION     
1       	Fri May 16 21:58:49 2025	deployed	helmtest-0.1.0	1.16.0     	Install complete

#kubectl get pods -n helmtest
NAME                        READY   STATUS    RESTARTS   AGE
helmtest-6ccc4cfd46-2nrp6   1/1     Running   0          2m30s
helmtest-6ccc4cfd46-5sfx2   1/1     Running   0          2m30s
helmtest-6ccc4cfd46-dztxl   1/1     Running   0          2m30s
helmtest-6ccc4cfd46-vhkcn   1/1     Running   0          2m30s

#helm uninstall newrelease
release "newrelease" uninstalled








#helm install myrelease helmtest

#helm install <releasename> <dir which contains charts values templates>

#helm  uninstall  myrelease helmtest



