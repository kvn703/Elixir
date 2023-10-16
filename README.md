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

### 5.1: Manipulation de List.

Écrivez une fonction `even_numbers` qui prend en entrée une liste d'entiers et renvoie une nouvelle liste contenant uniquement les nombres pairs de la liste d'entrée.

Main pour tester:

```
defmodule Main do
  def run do
    list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
    even_numbers = MathFunctions.even_numbers(list)
    IO.puts("Nombres pairs : #{inspect(even_numbers)}")
  end
end

Main.run()
```

### 5.2: Manipulation de List.

Écrivez une fonction `sum_of_list` qui prend en entrée une liste d'entiers et renvoie la somme de tous les nombres de la liste.

Main pour tester:

```
defmodule Main do
  def run do
    list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
    sum = MathFunctions.sum_of_list(list)
    IO.puts("Somme de la liste : #{sum}")
  end
end

Main.run()
```

### 5.3: Manipulation de List.

Écrivez une fonction `unique_elements` qui prend en entrée une liste d'entiers et renvoie une nouvelle liste contenant uniquement les éléments uniques de la liste d'entrée.

Main pour tester:

```
defmodule Main do
  def run do
    list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 1, 2, 3]
    unique_elements = MathFunctions.unique_elements(list)
    IO.puts("Éléments uniques : #{inspect(unique_elements)}")
  end
end

Main.run()
```

### 5.4: Manipulation de List.

Écrivez une fonction `string_to_list` qui prend en entrée une chaîne de caractères et renvoie une liste contenant tous les caractères de la chaîne.

Main pour tester:

```
defmodule Main do
  def run do
    string = "Hello World!"
    list = StringFunctions.string_to_list(string)
    IO.puts("Liste : #{inspect(list)}")
  end
end

Main.run()
```

### 5.5: Manipulation de List.

Écrivez une fonction `sort_list` qui prend en entrée une liste d'entiers et renvoie une nouvelle liste contenant les éléments de la liste d'entrée triés par ordre croissant.

Main pour tester:

```
defmodule Main do
  def run do
    list = [9, 8, 7, 6, 5, 4, 3, 2, 1]
    sorted_list = ListFunctions.sort_list(list)
    IO.puts("Liste triée : #{inspect(sorted_list)}")
  end
end

Main.run()
```

## exercice 6: Manipulation de Map.

Nous allons maintenant apprendre à manipuler les maps en Elixir.

### 6.1: Creation de Map.

Écrivez une fonction create_map qui prend en entrée une liste d'entiers et renvoie une nouvelle map contenant des champs nom, prénom, âge et l'id.

### 6.2: Manipulation de Map.

Écrivez une fonction get_value qui prend en entrée une map et une clé et renvoie la valeur correspondante.

Main pour tester:

```
defmodule Main do
  def run do
    map = %{"a" => 1, "b" => 2, "c" => 3}
    value = MapFunctions.get_value(map, "b")
    IO.puts("Valeur : #{value}")
  end
end

Main.run()
```

### 6.3: Manipulation de Map.

Écrivez une fonction `get_keys` qui prend en entrée une map et renvoie une liste contenant toutes les clés de la map.

Main pour tester:

```
defmodule Main do
  def run do
    map = %{"a" => 1, "b" => 2, "c" => 3}
    keys = MapFunctions.get_keys(map)
    IO.puts("Clés : #{inspect(keys)}")
  end
end

Main.run()
```

## exercice 7 : Manipulation de fichier.

Nous allons maintenant apprendre à manipuler les fichiers en Elixir.

Pour cette partie, veuillez créer un fichier `sample.txt` pour faire vos tests.

### 7.1: Lire le fichier.

Écrivez une fonction `read_file` qui prend en entrée le nom d'un fichier et renvoie son contenu.

Main pour tester:

```
defmodule Main do
  def run do
    content = FileFunctions.read_file("sample.txt")
    IO.puts("Contenu : #{content}")
  end
end

Main.run()
```

### 7.2: Ecrire dans le fichier.

Écrivez une fonction `write_file` qui prend en entrée le nom d'un fichier et son contenu et écrit le contenu dans le fichier.

Main pour tester:

```

defmodule Main do
  def run do
    FileFunctions.write_file("sample.txt", "Hello World!")
  end
end

Main.run()
```

### 7.3: Stocker le contenu du fichier dans une liste.

Écrivez une fonction `read_file_to_list` qui prend en entrée le nom d'un fichier et renvoie son contenu sous forme de liste. Et ensuite avec la fonction `sort_list` triez la liste et écrivez le contenu dans un nouveau fichier `sorted.txt`.

# Step 2 : Petit projet

Après avoir appris les bases du langage Elixir, nous allons maintenant faire un petit projet pour mettre en pratique ce que nous avons appris.

### But du projet

Le but de ce projet est de créer un programme qui permet de gérer une liste de tâches.

### Fonctionnalités

- Ajouter une tâche

- Supprimer une tâche

- Afficher la liste des tâches

- Sauvegarder la liste des tâches dans un fichier

- Charger la liste des tâches depuis un fichier

Aucune interface graphique n'est nécessaire, le programme peut être exécuté en ligne de commande.

Je vous invite fortement à utiliser les fonctions que vous avez créés dans les exercices précédents.

A vous de jouer !