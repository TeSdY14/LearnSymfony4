# Stellar Development with Symfony 4
## [Chapter 02 - Our Micro-App & PhpStorm Setup](https://symfonycasts.com/screencast/symfony4/micro-app-phpstorm#play)

Notre mission : aller audacieusement là où personne n'est allé auparavant... en consultant notre application ! 
J'ai déjà ouvert le nouveau répertoire dans PhpStorm, alors "lancez votre tricordeur" (_référence à un appareil de détection dans Star Trek_) et explorons!!

### Le répertoire Public/
Il n'y a que trois répertoires auxquels vous devez penser. 
Tout d'abord, `public/` est la racine du document : il contiendra donc tous les fichiers accessibles au public. Et ... il n'y en a qu'un en ce moment : **`index.php`**. 
C'est le "**contrôleur frontal**" : un mot sophistiqué inventé par les programmeurs qui signifie que c'est le fichier qui est exécuté lorsque vous accédez à n'importe quelle URL.

Mais, vraiment, vous n'aurez presque jamais à vous en soucier. En fait, maintenant que nous avons parlé de ce répertoire, arrêtez d'y penser !

### Répertoire src/ et config/
Oui, j'ai menti ! Il n'y a vraiment que deux répertoires auxquels vous devez penser : **`config/`** et **`src/`**. **`config/`** détient... euh... _**les fichiers de configuration**_ et 
**`src/`** est l'endroit **où vous placerez tout votre code PHP**. C'est aussi simple que cela.

Où est Symfony ? Comme d'habitude, lorsque nous avons créé le projet, Composer a lu notre fichier `composer.json` et a téléchargé toutes les bibliothèques tierces (les dépendances) - _y compris des parties de Symfony_ - dans le répertoire `vendor/`.

## Installer le serveur

Revenez à votre terminal et trouvez l'onglet d'origine. Vérifiez ceci : en bas, il est dit que nous pouvons obtenir un meilleur serveur Web en exécutant `composer require server`. 
J'aime les meilleurs choses, alors essayons-le ! Appuyez sur Ctrl+C pour arrêter le serveur existant, puis exécutez :
```shell
composer require server
```
Si vous êtes familier avec Composer... ce nom de package devrait avoir l'air drôle ! Vraiment faux ! 
Normalement, chaque nom de paquet est 'quelque chose' slash 'quelque chose', comme `symfony/console`. Donc ... le serveur ne devrait tout simplement pas fonctionner ! 
Mais c'est le cas ! Cela fait partie d'un nouveau système cool appelé **`Flex`**. 
Plus à ce sujet prochainement !

Lorsque cela est terminé, vous pouvez maintenant exécuter :
```shell
php ./bin/console server:run
```
Cela fait essentiellement la même chose qu'avant ... mais la commande est plus courte. Et quand on rafraîchit, ça marche toujours !

Au fait, cette commande `bin/console` va être notre nouveau "robot acolyte" (_sidekick robot_). Mais ce n'est pas magique : notre projet a un répertoire `bin/` avec un fichier console à l'intérieur. 
Les utilisateurs de Windows devraient utiliser `php bin/console`... car ce n'est qu'un fichier PHP.

Alors, quelles choses étonnantes ce robot `bin/console` peut-il faire ? Dans votre onglet de terminal ouvert, exécutez simplement :
```shell
php ./bin/console
```
Oui ! Ceci est une liste de toutes les commandes `bin/console`. Certains d'entre eux déboguent de l'or. Nous en parlerons en cours de route !

### PhpStorm Setup
Ok, nous sommes presque prêts à commencer à coder ! Mais nous devons parler de notre vaisseau spatial, je veux dire, éditeur ! 
Regardez, vous pouvez utiliser ce que vous voulez... mais... je recommande fortement PhpStorm ! 
Sérieusement, cela fait du développement dans Symfony un rêve ! Et non, ces gentils gars et filles de PhpStorm ne me paient pas pour dire ça... mais ils le peuvent s'ils le veulent !

Euh, si vous l'utilisez... ce qui serait génial pour vous... il y a 2 secrets que vous devez savoir pour tromper votre vaisseau spatial, ah, éditeur ! 
De toute évidence, j'étais en hyper-sommeil trop longtemps.

Allez dans **Préférences > Plugins**, puis cliquez sur **Parcourir les référentiels**. 
Il y a 3 plugins indispensables. Recherchez « **Symfony** ». 
Premièrement : le '**Symfony Plugin**'. Il a plus de 2 millions de téléchargements pour une raison : il vous donnera des tonnes d'auto-complétion ridicule. 
Vous devez également télécharger « **PHP Annotations** » et « **PHP Toolbox** ». Je les ai déjà installés. Sinon, vous verrez un bouton '_Installer_' en haut de la description. 
Installez-les et redémarrez PHPStorm.

Ensuite, revenez aux **Préférences**, recherchez '**symfony**' et trouvez la nouvelle section '**Symfony**'. 
Cliquez sur la case à cocher '**Activer le plugin**' : vous devez activer le plugin Symfony pour chaque projet. _Il dit que vous devez redémarrer... mais je pense que c'est un mensonge._ 
C'est de l'espace ! Qu'est-ce qui pourrait mal se passer ?

Voilà donc l'astuce PhpStorm n°01. 
Pour le second, recherchez '**Composer**' et cliquez sur la section '**Composer**'. 
Cliquez pour rechercher le '**Chemin vers `composer.json`**' et sélectionnez celui de notre projet. Je ne sais pas pourquoi ce n'est pas automatique... mais peu importe ! 
Grâce à cela, PhpStorm facilitera la création de classes dans `src/`. Vous verrez cela très bientôt.

D'accord ! Notre projet est mis en place et fonctionne déjà. 
Commençons à créer des pages et à découvrir des choses plus intéressantes sur la nouvelle application.