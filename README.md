# pelorus-install

Prerequisitos:
  - ansible (version 2.9)
  - Cuenta GitHub y su token
  - Cuenta de Jira Cloud y su token
  - OCP cluster - Lab enviroment from RHPDS
    Ask for service enviroment:
      Workshops (High-Cost Worloads) -> "OpenShift 4.6 Workshop (Training)"   

Credenciales de usuario

  - Configurar ansible vault

  Prerequisites

      You have cluster administrator privileges.

  Procedure

    - Descargar repo Git

    - Log into OCP cluster with account with administrator privileges

    ansible-vault edit secret.yml

      openshift_user: "opentlc-mgr"
      openshift_password: "r3dh4t1!"
      openshift_api_url: "https://api.cluster-7998.7998.example.opentlc.com:6443"
      openshift_apps_domain: "apps.cluster-7998.7998.example.opentlc.com"


Paso a paso --> usar base del de install pelorus
  - Ejecución del playbook
    ansible-playbook site.yml -K --ask-vault -vvv




