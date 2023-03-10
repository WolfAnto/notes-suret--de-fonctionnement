# notes-suret--de-fonctionnement

## Introduction
```
la sûreté : fiabilité, disponibilité et maintenabilité
```

```
la sécurité qui recouvre les dispositions suivantes :
– la confidentialité
– imputabilité et traçabilité des informations
– l’intégrité des systèmes et des données
```

```
Valeur = confidentialité * intégrité * disponibilité
```

```
politique de sécurité = empecher, détecter, intervenir
```

## PCA/PRA
```
Risques physiques :
- Désastre naturel
-Environnement
-Panne matérielle
-Panne du réseau
-Coupure électrique
```

```
Risques humaines :
-Erreur de conception
```

```
Risques opérationnelles :
-Bogue
-Mauvaise configuration, saisie, absentéisme
-Obsolescence des technologies
```

```
Télérance aux pannes :
(capacité d'un système à fonctionner malgré une défaillance)
-redondance (duplication)
-matériel extractibles à chaud (hot swappable)
En anglais le terme de « Fail-Over Service » (noté FOS) est ainsi utilisé
```

```
Sauvegarde :
-Réguliere
-méthode 3 2 1
```

## Haute disponibilité
```
Assurer le bon fonctionnement d'un service 24H/24
FMD désigne le triptyque Fiabilité , Maintenabilité , Disponibilité
Les indicateurs FMD permettent de classer les machines selon leurs valeurs et de décider d'une politique ou des priorités d'action circonstanciées.
```

## Les différentes Solutions
```
-Redondance
	>sauvegarde, réplication, partage
	> surveillance
	> Mode Actif/Passif
	>agrégation
```

```
-Clustering
	> Répartition ou équilibrage de charge (load balancing)
	> Gestion dynamique des éléments
	> Mode Actif/Actif
```

```
Le RAID permet de sécuriser les données, améliorer les performances et garantir la haute disponibilité de celles-ci.
Créer des snapshots
```

```
a. Services de fichiers partagés : NAS (Network Attached Storage)
b. Services de données partagées : Base de données (BDD) ou Annuaire (LDAP)
c. Services de partitions partagées : SAN (Storage Area Network) 
```

```
Agrégation Ethernet : bond0
```
```
Pont/bridge : br0
```
```
Vlan : vlan0
```

## Virtualisation
```
La virtualisation est un processus qui va permettre de masquer, d'émuler et de partager des caractéristiques physiques d’une ressource informatique de manière à en simplifier la gestion et les interactions avec un ou plusieurs systèmes, applications et utilisateurs.
```

## Virtualisation de réseaux
```
Exemples :
> VLAN
> VPN
```

##  Cartes réseaux des Vm
```
> Pont (bridge)
> Routeur avec NAT
> Hôte seulement
> réseau privé interne
```

## Les machines virtuelles
```
Consiste à partager ou émuler les ressources physiques du serveur pour chaque système d’exploitation.
Ces environnements isolés sont appelés serveurs privés virtuels ou émulateurs. 
```

```
Avantages :
• Optimisation de l’infrastructure, de la charge de travail des serveurs
• Une réduction de l’infrastructure physique et des économies d’´énergies. (équipements,alimentation climatisation...)
• Une reprise automatique lors des incidents, sauvegarde et restauration et migration facilitées des systèmes virtualisés.
• Optimisation de la sécurité et la sûreté de ses données par cloisonnement
• Une installation, un démarrage rapide et une sauvegarde d'état.

Inconvénients :
• La panne d'une machine physique impacte plusieurs environnements virtuels
• Nécessite des machine puissantes (CPU, mémoire, disques ..) et spécifiques.
• Une dégradation des performances (temps de réponse …)
• Une complexité accrue et donc une analyse d’erreurs plus difficile.
• Une impossibilité de virtualisation. ( système non pris en charge ou dégradation des perf. trop importante).
```

## Type de virtualisation
```
Emulation matérielle
Virtualisation totale
Para virtualisation
Virtualisation au niveau matériel
```

## La virtualisation d’applications
```
Wine
Sandbox
App-V
LXC
Docker
```

## Solutions serveurs
```
VmWare ESX
Hyper-V
KVM
XEN
Virtualbox
Proxmox
```

## Virtualisation du poste de travail
```
Client léger & Client zéro

Avantages :
- L’indépendance vis-à-vis du matériel
- Le déploiement rapide des nouvelles applications et des mises à jour
- La surveillance centralisée des performances
- La gestion des modifications apportées aux postes par les utilisateurs
- La possibilité de réduire la consommation électrique
```

## Gérer les espaces de stockage
```
Gérer les disques
Organiser l'arborescence (physique et logique) 
Protéger , contrôler, sécuriser
Gérer, Surveiller l'espace disques
Organiser l'intégrité, sauvegardes et synchro

Méthodologie :
> Sauvegarder
> Consigner
> Etablir des procédures
> Faire de la prévention
```

## Les différentes types de stockage
```
> bandes magnétiques (Archivage)
> disques magnétiques (Haute disponibilité)
> Disques flash (Haute disponibilité)
> Disques optiques (Archivage)
```

## Méthodes de sauvegarde et archivage
```
> Archivage
> Sauvegarde incrémentale
consiste à sauvegarder, une première fois, la totalité d’une arborescence et de sauvegarder ensuite, d’une fois à l’autre, les seuls fichiers qui ont été modifiés. Elle dépend de la sauvegarde précédente ( taille constante )

> La sauvegarde différentielle
dépend de la sauvegarde seulement initiale ( taille augmente de jour en jour ) 

> Tour de Hanoï
double sauvegarde des changements, différence sur 2 jour au maximum (Pour un cycle d’une semaine : 0 3 2 5 4 7 6)

> Sauvegarde physique de disques et de systèmes de fichiers
> Sauvegarde Bare Metal
>  Sauvegarde réseau
```

## Stockage locale
```
> DAS (Direct Attached Storage)
> RAID 0 : n'est pas une redondance mais une association de disques (Plus rapide)
> Remarque : Un RAID ne remplace pas les sauvegardes
```

## Stockage en réseau
```
> NAS (Network Attached Storage), Serveur de fichier
> SAN (Storage Area Network) , réseau de stockage fiable et dédié
```

## Réplication de données
```
> réplication synchrone
L'écriture des données se fait en temps réel sur tous les disques (locaux et distants).

> réplication asynchrone
L'écriture ne se fait que sur le disque répliqué et les opérations sont empilées avant d'être écrits sur les autres

> réplication semi-synchrone
C'est un compromis entre la réplication synchrone et la réplication asynchrone. L'écriture est réalisée sur le disque répliqué, et une fois qu'elle est terminée, elle est répliquée sur les disques distants.

> réplication périodique
C'est une solution d'économie de la bande passante. Les données sont écrites localement sur le disque répliqué, mais l'opération de réplication n'intervient que périodiquement à des moments bien définis, comme la nuit.
```

## Hyperconvergence
```
L'infrastructure hyperconvergée est un type d'infrastructure informatique distribuée dans lequel le stockage partagé est délivré non pas par une baie de stockage SAN ou NAS, mais par une couche logicielle exploitant la capacité des disques durs installés dans les serveurs eux-mêmes.
```


