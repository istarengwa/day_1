# Une série d'exercices en Ruby

Tu vas faire une série d'exercices qui vont se conclure par une très célèbre pyramide.

## 1\. Présentations

Ces exercices seront différents de ce que tu as pu voir jusqu'à présent. Nous entrons dans le vif du sujet de la programmation, avec des exercices qui te feront jouer avec des notions de programmation : variables, arrays, etc..

Tous ces programmes paraitront assez abstraits, et c'est normal. J'aimerais vous donner des exercices du genre "écris un programme qui va envoyer un message à une liste de 100 emails"; mais le soucis est que cela implique de connaître à la perfection les notions de boucles, de type de données, etc. Si tu ne sais pas boucler un programme pour qu'il compte jusqu'à 10, eh bien lui faire envoyer 100 emails sera très compliqué 😉

Ainsi, nous allons te donner une liste d'exercices qui vont te faire jouer avec les boucles et autre joyeusetés du genre. Ce sont des notions communes à TOUS les langages de programmation, et une logique à acquérir. Au début cela fera –un peu– mal à la tête, mais cela viendra naturellement à force d'en faire. L'autre bonne nouvelle est que c'est un peu comme le vélo : cela ne s'oublie pas. Je me souviens avoir galéré pendant des heures sur la [pyramide de Mario de CS50](https://docs.cs50.net/problems/mario/less/mario.html), pour au final la refaire en 20mn à peine un an après, sans avoir touché de code entre temps !

### 1.1\. État d'esprit

L'état d'esprit est à la débrouille. Nous te donnons plein d'exercices, et tu dois les résoudre à la suite. Certains te paraitront étrangement simples, d'autres te feront te tirer les cheveux.

Le but est de progresser. Si tu n'arrives pas à faire un exercice, passe au suivant, et vois si tu arrives à le faire. L'exercice final te demandera de mettre en pratique tout ce que tu auras vu lors des exercices précédents, et t'apprendra même à poser un problème pour mieux le résoudre.

Pour chaque programme, il y a plein de solutions différentes. Ici, nous ne jugerons pas la beauté du code, mais s'il marche ou non. L'élégance du code vient avec l'expérience 😉

### 1.2\. Les erreurs

Si tu as une erreur, ceci apparaitra :
```ruby
$ ruby hello.rb
hello.rb:1: unterminated string meets end of file
```

Il est indispensable que tu saches lire ce type d'erreurs, puisque tu vas en faire plein. Même moi il m'arrive de faire ces erreurs.

Ces lignes indiquent :
```ruby
$ ruby hello.rb
```

-> Tu as lancé le programme `hello.rb`
```ruby
hello.rb:1: unterminated string meets end of file
```

-> Le programme `hello.rb` a eu l'erreur suivante ligne 1 "unterminated string meets end of file". Cela veut dire qu'un string non fini a _rencontré une fin de ligne_. C'est assez cryptique aux premiers abords, mais tu as 1️⃣ la localisation de ton erreur 2️⃣ un ordre de grandeur qui t'indique grosso modo une erreur en rapport avec un string et une fin de ligne. La première chose à faire est d'aller dans ton programme, ligne 1\. Le programme ressemble à ceci :
```ruby
puts "Bonjour monde !
```

🤔 Il n'aime pas cette ligne. Et finalement après quelque temps, tu remarques qu'il manque le `"` fermant ton string. Tu l'ajoutes, relances le programme, et ça marche, miracle !

Si lire des erreurs au début peut te paraitre un peu barbare, cela sera rapidement une seconde nature. Comme dit précédemment, de même que tous les développeurs, tu en feras toute ta vie des erreurs, donc bien savoir les lire est indispensable à l'univers du code.

### 1.3\. Savoir rechercher ce que l'on veut

Tout bon développeur qui se respecte le dira : savoir rechercher l'information est indispensable quand on fait des programmes informatiques. Que ce soit pour trouver la bonne fonction qui gère notre programme ou bien trouver la réponse à l'erreur incompréhensible sortie par Ruby.

Prenons l'exemple de notre erreur ci-haut, qui était "unterminated string meets end of file", une recherche Google avec `ruby unterminated string meets end of file` te donnera [la réponse](https://www.codecademy.com/en/forum_questions/51d7d46b8c1ccc26dc028425) en quelques résultats à peine.

___
** 🚀 ALERTE BONNE ASTUCE**

L'univers du code est anglophone, donc il y aura 50 fois plus de résultats en anglais qu'en français. Ainsi, mets dès aujourd'hui ton terminal en anglais afin de pouvoir copier-coller l'erreur en anglais. Ce sera plus simple pour toi de trouver la solution.
___

## 2\. Les exercices

Voici ce qui va se passer pour cet exercice : pour chaque sous-partie, nous allons te demander de créer un programme, et de soit répondre à des questions, soit de le faire marcher.

Nous te conseillons de tout mettre dans un joli repo Git, afin que tu t'entraines avec le programme de versionning.

### 2.1\. Bonjour monde

