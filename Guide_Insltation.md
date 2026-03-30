# 🧌 Installation de Claude Code #

**1\. Installer Ollama**

**Sur Mac :** Ouvre ton terminal et tape ça :
> ```
> brew install ollama
> brew services start ollama
> ```

puis ça :

> ```
> ollama pull qwen2.5-coder:7b
> ```

**Sur Windows :** Ouvre ton terminal (Admin ) et tape ça :

> ```
> winget install ollama.ollama
> ollama pull qwen2.5-coder:7b
> ```

**Sur Linux :** 

> ```
> curl -fsSL [https://ollama.com/install.sh](https://ollama.com/install.sh) | sh
> ollama pull qwen2.5-coder:7b
> ```

**2\. Installer Node.js ( si tu ne la pas )**

**Sur Mac :** ``` brew install node ```

**Sur Windows :** ``` winget install OpenJS.NodeJS.LTS ```

**Sur Linux :** ``` #Pour Ubuntu/Debian
sudo apt update && sudo apt install nodejs npm ```

**3\. Installer Claude Code**

**Sur Mac :**

> ```
> sudo npm install -g @anthropic-ai/claude-code
> ```

**Sur Windows :**

> ```
> npm install -g @anthropic-ai/claude-code
> ```

**Sur Linux :**

> ```
> sudo npm install -g @anthropic-ai/claude-code
> ```


**4\. Lié Claude à Ollama** 

**Sur Mac :**

> ```
> echo 'export ANTHROPIC\_AUTH\_TOKEN=ollama' >> ~/.zshrc && echo 'export ANTHROPIC\_BASE\_URL="http://localhost:11434"' >> ~/.zshrc && source ~/.zshrc
> ```

**Sur Windows :**

> ```
> \[System.Environment\]::SetEnvironmentVariable('ANTHROPIC\_AUTH\_TOKEN', 'ollama', 'User')
> \[System.Environment\]::SetEnvironmentVariable('ANTHROPIC\_BASE\_U
> RL', 'http://localhost:11434', 'User') 
> ```

**Sur Linux :**

> ```
> # Ajoute la config à ton profil (bash ou zsh)
> echo 'export ANTHROPIC_AUTH_TOKEN=ollama' >> ~/.bashrc
> echo 'export ANTHROPIC_BASE_URL="http://localhost:11434"' >> ~/.bashrc
> source ~/.bashrc
> ```



**5\. Utilisation dans VS Code**

Maintenant, ouvre ton projet dans **VS Code**.

1.  Ouvre le terminal en bas (Ctrl + ù ou via le menu **Terminal**).
2.  Lance la machine :
> ``` 
> claude --model qwen2.5-coder:7b 
> ``` 

### 🦧 AVERTISSEMENT : INSTALLATION CLAUDE CODE + OLLAMA ###

**1\. RESPONSABILITÉ DE L'UTILISATEUR** En installant ces outils, vous devenez seul responsable des modifications effectuées sur votre ordinateur. L'IA (Claude Code) est un automate capable de lire, créer, modifier ou supprimer des fichiers. **Ne lancez jamais une commande suggérée par l'IA sans la comprendre.**

**2\. PROTECTION DES DONNÉES**

*   **Mode Local :** En configurant l'adresse ``` http://localhost:11434 ```, votre code source et vos données **ne quittent jamais votre machine**. Aucune donnée n'est envoyée chez Anthropic ou des tiers pour l'entraînement.
    
*   **Vigilance :** Même en local, évitez de laisser des mots de passe ou des clés API en texte clair dans vos fichiers. L'IA y a accès pour son analyse.
    

**3\. RISQUES TECHNIQUES**

*   **Erreurs de Code :** L'IA peut "halluciner" (inventer) des solutions fausses ou obsolètes. Testez toujours le code dans un environnement sécurisé.
    
*   **Ressources Système :** Faire tourner un modèle de 7B paramètres (Qwen) sollicite énormément le processeur et la batterie. Surveillez la température de votre matériel.
    
*   **Sauvegardes :** Il est **impératif** d'utiliser un système de versioning (comme Git) ou de faire des copies de sauvegarde avant de laisser l'IA modifier vos dossiers.
    

**4\. SÉCURITÉ RÉSEAU** L'installation via ```npm```, ```brew``` ou ```winget``` télécharge des paquets depuis internet. Utilisez uniquement les sources officielles citées dans ce guide pour éviter tout logiciel malveillant.


---
Hadi 😘
