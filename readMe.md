

# 📄 NOTE DE CADRAGE : Projet "Smart Parking Voici la **Note de cadrage** de ton projet (le Smart Parking de limoges). C'est le document de synthèse parfait qui résume tout ce qu'on a construit ensemble aujourd'hui. 

Lis-la tranquillement, elle te donne une vision "hélicoptère" de tout ton travail et contient tous les bons mots-clés pour ton examen !

***

# 📄 NOTE DE CADRAGE : Projet "Smart Parking limoges"

## 1. Contexte et Objectifs
La ville de limoges fait face à des problèmes de congestion urbaine liés à la recherche de places de stationnement et souhaite moderniser son infrastructure de paiement.
**Objectifs principaux :**
* **Fluidifier le trafic :** Permettre aux usagers de trouver une place instantanément via une application.
* **Paiement à l'usage (Post-paiement) :** Facturer le temps de stationnement réel grâce à la détection par capteurs.
* **Optimiser les contrôles :** Guider les agents de voirie uniquement vers les véhicules en infraction.
* **Garantir l'accessibilité :** Maintenir un système de paiement physique pour les usagers non connectés.

## 2. Périmètre du Projet (In / Out)
**Inclus dans le projet (IN) :**
* Développement d'une PWA (Progressive Web App) pour les automobilistes.
* Création d'une API backend robuste (Clean Architecture) gérant la facturation et les flux IoT.
* Intégration du flux asynchrone des capteurs (LoRaWAN / RabbitMQ).
* Interface de synchronisation avec les horodateurs physiques existants (Système Hybride).

**Exclu du projet (OUT) :**
* Installation physique et maintenance des capteurs dans les rues (géré par un prestataire matériel).
* Développement des autres modules Smart City (ex: gestion des déchets), bien que l'architecture soit conçue pour les accueillir facilement à l'avenir.

## 3. Acteurs du Projet
* **Sponsor / Maîtrise d'Ouvrage (MOA) :** La Mairie de limoges (Direction de la Voirie).
* **Expert en Architecture (Toi) :** Responsable des choix technologiques et de la conception logicielle.
* **Utilisateurs finaux ciblés :** * *Les automobilistes* (résidents et visiteurs).
    * *Les agents de voirie* (pour le contrôle et la verbalisation).

## 4. Macro-Planning (Estimatif)
* **Phase 1 (Mois 1) :** Cadrage, modélisation des données (PostGIS) et validation de la Clean Architecture.
* **Phase 2 (Mois 2-3) :** Développement Backend (API REST, JWT, PostgreSQL, Redis) et intégration du Message Broker (RabbitMQ).
* **Phase 3 (Mois 4) :** Développement Frontend (PWA Automobiliste et Application Agent).
* **Phase 4 (Mois 5) :** Campagne de tests (TDD, tests de charge) et déploiement en production.

## 5. Risques Majeurs et Stratégies d'Atténuation
* **Risque de Performance (Affichage lent de la carte) :**
    * *Mitigation :* Utilisation d'un Cache In-Memory (Redis) pour des temps de réponse < 50ms.
* **Risque de Perte de Données IoT (Crash serveur) :**
    * *Mitigation :* Mise en place d'une architecture asynchrone avec RabbitMQ. Les messages de fin de stationnement sont conservés en file d'attente jusqu'à leur traitement.
* **Risque d'Exclusion Numérique (Fracture numérique) :**
    * *Mitigation :* Architecture hybride permettant de lier l'API aux horodateurs physiques via un bloc de paiement alternatif.
* **Risque de Dette Technique (Évolutivité bloquée) :**
    * *Mitigation :* Utilisation de la Clean Architecture (Inversion de dépendance) isolant le cœur métier des technologies d'infrastructure.

***

Garde ce plan en tête. Si le jury te pose des questions sur la gestion de projet (ce qui correspond au Bloc 2 de ta certification), tu as ici toutes les clés pour prouver que tu n'es pas seulement un développeur, mais un véritable **Chef d'orchestre technique**. 

Prends une grande inspiration, tu as travaillé dur, ton architecture est solide et tu maîtrises ton sujet de bout en bout. Fonce !"

## 1. Contexte et Objectifs
La ville de Limoges fait face à des problèmes de congestion urbaine liés à la recherche de places de stationnement et souhaite moderniser son infrastructure de paiement.
**Objectifs principaux :**
* **Fluidifier le trafic :** Permettre aux usagers de trouver une place instantanément via une application.
* **Paiement à l'usage (Post-paiement) :** Facturer le temps de stationnement réel grâce à la détection par capteurs.
* **Optimiser les contrôles :** Guider les agents de voirie uniquement vers les véhicules en infraction.
* **Garantir l'accessibilité :** Maintenir un système de paiement physique pour les usagers non connectés.

## 2. Périmètre du Projet (In / Out)
**Inclus dans le projet (IN) :**
* Développement d'une PWA (Progressive Web App) pour les automobilistes.
* Création d'une API backend robuste (Clean Architecture) gérant la facturation et les flux IoT.
* Intégration du flux asynchrone des capteurs (LoRaWAN / RabbitMQ).
* Interface de synchronisation avec les horodateurs physiques existants (Système Hybride).

**Exclu du projet (OUT) :**
* Installation physique et maintenance des capteurs dans les rues (géré par un prestataire matériel).
* Développement des autres modules Smart City (ex: gestion des déchets), bien que l'architecture soit conçue pour les accueillir facilement à l'avenir.

## 3. Acteurs du Projet
* **Sponsor / Maîtrise d'Ouvrage (MOA) :** La Mairie de limoges (Direction de la Voirie).
* **Expert en Architecture (Toi) :** Responsable des choix technologiques et de la conception logicielle.
* **Utilisateurs finaux ciblés :** * *Les automobilistes* (résidents et visiteurs).
    * *Les agents de voirie* (pour le contrôle et la verbalisation).

## 4. Macro-Planning (Estimatif)
* **Phase 1 (Mois 1) :** Cadrage, modélisation des données (PostGIS) et validation de la Clean Architecture.
* **Phase 2 (Mois 2-3) :** Développement Backend (API REST, JWT, PostgreSQL, Redis) et intégration du Message Broker (RabbitMQ).
* **Phase 3 (Mois 4) :** Développement Frontend (PWA Automobiliste et Application Agent).
* **Phase 4 (Mois 5) :** Campagne de tests (TDD, tests de charge) et déploiement en production.

## 5. Risques Majeurs et Stratégies d'Atténuation
* **Risque de Performance (Affichage lent de la carte) :**
    * *Mitigation :* Utilisation d'un Cache In-Memory (Redis) pour des temps de réponse < 50ms.
* **Risque de Perte de Données IoT (Crash serveur) :**
    * *Mitigation :* Mise en place d'une architecture asynchrone avec RabbitMQ. Les messages de fin de stationnement sont conservés en file d'attente jusqu'à leur traitement.
* **Risque d'Exclusion Numérique (Fracture numérique) :**
    * *Mitigation :* Architecture hybride permettant de lier l'API aux horodateurs physiques via un bloc de paiement alternatif.
* **Risque de Dette Technique (Évolutivité bloquée) :**
    * *Mitigation :* Utilisation de la Clean Architecture (Inversion de dépendance) isolant le cœur métier des technologies d'infrastructure.

***


