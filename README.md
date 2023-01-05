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
```

```
a. Services de fichiers partagés : NAS (Network Attached Storage)
b. Services de données partagées : Base de données (BDD) ou Annuaire (LDAP)
c. Services de partitions partagées : SAN (Storage Area Network) 
```

```

```

```

```

