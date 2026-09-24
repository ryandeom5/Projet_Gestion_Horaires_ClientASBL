# Comprendre et Parler

Application web développée dans le cadre d'un projet intégré à la Haute École Robert Schuman (HERS).

L'application permet notamment de gérer des **interprètes**, des **bénéficiaires**, des **missions** et des **créneaux horaires**, avec une interface web permettant de consulter et gérer les différentes informations.

## Technologies utilisées

* Java
* Spring Boot
* Maven
* Base de données SQL
* HTML / CSS / JavaScript
* Thymeleaf
* Bootstrap

## Structure du projet

```text
├── database/
│   ├── Script_creation_BD.sql
│   ├── Script_initialisation_BD.sql
│   ├── Script_trigger_BD.sql
│   └── Script_view_BD.sql
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   ├── python/
│   │   └── resources/
│   └── test/
│
├── docs/
├── pom.xml
├── mvnw
└── mvnw.cmd
```

## Installation

### Prérequis

Avant de lancer l'application, il faut disposer de :

* un JDK compatible avec le projet ;
* une base de données compatible avec les scripts SQL ;
* IntelliJ IDEA ou un autre IDE Java ;
* Maven (facultatif si le Maven Wrapper est utilisé).

### 1. Télécharger le projet

Cloner ou télécharger ce dépôt.

### 2. Configurer la base de données

Les scripts nécessaires se trouvent dans le dossier `database/`.

Ils doivent être exécutés dans l'ordre suivant :

1. `Script_creation_BD.sql`
2. `Script_trigger_BD.sql`
3. `Script_initialisation_BD.sql`
4. `Script_view_BD.sql`

Le premier script crée la structure de la base de données.

Le deuxième met en place les triggers nécessaires à l'insertion et à la gestion des données.

Le troisième initialise la base avec les données de démonstration.

Le dernier met en place les vues nécessaires au fonctionnement de l'application.

### 3. Configurer l'application

Le fichier de configuration se trouve ici :

```text
src/main/resources/application.properties
```

Les identifiants présents dans la version publique du projet sont volontairement remplacés par des valeurs fictives (`XXXX`).

Il faut remplacer ces valeurs par les paramètres correspondant à votre propre environnement local.

Exemple :

```properties
spring.application.name=Comprendre_et_Parler

# Base de données
db.login=XXXX
db.password=XXXX

# Email
mail.host=smtp.gmail.com
mail.port=587
mail.user=XXXX
mail.password=XXXX
mail.from=XXXX
```

**Aucun compte ou mot de passe personnel n'est fourni avec ce dépôt.**

### 4. Lancer l'application

Avec IntelliJ IDEA, ouvrir le projet en tant que projet Maven puis lancer :

```text
ComprendreEtParlerApplication.java
```

## Comptes de démonstration

La base de données contient des comptes fictifs permettant de tester les différentes fonctionnalités de l'application.

| Rôle         | Identifiant | Mot de passe |
| ------------ | ----------- | ------------ |
| Responsable  | `LM2601`    | `DemoUserPI` |
| Responsable  | `TD2601`    | `DemoUserPI` |
| Interprète   | `ML2601`    | `DemoUserPI` |
| Interprète   | `CB2601`    | `DemoUserPI` |
| Bénéficiaire | `EP2601`    | `DemoUserPI` |
| Bénéficiaire | `HM2601`    | `DemoUserPI` |

Les données présentes dans la base sont des **données de démonstration fictives**.

## Fonctionnalités principales

L'application permet notamment de :

* gérer les utilisateurs ;
* gérer les interprètes ;
* gérer les bénéficiaires ;
* consulter et gérer les missions ;
* gérer les disponibilités et créneaux horaires ;
* gérer différentes compétences ;
* consulter les informations liées aux utilisateurs ;
* gérer l'authentification ;
* gérer les mots de passe ;
* consulter un calendrier des horaires.

## Tests

Les tests automatisés se trouvent dans :

```text
src/test/java/
```

Ils couvrent notamment différents modèles et DAO de l'application.

## Sécurité

Ce dépôt est une version destinée à la démonstration et au portfolio.

Les informations sensibles du projet original ont été retirées ou remplacées par des valeurs fictives.

Les données personnelles présentes dans les scripts SQL ont également été remplacées par des données de démonstration.

Pour une utilisation réelle, les identifiants de base de données et les paramètres de messagerie doivent être configurés localement et ne doivent pas être publiés dans le dépôt.

## Projet

Projet réalisé dans le cadre du cursus informatique à la **Haute École Robert Schuman (HERS)**.

Version publiée à des fins de portfolio et de démonstration.
