# Découverte de la programmation avec Ruby

Et bien c'est parti, on commence la programmation ! Nous allons voir les concepts de base quand on programme.

## 1\. Introduction

Dans cette ressource, nous allons te montrer les bases de la programmation avec Ruby. Tu verras comment créer un programme, comment déclarer tes premières variables, et quelques types de données de base. À la fin tu auras les armes pour attaquer les programmes d'aujourd'hui.

Ce qui est amusant (ou pas), c'est qu'en soit, la quantité d'information que tu va avoir sera assez légère, et la façon dont tu joueras avec ces informations te mettra en PLS pour les prochains jours. C'est le principe de l'informatique : c'est pas facile quand on débute, et tout le monde a été grand débutant, surtout toi. Donc ouais ça ne sera pas facile.

## 2\. Contexte et historique

Ruby a été créé en 1995 par un certain Yukihiro Matsumoto (Matz, pour les intimes) avec pour le but d'améliorer le bonheur des développeurs. Il a une syntaxe simple qui facilite l'écriture de code.

Voici les particularités

- il propose des solutions plus faciles à mettre en place
- syntaxe agréable
- langage simple mais puissant (on peut faire quasiment tout avec Ruby)

Ruby a aussi une forte communauté bienveillante qui fait beaucoup de programmes open source qui vont faciliter ta vie. Ces programmes s'appellent les gems. La plus célèbre d'entre elle est Ruby on Rails, qui permet de faire des sites web très rapidement.

Ces particularités en font un langage idéal pour découvrir l'univers de l'informatique

## 3\. La ressource

### 3.0\. Ruby bien installé ?

Pour faire cet exercice, Ruby doit bien être installé sur ton ordinateur, c'est à dire que l'installfest s'est déroulé à merveille.

### 3.1\. Ton premier programme

#### 3.1.1\. First program

Bon, est-ce qu'on lance notre premier programme ? As-tu le coeur plein d'émotion ? Lorsque j'ai lancé mon premier programme j'étais comme un petit fou sur mon ordinateur :') Bref, mets-toi dans un dossier que tu garderas pour la postérité puis créé un fichier qui s'appelle `my_first_program.rb`.

___
** 🚀 ALERTE BONNE ASTUCE**

Les fichiers écrits en html sont à l'extension `.html`. Les fichiers css en `.css`. Pour Ruby, c'est `.rb`
___

Écris dans ce programme les lignes suivantes :
```ruby
puts "Bonjour, monde !"
```

Puis lance le programme à partir de ton terminal :
```ruby
$ ruby my_first_program.rb
```

En effet, pour lancer un programme ruby, il faut faire `ruby nom_du_programme.rb` Si tu as tout bien fait, tu devrais avoir un terminal qui dit bonjour :) Alors, ça t'a fait quoi ? Avoue, c'est la classe ;)

___
** ⚠️ ALERTE ERREUR COMMUNE**

ALERTE ! J'ai cette erreur :
```ruby
$ ruby my_first_program.rb
Traceback (most recent call last):
ruby: No such file or directory -- my_first_program.rb (LoadError)
```

En effet, en faisant `ruby machin.rb`, tu dis à ton ordinateur "hey ! Exécute le fichier suivant en ruby". Il faut donc qu'il sache quel programme exécuter. Soit tu dois faire plein de `cd dossier_1/THP/je_ne_connais_pas_le_chemin` pour être dans le bon dossier, soit tu fais directement `ruby dossier_1/THP/je_ne_connais_pas_le_chemin/my_first_program.rb` pour exécuter le programme.
___

Maintenant essaie de changer le programme pour que ce dernier ne dise pas "Bonjour, monde !", mais "Hello, world !".

#### 3.1.2\. Programmes

Créé d'autres fichiers qui contiennent les lignes suivantes :
```ruby
# my_second_program.rb
puts "Bonjour, monde !"
puts "Je le redis une seconde fois : Bonjour, monde !"
puts "C'est cool de parler, allez, je m'en vais !"
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)
```ruby
# my_third_program.rb
10.times do
  puts "Bonjour, monde !"
end
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)
```ruby
# my_fourth_program.rb
print "Bonjour, monde !"
print "Je le redis une seconde fois : Bonjour, monde !"
print "C'est cool de parler, allez, je m'en vais !"
```

D'après-toi, quelle est la différence entre `puts` et `print` ? Exécute le programme et vérifie ;)
```ruby
# my_fifth_program.rb
puts "Salut encore !"
# Ceci est une de commentaire ?
puts "Ceci est une autre ligne, mais elle n'est pas en commentaire !"
# Une autre ligne de commentaire !
```

