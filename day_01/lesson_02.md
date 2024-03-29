# Git / Github

Dans ce cours, tu vas comprendre ce que c'est que Git, Github, et pouvoir t'en servir avec brio \o/

## 1\. Introduction

Tu as vu Git et Github lors de la semaine 1, ce qui t'a permis de faire tes premiers commit et uploader en ligne tes premiers repo. C'est super, mais j'imagine que cet univers reste encore un peu flou et que tu ne te sens pas encore à l'aise avec Git et GitHub. Et bien voilà tout l'intérêt de cette ressource, qui va te redonner des bases solides sur lesquelles tu vas pouvoir construire une chouette formation.

___
**🤓 PETITS RAPPELS**

**Le dictionnaire de Git**

**Un repo** = repository = un dossier sur ton ordinateur qui contient du code.  
**Un commit** = une sauvegarde d'un dossier (ou repo) via Git. sauve tout le code contient tout le code de tous fichiers du dossier tel que écrit au moment de la sauvegarde.

**Quelle différence entre Git et GitHub?**

**Git** est un programme installé sur ton ordinateur. Il permet de générer des sauvegardes (commits) de l'état de ton code et de garder ces sauvegardes pour y revenir plus tard, si besoin

**GitHub** par contre est un site web tiers fournissant un service pour héberger en ligne (dans le clooooud comme on dit) tes sauvegardes (ou commits) Git. Ca permet d'avoir une version de secours si ton ordi brûle et surtout ça facilite le partage de code entre 2 personnes sur 2 ordis. A noter qu'il existe d'autres sites concurrents faisant plus ou moins la même chose (GitLab notamment)
___

Dans cette ressource nous allons te montrer pourquoi sauvegarder ton code via Git est mieux qu'un simple `CTRL` + `S` sur ton éditeur de code. Tu verras comment faire les opérations suivantes :

- Comment initialiser Git sur un repo pour que ce dernier fasse de belles sauvegardes
- Comment faire un commit de ton repo à un instant T, en y ajoutant un commentaire
- Comment regarder l'état du repo, là où tu en es, ce qui a changé depuis ton dernier commit
- Comment regarder les différences que tu as apportées à tel fichier par rapport au dernier commit
- Comment voir l'historique des sauvegardes (ou commits) qui ont été faites dans ton projet
- Comment revenir en arrière à telle sauvegarde (ou commit) afin soit de juste voir un ancien état pour comparer ou carrément repartir sur une ancienne base
- Comment lier ton projet Git à des sites externes avec tes remotes

Tu t'es déjà servi d'une majorité de ces commandes, mais c'est important de revenir dessus afin de s'assurer que tu as bien compris Git. Cet outil est <u>indispensable</u> quand on fait de la programmation et bien le comprendre te permettra d'être à l'aise pour cet outil que l'on considérera comme acquis au long de la formation.

Cette ressource abordera une base solide pour travailler seul sur Git et GitHub. Elle est très dense et se veut exhaustive, donc tu auras peut-être un peu mal à la tête en la lisant. Cependant, j'y ai mis plein d'exemples et tu pourras retrouver un récapitulatif des commandes en fin de ressource. L'objectif est que tu comprennes l'importance de Git, que tu aies un aperçu des commandes qui vont te servir, et que tu gardes cette ressource dans un favori pour plus tard.

## 2\. Historique

Git est un logiciel créé par Linus Torvalds (le fondateur de Linux) en 2005\. C'est un logiciel de gestion de versions, c’est-à-dire que l'équivalent d'une fonction de sauvegarde très poussée qui permet de revenir facilement en arrière, de travailler à plusieurs, ou de prendre en photo l'état d'un projet.

## 3\. La ressource