Créé un programme `exo_01.rb` qui affiche "Bonjour, monde !". Voici les lignes qu'il doit avoir d'affichées lorsque tu l'exécutes :
```ruby
$ ruby exo_01.rb
Bonjour, monde !
```

### 2.2\. Bonjours, monde

Créé un programme `exo_02.rb` qui affiche les lignes suivantes :
```ruby
$ ruby exo_02.rb
Bonjour, monde !
Et avec une voix sexy, ça donne : Bonjour, monde !
```

En faisant une recherche Google, peux-tu connaître la différence entre `print` et `puts` ?

### 2.3\. Il ne dit pas bonjour

Reprends ton programme `exo_02.rb`, puis écris un programme `exo_03.rb` qui est le même, mais avec `#` devant la ligne 2\. Peux-tu me dire ce qu'il se passe ?

### 2.4\. Ça marche pô 😢

Créé un programme `exo_04.rb` avec les lignes suivantes :
```ruby
puts "Salut, ça farte ?
```

Lance le programme. Que se passe-t-il ? Pourquoi ?

### 2.5\. Opérations

Écris un programme `exo_05.rb` avec les lignes suivantes :
```ruby
puts "On va compter le nombre d'heures de travail à THP"
puts "Travail : #{10 * 5 * 11}"
puts "En minutes ça fait : #{10 * 5 * 11 * 60}"

puts "Et en secondes ?"

puts 10 * 5 * 11 * 60 * 60

puts "Est-ce que c'est vrai que 3 + 2 < 5 - 7 ?"

puts 3 + 2 < 5 - 7

puts "Ça fait combien 3 + 2 ? #{3 + 2}"
puts "Ça fait combien 5 - 7 ? #{5 - 7}"

puts "Ok, c'est faux alors !"

puts "C'est drôle ça, faisons-en plus :"

puts "Est-ce que 5 est plus grand que -2 ? #{5 > -2}"
puts "Est-ce que 5 est supérieur ou égal à -2 ? #{5 >= -2}"
puts "Est-ce que 5 est inférieur ou égal à -2 ? #{5 <= -2}"
```

D'abord, que fait `#{}` ? Ensuite, mets un commentaire devant chacune des lignes et explique ce qu'elle fait.

### 2.6\. Variables

Écris un programme `exo_06.rb` avec les lignes suivantes :
```ruby
number_of_hours_worked_per_day = 10
number_of_days_worked_per_week = 5
number_of_weeks_in_THP = 11

puts "Travail : #{number_of_hours_worked_per_day * number_of_days_worked_per_week * number_of_weeks_in_THP}"
```

Lance-le programme, et essaie de le comprendre.

Ajoute après la ligne suivante :
```ruby
puts "Et en minutes ça fait : #{number_of_minutes_in_an_hour * number_of_hours_worked_per_day * number_of_days_worked_per_week * number_of_weeks_in_THP}"
```

Lance-le programme. Que se passe-t-il ? Peux-tu l'expliquer ?

Astuce : même si ton programme affiche une interface en français (les puts), les variables doivent avoir des noms en anglais, afin d'éviter un franglais bizarre. Même si Marc utilise dans son cours des noms de variables en français, je pense que lui-même doit interdire ceci à Drivy et imposer des noms de variables anglais 😉

### 2.7\. Demander à l'utilisateur

Écris un programme `exo_07_a.rb` avec les lignes suivantes :
```ruby
puts "Bonjour, c'est quoi ton blase ?"
user_name = gets.chomp
puts user_name
```

Peux-tu me dire ce que fais `gets.chomp` ?

Après, écris un programme `exo_07_b.rb` avec les lignes suivantes :
```ruby
puts "Bonjour, c'est quoi ton blase ?"
print "> "
user_name = gets.chomp
puts user_name
```

Enfin, écris un programme `exo_07_c.rb` avec les lignes suivantes :
```ruby
user_name = gets.chomp
puts user_name
```

Quelles sont les différences entre les trois programmes ?

### 2.8\. Un programme qui dit bonjour

Écris un programme `exo_08.rb` qui demande le prénom de l'utilisateur, et qui salue l'utilisateur avec "Bonjour, _prénom_ !"

### 2.9\. Un programme qui dit bonjour de manière complète

Écris un programme `exo_09.rb` qui demande le prénom de l'utilisateur, qui lui demande après son nom de famille, et qui salue l'utilisateur avec "Bonjour, prénom nom !"

### 2.10\. Un programme qui calcule des âges

Écris un programme `exo_10.rb` qui demande son année de naissance à l'utilisateur, puis qui ressort l'âge que l'utilisateur a eu en 2017.

### 2.11\. Un programme qui répète

Écris un programme `exo_11.rb` qui demande un nombre à l'utilisateur, puis qui écrit autant de fois "Salut, ça farte ?"

### 2.12\. Compter

Écris un programme `exo_12.rb` qui demande un nombre à l'utilisateur, puis qui compte jusqu'à ce nombre.

## 3\. Rendu attendu

Le rendu attendu est un repository GitHub qui contient tous les exercices de cette journée.