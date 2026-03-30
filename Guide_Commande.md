## Guide d'Utilisation : Claude Code & Interface ##

Ce document recense les commandes et paramètres essentiels pour l'utilisation de Claude en environnement de développement.

**Commandes de Contrôle (Terminal)**

Ces commandes s'exécutent directement dans l'interface de discussion de Claude Code.

``` /init ``` : Analyse l'arborescence du projet pour indexer les fichiers et établir le contexte.

``` /bug ``` : Initie une recherche automatisée d'anomalies dans la base de code actuelle.

``` /review ``` : Génère une analyse critique du code pour identifier des optimisations potentielles.

``` /test ``` : Produit et exécute des scripts de tests unitaires adaptés au projet.

``` /terminal ``` : Autorise l'IA à exécuter des commandes système (ex: gestionnaire de paquets).

``` /clear ``` : Réinitialise l'historique de la session pour libérer de la mémoire contextuelle.

``` /exit ``` : Met fin à la session et ferme l'application proprement.

**Sécurité et Confidentialité**

Méthodes de restriction d'accès et de contrôle des modifications.

Fichier .claudeignore : À placer à la racine. Permet d'exclure des fichiers ou répertoires spécifiques de l'analyse de l'IA (données sensibles, dépendances lourdes).

Mode Lecture Seule (--read-only) : Paramètre de lancement empêchant toute modification directe du système de fichiers par l'IA.

Mode Automatique (--dangerously-skip-permissions) : Désactive les demandes de confirmation avant modification. À utiliser avec une extrême vigilance.

**Structuration des Requêtes (Prompts)**

Pour obtenir des résultats précis, privilégiez les structures explicites.

Encapsulation : Utilisez les balises <code> ... </code> pour isoler les extraits de code.

Contraintes de format : Précisez explicitement le format de sortie souhaité (JSON, Tableau, Markdown).

Définition de rôle : Assignez une expertise spécifique à l'IA (ex: "Agis en tant qu'expert en sécurité informatique").

 **Raccourcis Système**

``` Ctrl + C ``` : Interrompt immédiatement la génération de texte ou l'exécution d'une tâche.

``` Ctrl + L ``` : Réinitialise l'affichage du terminal (clear).

``` Flèche Haut ```: Accède à l'historique des commandes précédentes.

``` Maj + Entrée ```: Insère un saut de ligne sans valider l'envoi de la requête (Interface Web).

Note de sécurité : L'utilisation d'un système de contrôle de version (Git) est impérative pour permettre la restauration du code en cas de modification non souhaitée.