D'après-toi, que fait le symbole `#` ? Exécute le programme et vérifie ;)
```ruby
# my_sixth_program.rb
# Allez, un autre programme !
# Coucou !
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie. Pourquoi d'après toi le programme ne renvoie rien ?
```ruby
# my_seventh_program.rb
hello_string = "Bonjour, monde !"
puts hello_string
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie.
```ruby
# my_eigth_program.rb
puts 3
puts 2 + 1
puts 3 * 2
puts 3 - 1
puts 6 * 2
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie.
```ruby
# my_ninth_program.rb
birth_year = 1995
if birth_year == 1995
  puts "Cette personne est néée en 1995 !"
end
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie.

Bon, nous nous sommes bien amusés ! Passons maintenant à la suite !

### 3.2\. Les variables

La notion de variable est fondamentale en informatique. Si tu comptes te reconvertir en informatique, tu passeras ta future carrière à jouer avec des variables. Qu'est-ce qu'une variable ? Vois cela comme une boite qui contient de l'information. Cette boite aura deux caractéristiques : un nom, et ce qu'elle contient.

Prenons par exemple le programme suivant :
```ruby
# variable examples
hello_string = "Hello, world !"
simple_integer = 3
hello_string_in_french = "Bonjour, monde !"
a = "a"
```

Dans ce mini programme (qui n'affichera rien), nous avons fait quatre choses :

- Nous avons déclaré une variable `hello_string` et lui avons assigné la valeur `"Hello, world !"`
- Nous avons déclaré une variable `simple_integer` et lui avons assigné la valeur `3`
- Nous avons déclaré une variable `hello_string_in_french` et lui avons assigné la valeur `"Bonjour, monde !"`
- Nous avons déclaré une variable `a` et lui avons assigné la valeur `"a"`

Les variables marchent comme ça. On les déclare et on leur assigne ce qu'elle contient. On fait des programmes exemples ?
```ruby
# variables_01.rb
hello_string = "Hello, world !"
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie. Essaie de deviner pourquoi le programme ne renvoie rien ?
```ruby
# variables_02.rb
hello_string = "Hello, world !"
puts hello_string
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)
```ruby
# variables_03.rb
hello_word = "Hello"
world_word = "world"
puts hello_word + world_word
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)
```ruby
# variables_03.rb
hello_word = "Hello"
world_word = "world"
hello_string = hello_word + world_word
puts hello_string
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)

Tu vois les bases des variables, passons à la suite !

### 3.3\. Les types de données simples

Encore un concept fondamental dans l'informatique : les types de données. Les types de données sont grosso-modo ce que tu vas mettre dans les variables. Pour le moment tu en as vu un seul type : les _string_. Un string est une suite de caractères, par exemple `"Bonjour, monde !"` est un string. Un string sera toujours entre guillemets anglais (`"`) ou apostrophes (`'`).

Voici quelques autres types de données :

- **integer** : ce sont des nombres entiers (`2`, `0`, `23972` ou `-3` sont des integer)
- **float** : ce sont des nombres réels, généralement écrits avec un point (`3.14`, `2.5`, `4.0` sont des floats)
- **booléen** : ils deux valeurs : `true` ou `false`.

Voici les types de données de base.

En général les string servent à noter des chaines de caractères (tout ce qui est phrase, mots, lettres). Tu t'en serviras beaucoup.

Les integer sont très pratiques : en effet, c'est le type de données qui te permet de mettre un nombre précis sur une action. Par exemple tu ne vas pas envoyer `2.3984` emails à un utilisateur. Tu t'en serviras énormément.

Les booléens permettent de mettre des conditions : si ceci est vrai, fais cela, sinon, fais cela. Tu t'en serviras beaucoup.

Enfin, les float servent en général pour les opérations mathématiques, ou la physique (soit pas souvent).

Testons tout cela !
```ruby
# data_types_01.rb
one = 1
two = 2
puts one + two
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;) Et oui, il est possible de faire des opérations de base avec des integer. Heureusement, pas besoin d'être un crack en maths, étant donné que l'ordinateur fera tous les calculs à ta place !
```ruby
# data_types_02.rb
two = 2
three = 3
puts two * three
puts three - two
puts 3 - 2
puts three - 2
puts 3 - two
puts 2 - 3
puts two - 3
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)
```ruby
# data_types_03.rb
truthy = true
puts truthy
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)
```ruby
# data_types_04.rb
float_1 = 1.5
float_2 = 2.5
puts float_1 + float_2
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)
```ruby
# data_types_05.rb
two_in_integer = 2
two_in_string = "2"
puts two_in_integer + two_in_string
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;) Maintenant essaie de comprendre ce qui ne va pas. N'hésite pas à utiliser Google.

