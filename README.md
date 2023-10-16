# Projet Elixir - Exercices

## Installation d'Elixir

Pour installer Elixir, vous pouvez utiliser un gestionnaire de packages tel que `dnf` (pour les systèmes basés sur Red Hat) en exécutant la commande suivante :

```bash
sudo dnf install elixir
```

Après l'installation, vérifiez si Elixir est correctement installé en exécutant la commande :

```bash
elixir --version
```

## Lancer un Script Elixir

Pour exécuter un script Elixir, utilisez la commande elixir suivie du nom du fichier .ex. Par exemple :

```bash
elixir <lefichier.ex>
```

## exercice 1: HELLO WORLD?

print hello world.

## exercice 2: DES MATH?

Écrivez une fonction sum_of_digits/1 qui prend un nombre entier positif en entrée et renvoie la somme de ses chiffres.

Exemple d'utilisation:
```
IO.puts MathFunctions.sum_of_digits(123)
#6
```

## exercice 3: Qui est le plus grand ???

Écrivez une fonction max_number/1 qui prend une liste de nombres en entrée et renvoie le nombre le plus élevé.

Exemple d'utilisation:
```
numbers = [12, 45, 7, 98, 23, 56, 89]
IO.puts("Le plus grand nombre est #{ListFunctions.max_number(numbers)}")
#98
```