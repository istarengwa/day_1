# Découverte de la programmation avec Ruby

Nous allons voir les bases de Ruby, un puissant langage de programmation que l'on utilisera tout au long de la formation.

## 1\. Introduction

Et voilà ! Après avoir vu les bases du code avec le front, et notamment HTML / CSS, nous allons entrer dans le vif du sujet : les langages de programmation. Un langage de programmation est une notation conventionnelle destinée à formuler des algorithmes et produire des programmes informatiques qui les appliquent. En gros tu vas demander à ton ordinateur d'exécuter des tâches. Voici un exemple de tâches qu'un langage de programmation peut exécuter :

- compter jusqu'à cent
- envoyer des emails à cent personnes
- lancer un serveur qui va renvoyer du code HTML en fonction de la demande du client
- faire un algorithme qui va sortir les cents moussaillons les plus cools de la session
- et bien d'autres

Tu as vu comment fonctionnait une page web simple, nous allons maintenant te montrer comment faire des pages web qui s'adaptent à tes utilisateurs. Ainsi, durant les prochaines semaines nous allons aller plus en profondeur dans le merveilleux univers du backend.

Cette ressource visera à t'expliquer nos choix de langages.

## 2\. Contexte et historique

Les langages de programmation furent à la base de l'informatique. Il eut fallu attendre 1993 pour que Ruby voit le jour, créé par un certain Yukihiro Matsumoto (surnommé Matz).

## 3.La ressource

### 3.1\. Pouquoi Ruby ?

L'une des questions qui revient le plus souvent (avec celle des corrigés, répondue très bientôt) est : **pourquoi Ruby à THP ?**. La question bonus est : "j'ai lu dans un article parlant d'encodage informatique que Rails ne scalait pas et qu'il était en perte de vitesse dans la hype, alors pourquoi apprendre Ruby ?".

Ce sont d'excellentes questions, et je vais y répondre dans cette ressource. Avant toute chose, il faut comprendre ce qu'est l'informatique au sens large et vous verrez que le choix d'un langage est donc une question plus épineuse que la popularité de ce dernier.

#### 3.1.1\. L'informatique

L'informatique est le traitement automatique de l'information via l'exécution de programmes informatiques par des machines. C'est à dire que vous allez faire des programmes qui vont automatiser le traitement automatique de l'information.

Vous allez voir pendant toute la semaine des programmes simples qui vous demanderont grosso-modo de "faire des boucles et incrémenter des variables". Peu importe le langage, l'informatique vous demandera toujours d'incrémenter des variables et de faire des boucles.

Au début, le plus important est donc d'apprendre à faire ceci. Une fois que tu sauras faire des boucles, il te sera très aisé de passer d'un langage à un autre : c'est toujours la même logique, seule la syntaxe change.

Donc si l'informatique est toujours pareil, pourquoi y-a-t-il autant de langages, et comment choisir un langage ?

#### 3.1.2\. Comment choisir un langage ?

Il faut voir un langage informatique comme un outil avant tout. Un outil permettant de faire du traitement automatique de l'information via l'exécution de programmes informatiques par des machines, mais un outil. Chaque outil a ses avantages et ses inconvénients, et chacun évolue pour aller plus loin dans sa philosophie.

___
** 🎨 EXEMPLE ILLUSTRÉ**

Nous pouvons comparer un langage informatique avec un outil que tu connais bien : le système d'exploitation de ton ordinateur. macOS a des avantages que Windows n'a pas, et que Linux n'a pas. Et vice-versa. Pareil pour les inconvénients. Ces derniers ont des mises à jour régulières qui améliorent certains points par exemple. Peut être que tu fais partie des gens qui aimaient l'ajout de telle fonctionnalité quand tu es passé de WIndows XP à Windows 7\. Ou alors qui pensaient que Windows 10 est nul et tu préférais Windows 7.

C'est la même chose pour un langage de programmation. Les langages répondent tous au même besoin, c'est la façon dont ils répondent qui va changer.
___

Certains langages seront plus rapides d'exécution (exemple : C). D'autres seront plus rapides à écrire (exemple : Python). D'autres seront spécialisés dans la gestion de données (exemple : SQL). Il existe plein de spécificités pour chaque langage.

Ainsi, chaque langage a ses spécificité que d'autres n'auront pas. L'une des meilleures ressources pour découvrir ceci est [Quora](https://www.quora.com/topic/Programming-Languages). Quora est un site de questions-réponses non anonymes. C'est à dire que des personnes précises vont répondre à des questions pouvant paraître innocentes. Par exemple : quelqu'un demande une question sur les arts martiaux que Jackie Chan a appris dans sa vie, puis [Jackie Chan lui-même répond](https://www.quora.com/What-martial-art-styles-does-Jackie-Chan-know).

