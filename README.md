# Currency-converter — Chiffrement / Déchiffrement (Java Swing)

## Objectif du projet
Ce projet est une application Java avec interface graphique (Swing) permettant de chiffrer et déchiffrer un message texte à l’aide d’un algorithme de type chiffrement affine.

L’utilisateur peut :
- saisir un message
- définir deux paramètres numériques A et B
- chiffrer ou déchiffrer le message
- afficher le résultat dans l’interface graphique

---

## Description générale
L’application repose sur :
- une interface graphique développée avec Java Swing
- un alphabet prédéfini sous forme de tableau de caractères
- une transformation mathématique appliquée à chaque caractère du message

Le programme utilise une fonction affine pour transformer les indices des caractères dans l’alphabet.

---

## Principe du chiffrement
Chaque caractère du message est associé à un index `j` dans un tableau de caractères.

La formule de chiffrement est :

(j × A + B) mod 62

L’index obtenu permet de récupérer le caractère chiffré dans le tableau.

---

## Principe du déchiffrement
Le déchiffrement tente d’inverser la transformation affine en utilisant les mêmes paramètres A et B.

Attention : la méthode de déchiffrement implémentée dans le code actuel est incomplète et peut produire des résultats incorrects. Une version correcte nécessiterait le calcul de l’inverse modulaire de A.

---

## Fonctionnalités
- Interface graphique Swing
- Champ de saisie pour le message original
- Champ d’affichage du message chiffré ou déchiffré
- Paramètres A et B configurables
- Bouton de chiffrement
- Bouton de déchiffrement
- Bouton pour effacer les champs

---

## Prérequis
- Java JDK 8 ou supérieur
- Un environnement de développement Java (Eclipse, IntelliJ IDEA, NetBeans)
- Aucun framework externe requis

---

## Structure du projet
src/
└── projet/
    └── convertir.java

---

## Exécution du projet

### Depuis un IDE
1. Créer un projet Java
2. Ajouter le fichier `convertir.java` dans le package `projet`
3. Lancer la classe `convertir` (méthode main)

### Depuis le terminal
javac -d out src/projet/convertir.java  
java -cp out projet.convertir

---

## Utilisation
1. Entrer un message dans le champ principal
2. Saisir les valeurs A et B
3. Cliquer sur :
   - "chifrer" pour encoder le message
   - "dechifrer" pour tenter de le décoder
4. Cliquer sur "effacer" pour réinitialiser les champs

---

## Limitations connues
- Le modulo utilisé est fixé à 62 alors que l’alphabet contient plus de caractères
- Le déchiffrement n’est pas mathématiquement fiable
- L’interface graphique ne définit pas explicitement de LayoutManager
- Aucune validation des entrées utilisateur

---

## Améliorations possibles
- Utiliser table.length au lieu de 62
- Implémenter l’inverse modulaire de A
- Ajouter des contrôles de saisie
- Séparer la logique de chiffrement de l’interface graphique
- Améliorer l’ergonomie de l’interface
- Ajouter des tests unitaires

---

## Auteur
Adem
