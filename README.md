# MG-ANSSI-RECOM
Dans ce dépôt, vous pouvez trouver un rôle Ansible basé sur les directives de l'ANSSI. 
Ce rôle est conçu pour renforcer la sécurité d'un système Redhat.

Le rôle Ansible est une manière de regrouper des tâches Ansible liées, qui peuvent ensuite être réutilisées. 
Dans ce cas, le rôle est utilisé pour appliquer un ensemble de recommandations de sécurité sur un système Redhat selon les recommandation minimal et intermediaire Bp28

Pour utiliser ce rôle localement, vous devez utiliser un fichier `requirements.yml` et la commande `ansible-galaxy`.

#### requirements.yml
--- 
roles: 
```
- name: ANSSI-RECOM
    src: https://github.com/Simplon-AdminCloud-Bordeaux-2023-2025/MG-ANSSI-RECOM.git
    version: main
    scm: git

`ansible-galaxy install -r requirements.yml --force  -p path/to/your/playbook.yml`
```
---
## choix des tâches minimal-recom ou intermediaire-recom

Pour choisir une tâche, soit `minimale` soit `intermédiaire`, vous devez modifier *le fichier main.yml* qui se trouve dans le dossier des tâches (tasks). 

Ce fichier contient la liste des tâches à exécuter. 
Pour choisir une tâche spécifique, vous devez commenter ou décommenter les lignes correspondantes dans ce fichier.

*Notez que dans un fichier YAML, vous pouvez commenter une ligne en la précédant d'un caractère '#'. Pour décommenter une ligne, il suffit de supprimer ce caractère.*
