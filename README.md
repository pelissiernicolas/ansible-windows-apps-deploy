# ansible-windows-apps-deploy

Ce projet permet de déployer des applications sur des machines Windows via Ansible.

## Fonctionnalités
- Installation automatisée de plusieurs applications (ex : Google Chrome, Firefox, TightVNC)
- Gestion des fichiers MSI et MST pour les installations personnalisées
- Configuration de certains paramètres via des rôles dédiés

## Prérequis
- Ansible
- Accès WinRM configuré sur la machine cible
- Un fichier d'inventaire adapté (voir `inventory.ini`)

## Limites connues
- **L'installation et la configuration de TightVNC ne fonctionnent pas correctement à ce jour.**
- Certaines tâches sont désactivées/commentées dans les rôles pour éviter des erreurs.

## Utilisation
1. Adapter le fichier `inventory.ini` avec vos identifiants.
2. Modifier la liste des applications à installer dans `playbook.yml` si besoin.
3. Lancer le playbook :
   ```bash
   ansible-playbook -i inventory.ini playbook.yml
   ```

## Avertissement
Ce dépôt est fourni à titre d'exemple et n'est pas prêt pour un usage en production.
