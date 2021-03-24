# pelorus-install


Prerequisites:
 - An OpenShift 3.11 or higher Environment (You need to have cluster administrator privileges)
 - A machine from which to run the install (usually your laptop) 
  - ansible (version 2.9 or higher)
  - git
  - Ansible module "kubernetes.core" (ansible-galaxy collection install kubernetes.core)

  - Cuenta GitHub y su token
  - Cuenta de Jira Cloud y su token
  - OCP cluster - Lab enviroment from RHPDS
    Ask for service enviroment:
      Workshops (High-Cost Worloads) -> "OpenShift 4.6 Workshop (Training)"   

Set ansible vault
  Procedure

<<<<<<< HEAD
    - Get from your OCP cluster the following variables:
      . Openshift API URL: <OCP_API_URL>
      . Openshift user with cluster admin privileges: <OCP_USER_CLUSTER_ADMIN>
      . Openshift password with cluster admin privileges: <OCP_PASSWORD_USER_CLUSTER_ADMIN>
      . Openshift apps domain: <OCP_APPS_DOMAIN>
=======
   - Descargar repo Git

   - Log into OCP cluster with account with administrator privileges
>>>>>>> ed581b901e41a2b0b44468ed7a1e0631f984996a

    - Download git repo https://github.com/fmenesesg/pelorus-install/
      . git clone https://github.com/fmenesesg/pelorus-install/

<<<<<<< HEAD
    - In the root of this repository edit "secret.yml" (password vault: r3dh4t1!) 
      . ansible-vault edit secret.yml
=======
      openshift_user: ""
      openshift_password: ""
      openshift_api_url: "https://api.cluster.com:6443"
      openshift_apps_domain: "apps.cluster.com"
>>>>>>> ed581b901e41a2b0b44468ed7a1e0631f984996a

      and edit the following lines with corresponding values:

      openshift_user: "<OCP_USER_CLUSTER_ADMIN>"
      openshift_password: "<OCP_PASSWORD_USER_CLUSTER_ADMIN>"
      openshift_api_url: "<OCP_API_URL>"
      openshift_apps_domain: "<OCP_APPS_DOMAIN>"

Execute the ansible playbook (password vault: r3dh4t1!)
- ansible-playbook site.yml -K --ask-vault 

In a few seconds, you will see a number of resources get created:

* Prometheus and Grafana operators
* The core Pelorus stack, which includes:
  * A `Prometheus` instance
  * A `Grafana` instance
  * A `ServiceMonitor` instance for scraping the Pelorus exporters.
  * A `GrafanaDatasource` pointing to Prometheus.
  * A set of `GrafanaDashboards`. See the [dashboards documentation](/docs/Dashboards.md) for more details.
* The following exporters:
  * Deploy Time

