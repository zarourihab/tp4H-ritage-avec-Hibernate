TP 4 : Héritage avec Hibernate - Stratégies de Mapping
1. Objectif du TP

L’objectif de ce TP est d’étudier les différentes stratégies d’héritage en JPA avec Hibernate et de comprendre comment les classes Java héritées sont représentées dans la base de données.

Les stratégies étudiées sont :

SINGLE_TABLE

JOINED

TABLE_PER_CLASS

Le projet utilise Hibernate comme implémentation JPA et H2 Database comme base de données.

2. Technologies utilisées

Dans ce TP nous avons utilisé :

Java 8

Maven

JPA (Java Persistence API)

Hibernate

H2 Database

Hibernate Validator

SLF4J

3. Configuration du projet

Le projet est configuré avec Maven à travers le fichier pom.xml contenant les dépendances :

JPA API

Hibernate Core

Hibernate Validator

H2 Database

SLF4J

JUnit

Le fichier persistence.xml permet de configurer :

la connexion à la base H2

le dialecte Hibernate

la création automatique des tables

l’affichage des requêtes SQL.

4. Stratégies d’héritage implémentées
4.1 Stratégie SINGLE_TABLE

Dans cette stratégie, toutes les classes héritées sont stockées dans une seule table.

Classe de base :

Vehicule

Classes dérivées :

Voiture

Moto
4.2 Stratégie JOINED

Dans cette stratégie :

la classe parent possède une table

chaque classe enfant possède sa propre table

Classe de base :

Employe

Classes dérivées :

Developpeur

Manager
Les tests montrent que Hibernate gère correctement l’héritage en base de données.

Chaque stratégie produit une structure différente des tables :

SINGLE_TABLE → une seule table

JOINED → plusieurs tables liées

TABLE_PER_CLASS → une table par classe
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001051" src="https://github.com/user-attachments/assets/c9b3c9e5-9071-4f0b-b87a-0a17d6d2f19d" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001100 - Copie" src="https://github.com/user-attachments/assets/a078fa86-ae9b-4009-ad9f-105b7ebb3abf" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001100" src="https://github.com/user-attachments/assets/21c45ffd-d58e-40bd-9653-5c7d21655852" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001108" src="https://github.com/user-attachments/assets/3f28e79a-981b-425d-81cd-c80f37de9390" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001119" src="https://github.com/user-attachments/assets/3bf27e26-9b9e-4478-857b-783387009081" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001130" src="https://github.com/user-attachments/assets/91a069ed-d1c7-4542-8291-41453d707d3d" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001142" src="https://github.com/user-attachments/assets/7e8a13dc-16b2-467c-b87c-782a3811c5f2" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001154" src="https://github.com/user-attachments/assets/5c442c0f-ab8b-48e2-b0ea-294c1c769afe" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001204" src="https://github.com/user-attachments/assets/e1e0a25c-dd80-482f-9678-0921cec97dfa" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001214" src="https://github.com/user-attachments/assets/5d718033-98e4-4d4b-8771-4e4cf69b9d8c" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001223" src="https://github.com/user-attachments/assets/48e3711e-bce2-48f6-a429-cea2e12aa65d" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001233" src="https://github.com/user-attachments/assets/8e20fc23-ef4d-415a-b975-cb20bb3d5326" />
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001304" src="https://github.com/user-attachments/assets/dc0b202e-1506-474f-a4d6-a46b3f36c854" />

<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001313" src="https://github.com/user-attachments/assets/d748011a-1c65-4481-a2cd-7a8d18adf6e4" />

<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 001154 - Copie" src="https://github.com/user-attachments/assets/6e392903-f905-480e-98ea-643279d4c983" />
diagramme de classe
<img width="1920" height="1080" alt="Capture d&#39;écran 2026-02-24 213918" src="https://github.com/user-attachments/assets/037de003-afd7-40e7-a6b7-26f92f146460" />
