# Projekt

This is the project repository for the final project of the vocational training as an IT specialist for system integration by Jan Sulga, focusing on "Automated Setup of a Root Server Including Two Web Applications Using Ansible."

This repository includes an Ansible folder with the corresponding Ansible playbooks, as well as project folders for each of the individual services.

## Order of execution of the playbooks

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

2. Applications
   1. Directus

        ```shell
        ansible-playbook pb4_directus.yml 
        ```

   2. Passbolt

        ```shell
        ansible-playbook pb5_passbolt.yml
        ```
