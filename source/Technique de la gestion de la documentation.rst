Technique de la gestion de la documentation
===========================================



Installatin de Sphinx
---------------------
Installer Chocolatey pour gérer les packets

.. code-block:: bash

    choco install sphinx


Création de la documentation dans un répertoire
-----------------------------------------------
Se rendre dans le dossier de la documentation

.. code-block:: bash

    E:
    cd E:\Iban\Documents\Sailing_Simulator\Documentation_Sphinx

Installer l'environnement virtuel dans le dossier

.. code-block:: bash

    python -m venv .venv

Activer l'environnement virtuel

.. code-block:: bash

    .venv\Scripts\activate

Installer Sphinx

.. code-block:: bash

    pip install sphinx

Créer la documentation

.. code-block:: bash

    sphinx-quickstart

Configuration de la documentation
---------------------------------
Pour que la documentation soit jolie il faut installer un thème. Le thème 'sphinx_rtd_theme' est très bien.

Installer le thème en ligne de commande

.. code-block:: bash

    pip install sphinx_rtd_theme


Ouvrir le fichier **con.py** qui se trouve dans le répertoire **source** et remplacer le thème

.. code-block:: rst

    html_theme = 'sphinx_rtd_theme'

Build de la documentation
-------------------------
Se rendre dans le dossier de la documentation.

.. code-block:: bash

    E:
    cd E:\Iban\Documents\Sailing_Simulator\Documentation_Sphinx

Si .venv n'est pas activée, l'activer

.. code-block:: bash

    .venv\Scripts\activate

Puis exécuter la commande suivante pour chaque régénération de la documentation :

.. code-block:: bash

    sphinx-build -b html source docs

.. note::
    Traditionnellement, la documentation est générée dans le dossier **build** avec la commande **make.bat html**. Mais étant donné que GitHUB ne lit que le répertoire **docs** pour afficher la documentation en ligne, nous devons utiliser la commande de build **sphinx-build -b html source docs**.

Création d'une nouvelle page
----------------------------

Créer un fichier texte dans le répertoire **source** avec un titre et l'extension **.rst**.
Ouvrir ce fichier et écrire son titre, sous-ligné de signes **==** de même longueur que le titre.
Dans le fichier **index.rst** reporter le titre de la nouvelle page dans la table des matières.

Sous-titre de niveau 2
~~~~~~~~~~~~~~~~~~~~~~~

Sous-titre de niveau 3
^^^^^^^^^^^^^^^^^^^^^^^
