# pelorus-install

Prerequisitos:
  - ansible (version ?)
  - httpd-tools package
  - Cuenta GitHub y su token
  - Cuenta de Jira Cloud y su token
  - OCP cluster - Lab enviroment from RHPDS
    Ask for service enviroment:
      Workshops (High-Cost Worloads) -> "OpenShift 4.6 Workshop (Training)"   

Manejo de usuario (agregar pelorus-admin a htpass actual)


  Prerequisites

      You have created a Secret object that contains the HTPasswd user file. This procedure assumes that it is named htpass-secret.

      You have configured an HTPasswd identity provider. This procedure assumes that it is named my_htpasswd_provider.

      You have access to the htpasswd utility. On Red Hat Enterprise Linux this is available by installing the httpd-tools package.

      You have cluster administrator privileges.

  Procedure

    - Descargar repo Git

    - Log into OCP cluster with account with administrator privileges

    - Retrieve the HTPasswd file from the htpass-secret Secret object and save the file to your file system:
      $ oc get secret htpass-secret -ojsonpath={.data.htpasswd} -n openshift-config | base64 -d > users.htpasswd

Paso a paso --> usar base del de install pelorus
  - Ejecución del playbook



