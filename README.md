# Azure-Kubernetes-Services
Repositorio con ejemplos base para la utilizacion de AKS

### Pasos para la utilizacion de AKS

se deben ejecutar los siguientes comandos basicos

creacion de grupo de recursos para AKS
- az group create -n 'nombre-de-resource-group' name  eastus 

Creacion de AKS con 4 nodes asociado a resource group creando anteriormente
- az create -n 'nombre-kubernetes-cluster' -g 'nombre-de-resource-group' -c 3 -k 1.7.7

- az AKS get-credentials -n 'nombre-kubernetes-cluster' -g 'nombre-de-resource-group'

### comandos manejo del cluster

create a service tunel to the k8 dashboard service
´´´az aks browse -n 'nombre-kubernetes-cluster' -g 'nombre-de-resource-group' ´´´

escalamiento de nodos AKS
- az aks scale -n 'nombre-kubernetes-cluster' -g 'nombre-de-resource-group' -c 'cantidad de nodos a escalar'

obtener version de AKS
az aks get-versions -n 'nombre-kubernetes-cluster' -g 'nombre-de-resource-group' 

Upgrade version AKS
az aks upgrade -n 'nombre-kubernetes-cluster' -g 'nombre-de-resource-group'  -k 1.8.2

