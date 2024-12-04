# Bowling multi-joueurs

### [Voir la solution](./Solution.md)

## Enoncé
À partir de la [correction de l'exercice "Bowling"](https://github.com/bastide/BowlingMavenCorrection), implémentez l'interface `IPartieMultiJoueurs` et testez votre implémentation.

Voir le javadoc pour le comportement attendu des méthodes.

Vous devez vous approcher d'une couverture de tests de 100 % pour votre implémentation.

### Exemple de déroulement d'une partie
```java
IPartieMultiJoueurs partie = new PartieMultiJoueurs();
partie.demarreNouvellePartie({"Pierre", "Paul"});
// ➜ String "Prochain tir : joueur Pierre, tour n° 1, boule n° 1"
partie.enregistreLancer(5);
// ➜ String "Prochain tir : joueur Pierre, tour n° 1, boule n° 2"
partie.enregistreLancer(3);
//➜ String "Prochain tir : joueur Paul, tour n° 1, boule n° 1"
partie.enregistreLancer(10);
// ➜ String "Prochain tir : joueur Pierre, tour n° 2, boule n° 1"
partie.enregistreLancer(7);
// ➜ String "Prochain tir : joueur Pierre, tour n° 2, boule n° 2"
partie.enregistreLancer(3);
// ➜ String "Prochain tir : joueur Paul, tour n° 2, boule n° 1"
partie.scorePour("Pierre");
// ➜ int 18
partie.scorePour("Paul");
// ➜ int 10
partie.scorePour("Jacques");
// ➜ IllegalArgumentException : "Joueur inconnu"
```