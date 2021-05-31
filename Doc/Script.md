Salut ! Il est temps de Symfony 4 ! Je suis tellement excité. Pourquoi ? 
Parce que rien ne me rend plus heureux que de travailler dans un cadre où le codage est vraiment amusant et où je peux créer des fonctionnalités rapidement, mais sans sacrifier la qualité. 
Eh bien, peut-être que je serais encore plus heureux de faire tout ça sur une plage ... avec, peut-être une boisson fraîche ?

Quoi qu'il en soit, Symfony 4 a complètement repensé l'expérience des développeurs : vous allez créer de meilleures fonctionnalités, plus rapidement que jamais. 
Et, Symfony a un nouveau super-pouvoir unique : il commence comme un microframework, puis s'adapte automatiquement à la taille de votre projet. Comment ? Restez à l'écoute...

Oh, et ai-je mentionné que Symfony 4 est la version la plus rapide de tous les temps ? Et le framework PHP le plus rapide ? 
Honnêtement, tous les frameworks sont assez rapides de toute façon, mais le fait est le suivant : __vous construisez sur une base vraiment impressionnante__.

> Tip
> 
> Voir http://www.phpbenchmarks.com pour les statistiques de référence tierces!!

### Préparation : Télécharger et mettre à jour Composer

Ok, commençons ! Ouvrez un nouveau terminal et accédez au répertoire de votre choix. 
Assurez-vous que Composer est déjà installé globalement afin de pouvoir simplement dire "**composer**".

Et assurez-vous également que vous disposez de la dernière version:
```shell
composer self-update
```
*C'est important : Composer a récemment corrigé un bogue pour aider Symfony.*

### Installer Symfony!
Pour télécharger votre nouveau projet Symfony, exécutez "**composer create-project symfony/skeleton**" et placez-le dans un nouveau répertoire appelé "the_spacebar".
```shell
composer create-project symfony/skeleton the_spacebar '4.4.*'
```
C'est le nom de notre projet ! 

'The Spacebar' sera le lieu où les gens de toute la galaxie pourront communiquer, partager des nouvelles et discuter des célébrités et de BitCoin. 
Ça va être incroyable !

Cette commande clone le projet **symfony/skeleton**, puis exécute "**composer install**" pour télécharger ses dépendances.

Plus bas, il y a quelque chose de spécial : quelque chose sur les « recipes » (recettes). Les "recipes" sont un concept nouveau et très important. Nous en parlerons dans quelques minutes.

### Démarrer le serveur Web
Et en bas, cool ! Symfony nous donne des instructions claires sur la marche à suivre. 
Déplacez-vous dans le nouveau répertoire :
```shell
cd the_spacebar
```
Apparemment, nous pouvons exécuter notre application immédiatement en exécutant :
```shell
php -S 127.0.0.1:8000 -t public
```
Cela démarre le serveur Web PHP intégré, ce qui est idéal pour le développement. **Public/** est la racine du document du projet - mais plus à ce sujet bientôt !

> Tip
>
> Si vous souhaitez utiliser Nginx ou Apache pour le développement local, vous pouvez : Voir http://bit.ly/symfony-web-servers.

Il est temps de décoller ! Ouvrir votre navigateur et accédez à **http://localhost:8000**. 
Dites bonjour à votre nouvelle application Symfony !

### Notre petit projet
> Tip
>
> Symfony ne crée plus automatiquement de référentiel Git pour vous. Mais pas de problème ! Tapez simplement git init une fois pour initialiser votre référentiel.

De retour dans le terminal, je vais créer un nouvel onglet de terminal. Symfony a déjà initié un nouveau dépôt git pour nous et nous a donné un fichier **.gitignore** parfait. 
Merci Symfony !

> Tip
>
> Si vous utilisez PhpStorm, vous voudrez ignorer le répertoire ".idea" dans le depôt Git. Je l'ai déjà ignoré dans mon fichier global **.gitignore** : 
> https://help.github.com/articles/ignoring-files/

Cela signifie que nous pouvons créer notre premier **commit** simplement en disant :
```shell
git init
git add .
git commit
```

Créez un message de validation calme et réfléchi.
```shell
# Woohoo ! OMG WE ARE USING SYMFONY4
```
Woh ! Vérifiez ceci : le projet entier - y compris Composer et les trucs **.gitignore** - ne contient que 16 fichiers ! 
Notre application est toute petite !

Apprenons-en plus sur notre projet ensuite et configurons notre éditeur pour rendre le développement Symfony incroyable !