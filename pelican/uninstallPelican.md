# Uninstall pelican from EKS

To uninstall the pelican from EKS execute the following steps

### Run helm list command to get the release name
```
  $ helm list
```
![alt text](resources/pelican-uninstall/00-helm-list.png)
*note down the pelican release name that you wish to delete*

### Uninstall the helm release
```
  $ helm delete <pelican release name>
```
![alt text](resources/pelican-uninstall/01-helm-delete.png)

### List the associated persistent volume and persistent volume claims
```
  $ kubectl get pv,pvc
```
![alt text](resources/pelican-uninstall/02-list-pv-pvc.png)

### Remove the persistent volume and persistent volume claims
```
  $ kubectl delete persistentvolumeclaim/mysql-data-<release-name>-db-0
  $ kubectl delete persistentvolume/<pv with claimref as pelican-web>
```
![alt text](resources/pelican-uninstall/03-del-pv-pvc.png)
