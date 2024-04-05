# MG-ANSSI-RECOM
Dans ce dépôt, vous pouvez trouver un rôle Ansible basé sur les directives de l'ANSSI (Agence nationale de la sécurité des systèmes d'information française). Ce rôle est conçu pour renforcer la sécurité d'un système Redhat. Il appartient au profil minimal et intermediare BP28 de l'ANSSI.

Le rôle Ansible est une manière de regrouper des tâches Ansible liées, qui peuvent ensuite être réutilisées. 
Dans ce cas, le rôle est utilisé pour appliquer un ensemble de recommandations de sécurité sur un système Redhat.

Pour utiliser ce rôle localement, vous devez utiliser un fichier `requirements.yml` et la commande `ansible-galaxy`.
Le fichier requirements.yml est un fichier YAML qui spécifie quels rôles Ansible doivent être installés.
La commande ansible-galaxy est une commande Ansible qui vous permet de gérer (créer, supprimer, lister, etc.) les rôles Ansible.

# requirements.yml
---
roles:

- name: ANSSI-RECOM
    src: https://github.com/Simplon-AdminCloud-Bordeaux-2023-2025/MG-ANSSI-RECOM.git
    version: main
    scm: git

ansible-galaxy install -r requirements.yml --force  -p path/to/your/playbook.yml

### task minimal-recom ou intermediaire-recom

Pour choisir une tâche, soit minimale soit intermédiaire, vous devez modifier le fichier main.yml qui se trouve dans le dossier des tâches (tasks). Ce fichier contient la liste des tâches à exécuter. Pour choisir une tâche spécifique, vous devez commenter ou décommenter les lignes correspondantes dans ce fichier.
Par exemple, si vous voulez exécuter la tâche minimale, vous devez décommenter les lignes correspondantes et commenter les autres. De même, pour exécuter la tâche intermédiaire, vous devez décommenter les lignes correspondantes et commenter les autres.

Notez que dans un fichier YAML, vous pouvez commenter une ligne en la précédant d'un caractère '#'. Pour décommenter une ligne, il suffit de supprimer ce caractère.