Pour cette ressource, nous allons l'illustrer avec une présentation "corporate" : un PowerPoint sur le bilan annuel de Big_Corpo_Food, un grand groupe spécialisé dans l'agroalimentaire. Comme tu es cool et branché, tu vas faire cette présentation en [HTML / CSS](https://revealjs.com/#/). Ton n+1 aime cet esprit de hackeur, mais cette présentation devra faire des aller-retours entre ton n+5, le designer, ton collègue qui veut jeter un œil, Jean-Michel de la compta. Même le facteur aura son mot à dire ! Bref, de grands moments de sauvegardes partout, de points récap’, de commentaires inutiles dans tous les sens, de franglais et acronymes dont même Google ignorait l'existence, mais gérés d'une main de fer grâce à git 🙏

### 3.1\. Introduction à git

Comme vu plus haut, git est un outil qui permet de faire du contrôle de version, c’est-à-dire une fonction sauvegarde d'un dossier, où chaque sauvegarde est accompagnée d'un commentaire. Cela permet de travailler très facilement à plusieurs sur un projet, et cela te permet à toi d'éviter d'avoir des fichiers comme `ProjetFinal_versionfinale_03_xretours.pptx` (avec un outil de sauvegarde puissant, revenir en arrière est aussi simple qu'une commande git).

Git fonctionne comme toute application sur ton terminal : il te suffit de rentrer `$ git ta_commande` et cela fera l'effet de la commande désirée. Par exemple si tu tapes `$ git --version`, ton ordinateur ressortira la version de git que tu utilises.

### 3.2\. Initialisation d'un repository

Avant de pouvoir dire à Git "hey sauvegarde mon dossier à l'instant T", il faut dire à Git "hey ce dossier sera un dossier que tu vas gérer". Pour ceci, il faut rentrer la commande suivante :
```shell
$ git init
```

Si tu fais `$ ls -a` tu pourras voir qu'un dossier `.git/` a été créé. Tu n'as pas besoin de toucher à ce dossier, mais sache que c'est là dedans que git va récupérer les infos dont il a besoin pour bien gérer ton dossier de projet.

___
**⚠️ ALERTE ERREUR COMMUNE**

Avant de te lancer, il est important que tu aies en tête qu'initialiser un repository Git signifie que le dossier (dans lequel tu es) correspond **à un seul et unique projet bien défini**. Il faut éviter de faire des `$ git init` dans des dossiers contenant eux-mêmes des dossiers de projets. Pourquoi ? Pour plein de raisons :

- L'historique Git va être commun à tous les projets et donc tu vas t'emmêler les pinceaux;
- Quand tu va envoyer ton repo sur GitHub, ça va créer un repo commun pour tous les projets, en mode "fourre-tout" pas propre;
- Si quelqu'un (par exemple tes futurs correcteurs) veut récupérer le code d'un de tes projets, il ne peut pas : il doit télécharger tout le dossier initialisé et donc tous les projets;
- Tu peux éventuellement t'en sortir quand un projet n'est qu'un petit fichier Ruby d'exercices mais le jour où c'est une application Rails, il est indispensable de créer un repo par application pour des raisons que le toi du futur (dans 2 mois) comprendra : c'est le bordel d'avoir un Git commun à plusieurs app Rails, Heroku n'arrivera pas à lire un dossier contenant plusieurs app Rails, etc.

En gros, à chaque projet (par exemple une session d'exercices Ruby), tu fais un dossier et tu initialises Git dans ce dossier. Si tu as un nouveau projet (nouvelle série d'exo, nouveau site à coder, etc.) tu fais un nouveau dossier et tu fais un nouveau `$ git init`.
___

Pour notre superbe présentation, cette dernière serait dans un dossier simple contenant le code HTML / CSS à mettre en ligne. On ferait `$ git init` dans le dossier `BilanAnnuelBigCorpoFood/` pour le démarrer.

### 3.3\. Effectuer une sauvegarde

Ah, c'est la commande importante. Celle de la sauvegarde. À partir de maintenant nous allons utiliser son vrai terme : commit. Le mot sauvegarde était bien pour que tu puisses imaginer ce que cela veut dire, mais en vrai dans git nous parlons de commit.

#### 3.3.1\. Qu'est-ce qu'un commit ?

Un commit est une sauvegarde à l'instant T de ton projet, dans lequel tu as mis un commentaire qui explique la sauvegarde ("retours de Christine sur les KPIs de janvier", "correction d'une faute de grammaire slide 6", etc).

___
** 🎨 EXEMPLE ILLUSTRÉ**

Tu peux voir un commit comme une métaphore d'une photographie de mariage : tu choisis qui tu vas photographier, puis tu prends ces personnes en photo.
___

Dans un commit tu vas dire à Git quels fichiers tu aimerais photographier, puis tu vas exécuter ton commit. Nous allons voir les commandes pour ceci.

#### 3.3.2\. Comment faire un commit ?

Pour faire un commit, tu vas d'abord ajouter les fichiers que tu voudrais sauvegarder avec `git add nom_fichier`, puis tu vas les sauvegarder avec `git commit -m "message de commit"`. C'est aussi simple que cela.

Prenons l'exemple de notre présentation trop cool. Chantal du marketing t'a dit d'ajouter trois diapositives à la fin dans lesquelles il faut mentionner que Big_Corpo_Food compte "externaliser les workshops risque pour lutter contre les deadlines qui vont switcher". Tu n'es pas trop sûr de ce que ça veut dire, mais tu crées ces trois diapositives nommées `15.html`, `16.html` et `17.html`, dans lesquelles tu balances des phrases trouvées sur [Pipotronic](http://pipotronic.com/). Pour faire un commit et lui montrer ce travail tu feras :
```shell
$ git add 15.html
$ git add 16.html
$ git add 17.html
$ git commit -m "ajout de trois slides selon les retours de Chantal"
```

Et voilà, Chantal aura une belle version que tu pourras présenter sans crainte d'avoir perdu ce que tu as fait avant.

___
**⚠️ ALERTE ERREUR COMMUNE**

La commande `$ git add .` permet d'ajouter tous les fichiers à ton futur commit. Cependant, cette commande est à utiliser que si c'est pertinent de faire un commit avec tous les fichiers.

Prenons l'exemple de notre présentation. Pendant que tu étais en train de faire la diapositive `16.html`, tu reçois un e-mail avec "URGENT" dans l'objet, où Jean-Michel te dit qu'il faut changer ASAP la diapo `3.html` pour qu'elle soit moins "touchy". Tu le fais et tu veux lui envoyer ton travail. Or, si tu fais `$ git add .`, et après `git commit`, tu feras un commit qui prendra les diapos `15.html` et `16.html`, qui n'ont rien à voir avec la demande de Jean-Michel. Ainsi, pour faire un commit proprement, tu feras :
```shell
$ git add 3.html
$ git commit -m "slide 3 moins touchy selon les retours de Jean-Michel"
```

Cette technique de pro permettra d'avoir des commit bien rangés 👍

___

___
** 🚀 ALERTE BONNE ASTUCE**

L'univers du code est anglais, les commits c'est la même. De manière générale, il est convenu de mettre de l'anglais dans les messages de commits. C'est une convention.

Le bon côté est que cela t'évitera un entre-deux foireux en mettant les franglais bizarres de tes collègues de Big_Corpo_Food 😉
___

#### 3.3.3\. Petite explication sur les commandes git add et git commit

Afin que tu connaisses bien tes futures commandes préférées, nous allons te montrer comment elles marchent :

##### 3.3.3.1\. Git add

`git add nom_fichier` ajoute ton fichier à ce que va être commit. Il faut toujours préciser quoi ajouter sinon ton ordinateur ne saura pas quel fichier ajouter :
```shell
$ git add
Nothing specified, nothing added.
Maybe you wanted to say 'git add .'?
```

##### 3.3.3.2\. git commit

`git commit` effectue un commit, dans lequel il y aura un message de commit qui explique ce que tu as commit. En faisant `$ git commit`, ton terminal va ouvrir un éditeur de texte dans lequel tu peux faire un message très long qui prend plusieurs lignes. Nous sommes un peu malins et on va tout faire en une ligne en mettant la commande `-m`. Ainsi, ton commit se fera avec :
```shell
$ git commit -m "ton message"
```

Et voilà pourquoi on utilise le fameux `-m`. Attention si tu fais un commit alors qu'aucun fichier n'a été ajouté avec `git add`, ton ordinateur t'enverra chier. La commande d'après te sera donc très utile pour savoir où tu en es.

### 3.4\. Voir l'état de nos fichiers à sauvegarder

Cette commande sera celle que l'on utilise le plus. Comme dirait ce bon vieux dicton : "dans le doute, fais `$ git status`". `git status` est une commande qui permet de te dire :

- les fichiers qui sont différents par rapport au dernier commit, et qui n'ont pas été ajoutés avec `git add`
- les fichiers qui sont différents par rapport au dernier commit, et qui ont été ajoutés avec `git add` (donc qui seront pris en compte dans le prochain commit)

Pour chacun de ces cas, `git status` te dira aussi si le fichier vient d'être créé, ou si le fichier était déjà là au dernier commit et tu as juste affaire à une modification.

En gros il compare ton travail actuel avec le dernier commit, et te dit l'état des fichiers.

Prenons l'exemple de notre présentation. Tu viens de finir la troisième diapo de Chantal, mais tu ne sais pas trop où tu en es : est-ce que tu as fais "add" sur `16.html` ? En plus avec les remarques de Jean-Michel, c'est un peu le doute. Mais tu te souviens du super dicton de Félix, donc tu rentres la fameuse commande :
```shell
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

  new file:   15.html
  new file:   16.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

  new file:   17.html
  modified:   3.html
```

Super, tu peux voir que les fichiers `15.html` et `16.html` ont bien été "add", et que `17.html` et `3.html` ne sont pas "add" pour ton futur commit. Le fichier `3.html` doit correspondre à la demande de Jean-Michel. On va s'occuper de la demande de Chantal avant vérifier le fichier `3.html`. Pour "add" le fichier `17.html` on va faire la commande `$ git add 17.html`. Si tu fais `$ git status` à ce moment-là, tu devrais avoir :
```shell
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

  new file:   15.html
  new file:   16.html
  new file:   17.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

  modified:   3.html
```

C'est exactement ce que tu recherches : les trois fichiers sont ajoutés, prêts à être commit. Et bien faisons le fameux commit :
```shell
$ git commit -m "3 slides added following advices from Chantale"
```
___
** 🚀 ALERTE BONNE ASTUCE**

On ne le répétera jamais assez, mais la commande `git status` est vraiment super pratique et te donnera en quelques lignes l'état de ton dossier Git. Utilise-la, abuses-en. Elle sera ta meilleure amie 👨‍🏫
___

### 3.5\. Comparer un fichier avec son ancienne version

Des fois, tu as envie de voir quelles sont les modifications que tu as apportées à un fichier avant de le commit. Prenons l'exemple précédent, du fichier `3.html`, qui, selon `git status` est différent par rapport au dernier commit. Tu es pourtant sûr d'avoir envoyé la bonne version à Jean-Michel. Tu aimerais bien voir les différences avec le dernier commit. Ainsi tu peux utiliser la commande `git diff` qui donne les lignes différentes entre le fichier modifié et le fichier au moment du commit précédent.
```shell
$ git diff
==> affiche toutes les modifications de tous les fichiers entre les commits
```
___
**🚀 ALERTE BONNE ASTUCE**

Tu peux faire `$ git diff nom_fichier` pour avoir git diff limité seulement à ce fichier 👻
___

En l’occurrence, pour notre fichier `3.html` tu as pu voir que la modification est due à une correction d'une faute de grammaire. Tu avais écrit "il fallait que je forwarde" au lieu de "il fallait que je forwardasse". Grave faute d'accord de l'imparfait du subjonctif du verbe "forwarder" que tu as corrigée, mais oublié de commit. Avec un petit `git add` et `git commit` voici ta faute réparée. Parfait.

### 3.6\. Regarder l'historique des versions

Imaginons que tu aies envie de voir l'historique des commits. Après tout, que serait un outil de gestion de sauvegarde si l'on ne pouvait pas aller en arrière ? La commande `git log` est là pour t'aider 👌
```shell
$ git log
commit df31a99ba2980d31c6e84179d35a557dd59c10c2
Author: pseudo 
Date:   la_date

    3 slides added following advices from Chantal

commit 100d6f07dbf4cfb9103b3819e64432186750a1a2
Author: pseudo 
Date:   la_date

    grammar mistake for a verb
```

Tu peux voir la liste des commits, avec les informations importantes :

- Qui l'a commité
- Quand a-t-il été commité
- Pourquoi ? (avec le message)
- Qu'est-ce qui a été commité ? (grâce au code bizarre)

Le code `100d6f07dbf4cfb9103b3819e64432186750a1a2` est le SHA du commit. C'est son identifiant unique. Tu peux facilement revenir en arrière avec ceci.

### 3.7\. Revenir en arrière

Il y a deux façons de revenir en arrière :

- La première est à titre purement indicatif, et te servira juste pour regarder un état précédent
- La seconde est un retour définitif en mode "je veux revenir à tel endroit pour retravailler à partir de là"

#### 3.7.1\. Retour en arrière à titre purement indicatif

Imaginons que Jean-Michel, pas très sûr de lui, te demande s'il peut vérifier son ancienne diapo `3.html` pour voir ce qu'il y avait avant dedans. Dans un format classique en mode corpo, tu aurais eu un fichier `présentationfinale_sansretoursjeanmi.pptx`, mais fini les bêtises, avec git tu as juste à faire :
```shell
$ git checkout SHA
```

(en remplaçant "SHA" par le code que tu as eu lors du `git log`)

Ainsi, tu peux naviguer dans l'ancienne version pour consulter les fichiers à cet instant T. Aussi simple que cela. Pour revenir à la version actuelle tu n'as qu'à faire :
```shell
$ git checkout master
```
___
**⚠️ ALERTE ERREUR COMMUNE**

Cette commande n'est pas à utiliser si jamais tu veux faire des modifications sur un fichier. Si jamais tu fais cela, tu vas avoir une erreur qui va te faire atterrir [sur l'un des threads les plus célèbres](https://stackoverflow.com/questions/5772192/how-can-i-reconcile-detached-head-with-master-origin) de Stack Overflow. Si jamais tu veux revenir en arrière pour faire des modifications, il te faudra passer à la section suivante
___

___
** ⚠️ ALERTE ERREUR COMMUNE**

`git checkout` ne marche que si tu n'as pas de modifications non sauvegardées. Si tu es entre deux commits, git checkout te renverra cette erreur :
```shell
$ git checkout 100d6f07dbf4cfb9103b3819e64432186750a1a2           
error: Your local changes to the following files would be overwritten by checkout:
  3.html
Please commit your changes or stash them before you switch branches.
Aborting
```

Par conséquent, il te faudra soit faire une sauvegarde (== faire un commit), soit effacer tout pour revenir au commit d'avant, soit stash tes modifications. Je vais montrer ces commandes plus en détails plus tard tkt.
___

#### 3.7.2\. Revenir en arrière définitivement

Imaginons que Christine ne valide pas l'idée de Jean-Michel, et te demande de la supprimer. Tu peux revenir en arrière définitivement avec la commande `git reset` qui s'utilise comme ceci :
```shell
$ git reset --hard SHA
```

(en remplaçant "SHA" par le code que tu as eu lors du `git log`)

___
** 🚀 ALERTE BONNE ASTUCE**

La commande `git reset` est aussi très pratique pour effacer son travail actuel et revenir au commit précédent. Par exemple : tu es en train de travailler sur la diapo de Jean-Michel, mais en plein milieu tu te dis que l'approche que tu as faite n'est pas bonne et tu as envie d'effacer tout ce que tu as fait jusqu'à présent. Plutôt que de faire `CTRL` + `Z` plein de fois, tu peux rentrer la commande suivante :
```shell
$ git reset --hard
```

Et hop tu reviens à ton dernier commit. Très pratique pour tester des concepts à la volée, ou bien te rendre compte que tu n'as pas envie de commit les changements que tu viens de faire.
___

### 3.8\. Sauvegarde provisoire de son travail

Des fois tu seras en train de travailler sur une fonctionnalité qui prend du temps, et tu auras envie de bouger ailleurs, par exemple vers un commit précédent, ou une autre branche (on verra le système de branches plus tard). Si jamais tu fais `git checkout` alors que tu as du travail non committé, Git t'enverra chier en disant "Your local changes to the following files would be overwritten by checkout. Please commit your changes or stash them before you switch branches". Nous allons voir la commande `git stash` qui permet de faire une sauvegarde provisoire.

Par exemple, tu es en train de travailler sur la diapo de Jean-Michel. Sauf qu'en plein milieu de ton travail, tu aimerais bien vérifier un truc sur un ancien commit. Le souci, c'est que tu ne peux pas faire `git checkout SHA` sinon Git va t'envoyer bouler. Et tu ne peux pas faire de commit car ton travail n'est pas prêt. Cependant, tu peux faire `$ git stash` et Git s'occupera pour toi de mettre de côté les fichiers, comme ça tu peux facilement te balader d'un commit à l'autre avec `git checkout`

Et une fois que tu es de retour sur le bon commit, tu as juste à faire `$ git stash pop` pour récupérer ton travail. Aussi simple que cela.

### 3.9\. Gérer les remotes

Nous entrons dans la dernière partie de cette longue ressource : les remotes. Qu'est-ce qu'un remote ? C'est une version à distance de ton repo Git, comme une copie stockée (souvent sur Internet). Tu peux facilement faire local -> remote ou remote -> local avec Git.

Avec `git remote`, tu peux facilement ajouter des remotes, voir la liste des remotes, enlever des remotes.

Il existe plusieurs types de remote :

- GitHub, qui te permet d'avoir un repository à distance qui te permet de partager à d'autres ton travail et de disposer d'une sauvegarde en cas de coup dur. C'est extrêmement pratique et ce sera notre façon principale de travailler pour cette session
- Heroku, qui te permet d'envoyer le code d'une application Rails pour qu'il la transforme en serveur (= qu'il la publie sur Internet) ;
- GitLab, qui est un peu comme GitHub ;
- Et bien d'autres.

Chaque remote aura un nom. Ce nom peut être par exemple "other_github", "origin", "heroku", ou "jetaime". Par convention, le repo en ligne principal s'appelle "origin". C'est d'ailleurs pour cela que tu ajoutes bien souvent ton repo github avec `$ git remote add origin ton_url` : avec cette commande, tu ajoutes une remote nommée origin qui n'a autre que l'url "ton_url".

Pour voir toutes les remotes associées à ton dossier git, tu peux faire : `$ git remote -v`

### 3.10\. Jouer avec les remotes

Avec Git, c'est facile d'envoyer son repo sur le remote (local -> remote) ou de récupérer les infos d'un remote sur ton ordi (remote -> local) : les commandes `git pull` et `git push` vont faire cela.

#### 3.10.1\. git push

La commande `git push` va pousser ton code stocké en local vers un remote de ton choix. Elle s'utilise de la manière suivante : `$ git push nom_remote nom_branche`. Ainsi, si tu veux push ta branche "master" vers la remote "origin" tu feras :
```shell
$ git push origin master
```

Ou alors si tu veux push ta branche "other_branch" vers la remote "heroku" tu feras :
```shell
$ git push heroku other_branch
```
___
**🤓 QUESTION RÉCURRENTE**

**Jamy je suis perdu : c'est quoi une branche ?**

Ce n'est pas l'objet du cours, mais je vais faire un petit aparté à ce sujet. Une branche, grosso modo, est une bifurcation de ton projet sur laquelle tu vas travailler de manière indépendante. Cette fonctionnalité très pratique permet de travailler sur une version parallèle de ton projet, et de la re-fusionner plus tard, quand tu seras content des modifications que tu as apportées. Pour le moment tu fais des commits sur Master, mais la plupart des fonctionnalités te demanderont de travailler sur une branche, pour éviter de faire des commits sur Master, et de proposer à tes utilisateurs une fonctionnalité non terminée.

![](https://i.imgur.com/fKP7zaP.png)

Prenons l'exemple de la présentation. Marie, l'experte en design voudrait retravailler les couleurs de la présentation, ce qui va prendre plusieurs jours de meetings intenses sur la psychologie du rouge. Pour ceci, tu voudrais créer une branche nommée `new_design` sur laquelle vous allez faire plusieurs commits, envoyer des échantillons au reste de l'équipe. Quand vous serez content, vous n'aurez qu'à fusionner la branche `new_design` avec la branche `master` et à vous la gloire.

Pour le moment, nous n'allons pas voir les branches. Sache juste qu'il existe un système de branches, et que tu vas travailler sur branche principale nommée `master`.
___

___
** 🤓 QUESTION RÉCURRENTE**

**Je viens d'initialiser un repo mais quand je push sur GitHub, certains dossiers de mon repo n'apparaissent pas (mais le reste si). Pourquoi?**

S’il n’y a aucun fichier dans un dossier, Git ne pushe pas le dossier. Donc ne t'étonne si un dossier vide sur ton ordi n'apparait pas dans GitHub : dès qu'un fichier (Ruby ou autre) y sera ajouté avec `$ git add` puis commit et push, le dossier apparaîtra avec son fichier !
___

#### 3.10.11\. git pull

La commande `git pull` est le contraire de `git push` : elle prend le code de la remote de ton choix et remplace le code en local. Elle s'utilise de la manière suivante : `$ git pull nom_remote nom_branche`. Ainsi, si tu veux pull ta branche "master" depuis la remote "origin" tu feras :
```shell
$ git pull origin master
```

### 3.11\. Messages d'erreur

On ne va pas se leurrer, Git au début ce n'est pas facile, comme tu as pu voir durant la semaine 1\. Avant de te précipiter et de maudire ton ordinateur, nous allons annoncer quelque chose : c'est normal d'avoir des erreurs, surtout au début. C'est arrivé à TOUT le monde, surtout ceux qui sont à l'aise aujourd'hui ❤ Le but c'est de ne pas désespérer, et de résoudre tes soucis. Comme tout développeur est passé par ce chemin, les réponses aux problèmes classiques pullulent sur Stack Overflow. Copie-colle ton message d'erreur, lis les réponses, essaie de comprendre, et résous ton erreur.

___
** 🎨 EXEMPLE ILLUSTRÉ**

Prenons l'exemple d'une erreur que j'ai eue à mes débuts sur git. J'avais un repo git en local que j'avais déjà lié à une remote `origin` qui était un repo GitHub. Je n'étais pas content de mon repo GitHub, donc je l'ai supprimé et ai recréé un repo GitHub. Puis j'ai voulu lier mon repo local à ce nouveau repo GitHub. Pour ceci, une commande : `$ git remote add origin url_du_repo`. Sauf que :

<pre><`$ git remote add origin url_repo
fatal: remote origin already exists.`</pre>

Fatal. En général les erreurs sont en mode "error bug", mais là c'est fatal. C'est que ça doit être grave, non ? Non. Une recherche Google du message d'erreur et tu pourras trouver que [c'est juste un problème de remote origin qui existe déjà](https://stackoverflow.com/questions/1221840/remote-origin-already-exists-on-git-push-to-a-new-repository).

Bref, les erreurs tu en auras. La clé de succès de The Hacking Project est ta capacité à bien les analyser, et faire les bonnes recherches Google qui vont résoudre ton problème
___

## 4\. Points importants à retenir

La ressource est extrêmement dense et ton cerveau doit exploser. Voici un récap’ des commandes vues aujourd'hui. Elles constituent le kit de démarrage du moussaillon de THP :

- `$ git init` permet d'initialiser un répo git en local
- `$ git add nom_fichier` permet d'ajouter nom_fichier à ton futur commit
- `$ git commit -m "message_commit"` permet de faire un commit avec pour message message_commit
- `$ git status` permet d'afficher l'état de tes fichiers par rapport au commit que tu es en train de réaliser (⚠ commande très pratique, à faire tout le temps)
- `$ git diff nom_fichier` permet d'afficher les modifications de nom_fichier entre le dernier commit et le fichier actuel
- `$ git log` permet d'afficher l'historique des commits
- `$ git checkout SHA` permet de revenir en mode lecture uniquement au commit SHA
- `$ git checkout master` permet de revenir au commit actuel
- `$ git reset --hard SHA` permet de tout effacer pour revenir au commit SHA
- `$ git reset --hard` permet de tout effacer pour revenir au dernier commit
- `$ git stash` permet de sauvegarder provisoirement son travail sans le commit
- `$ git stash pop` permet de récupérer un travail précédemment sauvegardé avec `git stash`
- `$ git remote -v` permet de voir les différentes remotes de ton repo git
- `$ git remote add nom_remote url_remote` permet d'ajouter la remote url_remote à la liste de tes remotes. Cette remote aura le nom nom_remote (par convention, la remote principale où il y a le code s'appelle origin)
- `$ git push nom_remote nom_branche` permet de pousser ta branche nom_branche vers ta remote nom_remote
- `$ git pull nom_remote nom_branche` permet de récupérer ta branche nom_branche de ta remote nom_remote

## 5\. Pour aller plus loin

Te voici solidement armé pour faire du Git en mode solo. Nous verrons plus tard comment travailler en équipe via Git. En attendant, tu peux sauvegarder cette ressource dans un coin car tu y reviendras souvent 😉

Voici quelques ressources en plus si tu veux aller plus loin sur Git :

- Un ancien de THP a fait [un cours sur Git](https://github.com/Nicolas-Hermet/Git_GitHub_From_Zero_to_Solo
    ) si tu veux avoir un autre point de vue.
- Jonathan Boyer de la chaîne Grafikart a fait [un cours assez complet](https://www.grafikart.fr/formations/git) sur Git. En général ce qu'il fait c'est vraiment très cool donc n'hésite pas à jeter un œil à son site.
- Marc Gauthier a fait [un cours assez complet](https://openclassrooms.com/fr/courses/2342361-gerez-votre-code-avec-git-et-github) sur Git et GitHub, hébergé sur OpenClassrooms.
- La [documentation officielle](https://git-scm.com/docs) de Git permet de connaître toutes les commandes et ses options. Par exemple tu peux voir les options de [git remote](https://git-scm.com/docs/git-remote).

Si tu veux masteriser GitHub, voici [quelques astuces disponibles dans cet article](https://dev.to/_darrenburns/8-productivity-tips-for-github-44kn).