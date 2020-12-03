# test-tkg
## Infra
### tunnel SSH :
```bash
# ssh ubuntu@IPENV -L 9090:192.168.100.11:80
```

### clusters
dev01, dev02
```bash
# kubectl config use-context dev02-admin@dev02
```
### range metallb :
dev01 : 192.168.100.11-192.168.100.19 
vsphere-controlplane-ip : 192.168.100.10

dev02: 192.168.100.21-192.168.100.29
vsphere-controlplane-ip : 192.168.100.20
ip worker dhcp : 100 à 200 DON'T TOUCH

## deployment dev01
### metallb
```bash
# kubectl apply -k metallb/overlays/dev01
```

### kuard
```bash
# kubectl apply -f test1-adresseip-pod/kuard.yaml
```
check browser `http://localhost:9090`