### 3.5\. Le contrôle du flux

Encore une notion fondamentale dans l'informatique (décidément !) : le contrôle du flux. Ton programme va suivre un flux. Il va exécuter d'abord la ligne 1 de ton fichier, ensuite la ligne 2, ensuite la ligne 3, jusqu'à arriver à la dernière ligne. Cool, mais si jamais tu veux dire "si jamais il se passe si, fais cela", tu te retrouves bloqué. Et bien grâce au contrôle de flux, c'est possible !

Le contrôle de flux permet de dire à ton programme "si jamais ceci est vrai, fais cela". Ce va s'écrire comme ça :
```ruby
# conditions_01.rb
# on déclare un age qui est égal à 21
age = 21

# vérifie que l'age est bien strictement supérieur à 17 (=> qu'il soit égal à 18 ou plus)
if age > 17
  # si cela arrive, on écrit une phrase cool
  puts "Cette personne est majeure !"
end

# vérifie que l'age est égal à 21
if age == 21
  puts "Cette personne a 21 ans !"
end
```

Bon alors, que va faire ce programme ?

Comme tu peux le voir, notre ami Ruby est assez clair dans sa syntaxe. Nombreux sont les langages qui t'imposent de bien mettre les bonnes choses entre parenthèse, ou `{ }`. Déjà que ton cerveau fume, imagine ce que ce serait si jamais tu devais mettre ton code entre crochets 🤯

___
** 🤓 QUESTION RÉCURRENTE**

**Mais dis-donc Jamy, dans le programme je vois deux signes égal `==` alors que dans un autre programme il n'y en a qu'un seul**

C'est une excellente question. Deux signe égal veut dire que tu compares deux éléments. S'ils sont égaux, cela te renverra `true`, sinon `false`. Par exemple `12 == 13` te renverra `false`.

Un seul signe égal veut dire que tu assignes une valeur à une variable. C'est à dire que "la variable untel devient le type de données truc". Par exemple `number = 3` veut dire "la variable `number` devient l'integer `3`".

Pour t'en souvenir, utilise ce moyen mnémotechnique de ma création : Le signe égal, quand y'en a un, c'est que ta variable devient. Le signe égal, quand y'en a deux, vrai ou faux, c'est l'heure de ce petit jeu.
___

Perso, j'aime bien [cette page](https://launchschool.com/books/ruby/read/flow_control) de Launchschool qui te montre les diverses notions du contrôle de flux en Ruby.

### 3.4\. Les boucles

Bon allez, dernière notion pour la journée et on passe au projet. Alors celle là est fondamentale (pour changer) : les boucles.

En gros, grâce aux boucles, tu vas répéter une action de ton programme. On voit avec des exemples ?
```ruby
# loops_01.rb
puts "Bonjour, monde !"
puts "Bonjour, monde !"
puts "Bonjour, monde !"
puts "Bonjour, monde !"
puts "Bonjour, monde !"
puts "Ok, c'est cool, mais testons avec une nouvelle méthode."
5.times do
  puts "Bonjour, monde !"
end
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)

Jusqu'ici, tout va bien : une boucle permet de boucler. Maintenant introduisons LA notion qui fait perdre des cheveux aux moussaillons, la notion de variable incrémenteuse.
```ruby
# loops_02.rb
5.times do |index|
  puts index
end

5.times do |you_can_chose_any_name|
  puts you_can_chose_any_name
end

5.times do |i|
  puts i
end
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;) Comme tu peux le voir, le programme commence à compter à 0\. C'est une norme en informatique.
```ruby
# loops_03.rb
5.times do |i|
  puts i + 1
end
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)
```ruby
# loops_04.rb
5.times do |i|
  puts "=== Boucle n°#{i} ==="
  5.times do |j|
    puts j
  end 
end
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)
```ruby
# loops_05.rb
5.times do |i|
  puts "=== Boucle n°#{i} ==="
  i.times do |j|
    puts j
  end 
end
```

D'après-toi, que va faire ce programme ? Exécute-le et vérifie ;)

## 4\. Points importants à retenir

Pfiou, c'est une ressource intense. Il y a beaucoup de choses à retenir, mais nous te conseillons la pratique. Attaque le projet du jour.

## 5\. Pour aller plus loin

Je t'invite à attaquer le projet du jour.