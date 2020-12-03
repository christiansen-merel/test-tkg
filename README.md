# test-tkg
## clusters
dev01, dev02
kubectl config use-context dev02-admin@dev02

## range metallb :
dev01 : 192.168.100.11-192.168.100.19 
vsphere-controlplane-ip : 192.168.100.10

dev02: 192.168.100.21-192.168.100.29
vsphere-controlplane-ip : 192.168.100.20


ip worker dhcp : 100 à 200 DON'T TOUCH