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
Les indicateurs FMD permettent de classer les machines selon leurs valeurs et de décider d'une politique
ou des priorités d'action circonstanciées.
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
Le RAID permet de sécuriser les données, améliorer les performances
et garantir la haute disponibilité de celles-ci.
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
La virtualisation est un processus qui va permettre de masquer, d'émuler et de partager des
caractéristiques physiques d’une ressource informatique de manière à en simplifier la gestion et les interactions
avec un ou plusieurs systèmes, applications et utilisateurs.
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
• Une réduction de l’infrastructure physique et des économies d’´énergies.
(équipements,alimentation climatisation...)
• Une reprise automatique lors des incidents, sauvegarde et restauration et
migration facilitées des systèmes virtualisés.
• Optimisation de la sécurité et la sûreté de ses données par cloisonnement
• Une installation, un démarrage rapide et une sauvegarde d'état.

Inconvénients :
• La panne d'une machine physique impacte plusieurs environnements virtuels
• Nécessite des machine puissantes (CPU, mémoire, disques ..) et spécifiques.
• Une dégradation des performances (temps de réponse …)
• Une complexité accrue et donc une analyse d’erreurs plus difficile.
• Une impossibilité de virtualisation. ( système non pris en charge ou dégradation des perf. trop
importante).

```

```
```

```
```

```
```

```
```

```
```

