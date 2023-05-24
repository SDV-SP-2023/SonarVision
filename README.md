# SonarVision

## Infrastructures

### 2 machines virtuelles :
* Noms : svf001 et svb001
* Version : Debian 11
* RAM : 4GB
* Processeur : 2 coeurs


## Technologies utilisées

* Base de données avec 6 colonnes (nom, prénom, date de naissance, adresse, CP, ville)
* Installation SonarQube et Jenkins
* Microsoft Azure pour la création de machine virtuelle

## Configuration des VM

#### Création de la ressource sous Azure

```
New-AzResourceGroup -Name SonarVision -Location "East US"
```
#### Création de la VM
```
New-AzVM -ResourceGroupName SonarVision -Name vsb001 -Location 'eastus' -ImageName Debian:debian-11:11:latest -size Standard_B2s -OpenPorts 22,3306
```
