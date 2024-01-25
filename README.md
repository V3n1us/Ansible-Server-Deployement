# Projekt

Dies ist das Projekt-Repository des Abschlussprojektes zur Ausbildung Fachinformatiker für Systemintegration von Jan Sulga zum Thema "Automatisierte Einrichtung eines Rootservers inklusive zweier Webapplikationen mittels Ansible".

Dieses Repository enthält einen Ansible Ordner mit den zugehörigen Ansible-Playbooks sowie, Projektordner der einzelnen Services.

## Reihenfolge Ausführung der Playbooks

1. Rootserver
    1. Prepare

        ``` shell
        ansible-playbook pb1_prepare.yml --ask-become-pass 
        ```

    2. Setup

        ```shell
        ansible-playbook pb2_setup.yml --ask-become-pass 
        ```

    3. Traefik

        ``` shell
        ansible-playbook pb3_traefik.yml --ask-become-pass 
        ```

2. Applikationen
   1. Directus

        ```shell
        ansible-playbook pb4_directus.yml 
        ```

   2. Passbolt

        ```shell
        ansible-playbook pb5_passbolt.yml
        ```
