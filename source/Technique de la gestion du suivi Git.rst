Technique de la gestion du suivi Git
====================================

Création du dépôt sur GitHub
----------------------------

1. Connectez-vous à votre compte GitHub.
2. Cliquez sur le bouton New pour créer un nouveau dépôt.
3. Remplissez les champs :

    - Repository name : Entrez un nom pour votre projet (ex. sphinx-docs).
    - Description : Ajoutez une description si vous le souhaitez.
    - Cochez l'option Add a README file si vous voulez créer un fichier README.md.

4. Vous pouvez laisser les autres options par défaut.
5. Cliquez sur Create repository pour créer le dépôt.


Création du jeton pour avoir accès au dépôt GitHub
--------------------------------------------------

1. Sur votre compte GitHub, clic gauche sur la photo de de profil, puis Settings > Developer settings > Personal access tokens.
2. Cliquez sur Generate new token.
3. Donnez un nom au jeton, sélectionnez les autorisations nécessaires (généralement repo pour accéder aux dépôts privés ou publics), puis cliquez sur Generate token.
4. Copiez le jeton immédiatement, car vous ne pourrez pas le voir à nouveau.


Initialisation du Dépôt Git Local
---------------------------------

Il faut s'assure que Git est bien installé sur l'ordinateur. Git est disponible via le lien suivant : https://git-scm.com/downloads

1. Ouvrez votre terminal ou l'invite de commande dans le répertoire racine de votre projet Sphinx.
2. Initialisez un dépôt Git :

.. code-block:: bash

    git init

3. Ajoutez tous les fichiers Sphinx nouvellement créés à votre dépôt :

.. code-block:: bash

    git add .

4. Faites un premier commit :

.. code-block:: bash

    git commit -m "Initial commit of Sphinx documentation"

Assurez-vous que la branche s'appelle bien **main** et non **master**, avec la commande :

.. code-block:: bash

    git branch

Pour changer le nom de la bnache, utiliser la commande :

.. code-block:: bash

    git branch -M main


Connection du Dépôt Local au Dépôt GitHub
-----------------------------------------

1. Ajoutez le dépôt distant GitHub à votre dépôt local :

.. code-block:: bash

    git remote add origin https://github.com/USERNAME/sphinx-docs.git

2. Remplacez **USERNAME** par votre nom d'utilisateur GitHub et **sphinx-docs** par le nom de votre dépôt.

Avant le premier push, il faut s'assurer que le dépôt local contient les informations du dépôt distant, ce qui n'est pas forcément le cas si un fichier 'Readme' a été généré lors de la création du dépôt distant. Il faut donc rappatrier les données, en validant les changements locaux en amont :

.. code-block:: bash

    git add .
    git commit -m "Save local changes before rebase"
    git pull origin main --rebase


3. Poussez vos modifications sur GitHub :

.. code-block:: bash

    git push -u origin main

4. Si votre branche par défaut est master au lieu de main, remplacez main par master.


Utilisation de  SourceTree pour Gérer le dépôt
----------------------------------------------

Ouvrir le projet dans SourceTree
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Ouvrez SourceTree.
2. Cliquez sur **Add** dans la barre d'outils.
3. Sélectionner le dossier du projet.


Coupler SourceTree au dépôt GitHUB
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il faut rensigner le Token dans SourceTree :

1. Menu Outils > Options > Authentification > Ajouter

    - Service d'hébergement : GitHub
    - Protocole préféré : HTTPS
    - Authentification : Basic

Entrer son identifiant GitHub


Cliquez sur Clone.
Vous pouvez maintenant utiliser SourceTree pour gérer vos commits, vos branches, et vos push/pull vers GitHub.