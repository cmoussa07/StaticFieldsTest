# Exercice 6 : Tester les Champs Static

## Objectif
Ce projet est une application Java qui illustre la différence entre un attribut **static** et un attribut **non-static** en POO.
Il utilise une classe `Personne` avec deux compteurs pour observer leur comportement lors de la création de plusieurs instances.

---

## Structure du projet

- `Personne.java` : classe contenant un compteur static partagé entre toutes les instances et un compteur non-static propre à chaque instance.
- `Main.java` : classe principale qui crée plusieurs instances de `Personne` et affiche les valeurs des deux compteurs.

---

## Prérequis

- Java JDK 21
- IntelliJ IDEA (ou tout autre IDE compatible)
- Git installé sur votre machine

---

## Installation et exécution

- Clonez le dépôt :
```bash
git clone https://github.com/cmoussa07/StaticFieldsTest.git
```
- Ouvrez le projet dans IntelliJ IDEA.
- Vérifiez que le JDK est bien configuré sur la version 21.
- Lancez la classe `Main`.

---

## Fonctionnement

- Le programme crée 4 instances de la classe `Personne`.
- À chaque création, les deux compteurs sont incrémentés dans le constructeur.
- `nbInstances` (static) s'accumule à chaque nouvelle instance car il est partagé entre tous les objets.
- `nbLocal` (non-static) repart de 0 à chaque nouvelle instance, donc vaut toujours 1.

---

## Résultat attendu

```
(1,4)
```

- `1` correspond à `nbLocal` de `personne4` — repart de 0 à chaque instance.
- `4` correspond à `nbInstances` — s'accumule pour toutes les instances créées.

---

## Concepts illustrés

- **Attribut static** : une seule copie en mémoire partagée par tous les objets de la classe.
- **Attribut non-static** : chaque objet possède sa propre copie indépendante.
- **Constructeur** : utilisé pour incrémenter les deux compteurs à chaque création d'objet.
