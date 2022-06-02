#  Proposition de schema pour un référentiel des aides de mobilité

Des discussions avec les collectivités (IDFM, M2A, MGP, POLD, Orléans, Aude…), les opérateurs de plateforme d’aides (MesaidesPoleEmoloi, Dora, Data•inclusion), les associations (ECF…), les conseillers mobilités (Ademe, CCI, Wimoov) ont permis d’identifier un besoin de commun et une proposition de valeur : la nécessité de créer un point d’accès national aux données d’aides à la mobilité durable sur la base d’un référentiel commun de données d’aides, exploitables par tou•tes (financeurs, bénéficiaires des aides…), à l’instar du Point d’Accès National aux données de transports (PAN) tels que les aménagements cyclables ou aires de covoiturage.

Ce repo contient la définition d'une proposition schema pour ce référentiel. La fabrique des mobilité ouvre ce travail afin d'établir un format de donnée qui correspondra le plus aux besoins du grand nombre d'acteurs.

Une première version du schema est inspiré des besoins du projet CEE [Mon Compte Mobilité (moB)](https://moncomptemobilite.fr/), ou une liste des aides à la mobilité a été établie sur ses territoires d'expérimentation : Région Ile de France et Mulhouse Alsace Agglomération.


### Intégration continue

Localement, voici la procédure à suivre pour installer l'environnement de test et lancer les tests :

```bash
# Création d'un environnement virtuel en Python 3
python3 -m venv venv
source venv/bin/activate

# Installation des dépendances
pip install -r requirements.txt

# Test de la validité du schéma
frictionless validate --type schema schema.json

# Test de la conformité des fichiers d'exemples
frictionless validate --schema schema.json exemple-valide.csv
```
