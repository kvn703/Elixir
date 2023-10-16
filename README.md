# WORKSHOP Elixir

## Introduction

Elixir est un langage de programmation fonctionnel, concurrent, orienté objet. Il a été créé par José Valim en 2011 et est utilisé par des sociétés telles que Pinterest, Moz, Discord, Bleacher Report, The Outline, Inverse et plus encore.

Pour en savoir plus sur Elixir, consultez le site officiel d'Elixir : https://elixir-lang.org/

## Installation d'Elixir

Pour installer Elixir, vous pouvez utiliser un gestionnaire de packages tel que `dnf` (pour les systèmes basés sur Red Hat) en exécutant la commande suivante :

```bash
sudo dnf install elixir
```

Après l'installation, vérifiez si Elixir est correctement installé en exécutant la commande :

```bash
elixir --version
```

Pour installer Elixir sur d'autres systèmes d'exploitation, consultez la page d'installation officielle d'Elixir : https://elixir-lang.org/install.html

## Sommaire

Durant ce workshop, nous allons faire une serie d'exercice simple pour apprendre les bases du langage Elixir.

Ensuite, nous allons faire un projet simple pour mettre en pratique ce que nous avons appris.

# Step 1 : Les bases

## Lancer un Script Elixir

Pour exécuter un script Elixir, utilisez la commande elixir suivie du nom du fichier .ex. Par exemple :

```bash
elixir <lefichier.ex>
```

## exercice 1: HELLO WORLD?

affiche un hello world.

## exercice 2: DES MATH?

Écrivez une fonction `sum_of_digits` qui prend un nombre entier positif en entrée et renvoie la somme de ses chiffres.

Exemple d'utilisation:

```
IO.puts("La somme des chiffres de 123 est #{MathFunctions.sum_of_digits(123)}")
#6
```

## exercice 3: Qui est le plus grand ???

Écrivez une fonction `max_number` qui prend une liste de nombres en entrée et renvoie le nombre le plus élevé.

Exemple d'utilisation:

```
numbers = [12, 45, 7, 98, 23, 56, 89]
IO.puts("Le plus grand nombre est #{ListFunctions.max_number(numbers)}")
#98
```

## exercice 4: Palinquoi?

Écrivez une fonction `is_palindrome` qui prend une chaîne de caractères en entrée et renvoie true si elle est un palindrome, sinon false.

Exemple d'utilisation:

```
input_string = "A man, a plan, a canal, Panama"
if StringFunctions.is_palindrome(input_string) do
  IO.puts("La chaîne est un palindrome.")
else
  IO.puts("La chaîne n'est pas un palindrome.")
end
#Palindrome

input_string = "Elixir is fun"
if StringFunctions.is_palindrome(input_string) do
  IO.puts("La chaîne est un palindrome.")
else
  IO.puts("La chaîne n'est pas un palindrome.")
end
#pas Palindrome
```

## exercice 5: Manipulation de List.

Nous allons maintenant apprendre à manipuler les listes en Elixir.