#  Générateur de L-Système (Système de Lindenmayer)

Un générateur et visualiseur interactif de **L-systèmes (systèmes de Lindenmayer)** développé en Java. Ce projet permet de modéliser des processus de croissance organique (plantes, arbres) et de générer des fractales complexes en appliquant des règles de réécriture formelles, modélisées ensuite graphiquement grâce à un moteur de rendu basé sur la géométrie de la Tortue.

---

##  Technologies Utilisées

*   **Langage** : Java (JDK 8 ou supérieur)
*   **Interface Graphique (GUI)** : Java Swing & AWT (composants personnalisés dans `view`)
*   **Architecture** : Patron de conception **MVC (Modèle-Vue-Contrôleur)** avec un système de notification personnalisé (`Ecoutable`, `Ecoteur`).
*   **Automatisation** : Script Bash (`App.sh`) pour compiler et exécuter l'application en un clic.

---

##  Fonctionnalités principales

*   **Système de Règles Flexible (`LSystemRuler`)** : Définition de règles de réécriture complexes pour transformer l'axiome à chaque itération.
*   **Moteur de Génération (`LSystemGenerate`)** : Évaluation rapide des chaînes de caractères et gestion des exceptions de génération (`GeneratorException`).
*   **Rendu Géométrique de la Tortue** :
    *   Interprétation de commandes de déplacement et de rotation vectorielle.
    *   Calcul précis des coordonnées cartésiennes (`Coordonnees` et `MathsUtils`).
    *   Gestion de l'historique des positions pour supporter la ramification des branches.
*   **Interface Graphique Complète** :
    *   **Zone de Dessin (`ZoneAffichage`)** : Rendu visuel propre et dynamique.
    *   **Configuration (`ParametresConfiguration`)** : Ajustement de l'angle, du nombre d'itérations, de l'axiome et des règles.
    *   **Barre d'outils et Menus (`BarreOutils`, `MenuPrincipal`)** : Navigation fluide et ergonomique.
*   **Tests Unitaires (`test/`)** : Validation de la logique de réécriture et de génération pour garantir la stabilité du moteur.

---

##  Structure du Projet

Voici l'organisation exacte des sources de l'application :

```text
projet_LSystem/
├── src/
│   ├── controller/             # Contrôleurs assurant le lien entre Modèle et Vue
│   ├── model/                  # Logique métier et règles du L-Système
│   │   ├── LSystemGenerate.java
│   │   └── LSystemRuler.java
│   ├── test/                   # Tests unitaires du moteur de génération
│   │   ├── LSystemGenerateTest.java
│   │   └── LSystemRulerTest.java
│   ├── utils/                  # Classes utilitaires, calculs et patron MVC
│   │   ├── Coordonnees.java
│   │   ├── Ecoutable.java
│   │   ├── EcoutableModele.java
│   │   ├── Ecoteur.java
│   │   ├── GeneratorException.java
│   │   └── MathsUtils.java
│   └── view/                   # Interface graphique utilisateur (Java Swing)
│       ├── affichage/          # Composants de dessin (ZoneAffichage, etc.)
│       ├── dialogue/           # Fenêtres modales et boîtes de dialogue
│       ├── Application.java    # Point d'entrée de l'application Swing
│       ├── BarreOutils.java
│       ├── MenuPrincipal.java
│       ├── ParametresConfiguration.java
│       ├── UserInterface.java
│       └── ZoneAffichage.java
├── App.sh                      # Script Shell de compilation et d'exécution
└── README.md

##  Auteurs

Projet de conception logicielle réalisé par :

* **SORAÏ SERGE** 
* **Mayele Christenvie**

**LICENCE
Ce projet est sous licence libre. Sentez-vous libre de le cloner, de l'explorer et de faire pousser vos propres plantes virtuelles ! 🌿