En général, les personnes qui répondent à des questions précises sur les langages sont des professionnels ayant l'état d'esprit développeur. Ils ne choisiront pas tel langage pour sa popularité, mais pour tel avantage ou tel défaut. Ainsi, les réponses à `truc vs. machin` seront beaucoup plus fouillées que "truc est plus populaire que machin". Par exemple, [voici une fantastiques réponse](https://www.quora.com/What-is-the-difference-between-NodeJS-and-Ruby-on-Rails-based-on-real-world-experiences/answer/Osman-Ahmed-Osman) d'un ex-ingénieur de Google à la question "c'est quoi les différences entre Ruby on Rails et NodeJS".

C'est une fantastique mine d'or pour connaître des termes savants et frimer en entretien. "Après avoir découvert l'informatique avec Ruby et mis en place de prototypes ultra rapides avec Ruby on Rails, je me suis rendu compte que je préférais personnellement le côté asynchrone et ultra modulaire de NodeJS par rapport au design pattern SRP et le fort côté orienté objet de Ruby. Convention Over Configuration, c'est bien, mais un peu moins pour l'architecture microservices qui est le futur de l'informatique, à mon avis", ça claque beaucoup plus que "je code dans ce langage car c'est celui que j'ai appris dans ma formation : ils m'ont dit que je trouverais du travail et qu'il recrute".

Nous te conseillons d'être curieux et de ne pas hésiter à faire des recherches pour connaître les avantages et défauts de tel langage par rapport à tel langage. Voici des exemples de syntaxe que tu peux faire sur Google :

- `difference between [langage_1] and [langage_2] quora` : pour comparer deux langages. Voici par exemple un des résultats pour [Java vs. Ruby](https://www.quora.com/What-are-the-differences-between-java-and-ruby-as-well-as-their-web-based-counterparts-namely-JSP-vs-Rails)
- `pros and cons [langage] quora` : pour connaître rapidement un langage

Si jamais certains termes te semblent barbares dans les réponses (ex: microservice, design pattern, etc), n'hésite pas à faire des recherches (sur Quora, Google, Youtube, ou autre) sur ce qu'ils veulent dire et ainsi améliorer énormément ta culture générale sur l'informatique. En quelques recherches internet, tu auras appris suffisamment de concepts informatiques pour impressionner n’importe quel pro !
___
** 🚀 ALERTE BONNE ASTUCE**

C'est d'ailleurs une excellente question pour repérer le niveau d'un directeur technique. La prochaine fois que tu passes un entretien, je t'invite à demander à l'équipe technique pourquoi cette dernière a choisi leur langage informatique. Tu seras très souvent surpris des réponses.
___

#### 3.1.3\. Pourquoi choisir Ruby ?

Bref, pourquoi avons-nous choisi Ruby ? Nous avons choisi Ruby pour deux paramètres importants :

##### 3.1.3.1\. Syntaxe facile

Le premier est la simplicité d'utilisation du langage. Comme tu vas le voir cette semaine, tu vas te tirer les cheveux plus d'une fois sur la logique de l'informatique. Ton programme va planter car tu vas oublier des mots. Tu vas connaître toutes les étapes du deuil. C'est normal et tout le monde est passé par là.

Ruby a une syntaxe beaucoup plus permissive que n'importe quel autre langage : il a été conçu pour vouloir le bonheur du développeur et a donc une syntaxe se rapprochant à l'anglais. Ainsi, tu n'auras pas de soucis de programme qui plante car tu as oublié un `;` en fin de ligne d'un programme. Et pour être passé par là, je peux te jurer que de perdre 2 heures car tu as oublié un `;` dans ton programme est extrêmement frustrant, et l'envie de jeter ton ordinateur par la fenêtre l'emportera sur l'envie de continuer à apprendre le code.

La syntaxe bonheur de Ruby est idéale quand on débute l'informatique, et (avouons-le) très plaisante quand on est très séniors. On ne le prend pas la tête à devoir expliquer son code car ce dernier est explicite.

##### 3.1.3.2\. Prototype facile

Ruby on Rails permet de sortir des prototypes très rapidement et très facilement. L'objectif de la formation est de vous montrer qu'en 600 heures à peine, vous pouvez lancer à votre guise des projets viables. Rails permet exactement cela : il est possible de lancer un projet concret en deux semaines, là où tu serais encore avec l'authentification si tu choisissais Java par exemple.

##### 3.1.3.3.Autres

Ruby possède d'autres avantages que nous n'aborderons pas dans cette ressource. Évidemment, Ruby a des défauts. Idem, nous ne les aborderons pas ici (c'est très technique pour le moment).

En tout cas, ces avantages correspondent parfaitement à l'état d'esprit de la formation : donner les clés de la boite à outils de l'informatique pour que vous découvriez l'informatique et que vous sortiez en 12 semaines de quoi faire des projets viables.

## 4\. Points importants à retenir

Nous avons choisi Ruby pour éviter des vagues de dépression chez les moussaillons, ainsi que de vous permettre de faire un véritable site en 600 heures de projets.

## 5\. Pour aller plus loin

N'hésite pas à regarder et comprendre les forces et faiblesses des langages que tu croises !