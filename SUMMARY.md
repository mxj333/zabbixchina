# Summary

* [简介](README.md)

  * [1 Manual structure](manual/introduction/manual_structure.md)
  * 2 What is Zabbix
  * 3 Zabbix features
  * 4 Zabbix overview
  * 5 What's new in Zabbix 3.2.0
  * 6 What's new in Zabbix 3.2.1
  * 7 What's new in Zabbix 3.2.2
  * 8 What's new in Zabbix 3.2.3
  * 9 What's new in Zabbix 3.2.4

* [2. Zabbix concepts](manual/concepts/README.md)

  * [1 Zabbix definitions](manual/concepts/definitions.md)
  * [2 Server](format/introduction.md)
  * [3 Agent](format/chapters.md)
  * [4 Proxy](format/markdown.md)
  * [5 Java gateway](manual/concepts/java.md)
  * [6 Sender](format/cover.md)
  * [7 Get](format/languages.md)

* [3. Installation](manual/installation/index.md)

  * [1 Getting Zabbix](manual/installation/getting_zabbix.md)
  * [2 Requirements](manual/installation/requirements.md)
  * [3 Installation from packages](manual/installation/install_from_packages.md)
    * [1 Repository installation](manual/installation/install_from_packages/repository_installation.md)
    * [2 Server installation with MySQL database](manual/installation/install_from_packages/server_installation_with_mysql.md)
    * [3 Server installation with PostgreSQL database](manual/installation/install_from_packages/server_installation_with_postgresql.md)
    * [4 Agent installation](manual/installation/install_from_packages/agent_installation.md)
    * [5 Proxy installation](manual/installation/install_from_packages/proxy_installation.md)
  * [4 Installation from sources](manual/installation/install.md)
  * [5 Installation from containers](manual/installation/containers.md)
  * [6 Upgrade procedure](manual/installation/upgrade.md)
  * [7 Known issues](manual/installation/known_issues.md)
  * [8 Template changes](manual/installation/template_changes)
  * [9 Upgrade notes for 3.2.0](manual/installation/upgrade_notes_320)
  * [10 Upgrade notes for 3.2.2](manual/installation/upgrade_notes_322.md)
  * [11 Upgrade notes for 3.2.3](manual/installation/upgrade_notes_323.md)
  * [12 Upgrade notes for 3.2.4](manual/installation/upgrade_notes_324.md)

* [4. Quickstart](manual/quickstart.md)

  * [1 Login and configuring user](manual/quickstart/login.md)
  * [2 New host](manual/quickstart/host.md)
  * [3 New item](manual/quickstart/item.md)
  * [4 New trigger](manual/quickstart/trigger.md)
  * [5 Receiving problem notification](manual/quickstart/notification.md)
  * [6 New template](manual/quickstart/template.md)

* [5. Zabbix appliance](manual/appliance.md.md)

* [6. Configuration](manual/config.md)

  * [1 Hosts and host groups](manual/config/hosts.md)
  * [2 Items](manual/config/items.md)
  * [3 Triggers](manual/config/triggers.md)
  * [4 Events](manual/config/events.md)
  * [5 Event correlation](manual/config/event_correlation.md)
  * [6 Visualisation](manual/config/visualisation.md)
  * [7 Templates](manual/config/templates.md)
  * [8 Notifications upon events](manual/config/notifications.md)
  * [9 Macros](manual/config/macros.md)
  * [10 Users and user groups](manual/config/users_and_usergroups.md)

* [7. IT services](manual/it_services.md)

* [8. Web monitoring](manual/web_monitoring.md)

  * [1 Web monitoring items](manual/web_monitoring/items.md)
  * [2 Real life scenario](manual/web_monitoring/example.md)

* [9. Virtual machine monitoring](manual/vm_monitoring.md)

  * [Virtual machine discovery key fields](manual/vm_monitoring/discovery_fields.md)

* [10. Maintenance](manual/maintenance.md)

* [11. Regular expressions](manual/regular_expressions.md)

* [12. Event acknowledgment](manual/acknowledges.md)

* [13. Configuration export/import](manual/xml_export_import.md)

  * [Groups](manual/xml_export_import/groups.md)
  * [Hosts](manual/xml_export_import/hosts.md)

* [14. Discovery](manual/discovery.md)

  * [1 Network discovery](manual/discovery/network_discovery.md)
    * [Configuring a network discovery](manual/discovery/network_discovery/rule.md)
  * [2 Active agent auto-registration](manual/discovery/auto_registration.md)
  * [3 Low-level discovery](manual/discovery/low_level_discovery.md)
    * [Notes on low-level discovery](manual/discovery/low_level_discovery/notes.md)

* [15. Distributed monitoring](manual/distributed_monitoring.md)

  * [1 Proxies](manual/distributed_monitoring/proxies.md)

* [16. Encryption](manual/encryption.md)

  * [1 Using certificates](manual/encryption/using_certificates.md)
  * [2 Using pre-shared keys](manual/encryption/using_pre_shared_keys.md)
  * [3 Troubleshooting](manual/encryption/troubleshooting.md)
    * [1 Connection type or permission problems](manual/encryption/troubleshooting/connection_permission_problems.md)
    * [2 Certificate problems](manual/encryption/troubleshooting/certificate_problems.md)
    * [3 PSK problems](manual/encryption/troubleshooting/psk_problems.md)

* [17. Web interface](manual/web_interface.md)

  * [1 Frontend sections](manual/web_interface/frontend_sections.md)

    * [1 Monitoring](manual/web_interface/frontend_sections/monitoring.md)
      * [1 Dashboard](manual/web_interface/frontend_sections/monitoring/dashboard.md)
      * [2 Problems](manual/web_interface/frontend_sections/monitoring/problems.md)
      * [3 Overview](manual/web_interface/frontend_sections/monitoring/overview.md)
      * [4 Web](manual/web_interface/frontend_sections/monitoring/web.md)
      * [5 Latest data](manual/web_interface/frontend_sections/monitoring/latest_data.md)
      * [6 Triggers](manual/web_interface/frontend_sections/monitoring/triggers.md)
      * [7 Graphs](manual/web_interface/frontend_sections/monitoring/graphs.md)
      * [8 Screens](manual/web_interface/frontend_sections/monitoring/screens.md)
      * [9 Maps](manual/web_interface/frontend_sections/monitoring/maps.md)
      * [10 Discovery](manual/web_interface/frontend_sections/monitoring/discovery.md)
      * [11 IT services](manual/web_interface/frontend_sections/monitoring/it_services.md)
    * [2 Inventory](manual/web_interface/frontend_sections/inventory.md)
      * [1 Overview](manual/web_interface/frontend_sections/inventory/overview.md)
      * [2 Hosts](manual/web_interface/frontend_sections/inventory/hosts.md)
    * [3 Reports](manual/web_interface/frontend_sections/reports.md)
      * [1 Status of Zabbix](manual/web_interface/frontend_sections/reports/status_of_zabbix.md)
      * [2 Availability report](manual/web_interface/frontend_sections/reports/availability.md)
      * [3 Trigers top 100](manual/web_interface/frontend_sections/reports/triggers_top.md)
      * [4 Audit](manual/web_interface/frontend_sections/reports/audit.md)
      * [5 Action log](manual/web_interface/frontend_sections/reports/action_log.md)
      * [6 Notifications](manual/web_interface/frontend_sections/reports/notifications.md)
    * [4 Configuration](manual/web_interface/frontend_sections/configuration.md)
      * [1 Host groups](manual/web_interface/frontend_sections/configuration/hostgroups.md)
      * [2 Templates](manual/web_interface/frontend_sections/configuration/templates.md)
      * [3 Hosts](manual/web_interface/frontend_sections/configuration/hosts.md)
        * [1 Applications](manual/web_interface/frontend_sections/configuration/hosts/applications.md)
        * [2 Items](manual/web_interface/frontend_sections/configuration/hosts/items.md)
        * [3 Triggers](manual/web_interface/frontend_sections/configuration/hosts/triggers.md)
        * [4 Graphs](manual/web_interface/frontend_sections/configuration/hosts/graphs.md)
        * [5 Discovery rules](manual/web_interface/frontend_sections/configuration/hosts/discovery.md)
        * [6 Web scenarios](manual/web_interface/frontend_sections/configuration/hosts/web.md)
      * [4 Maintenance](manual/web_interface/frontend_sections/configuration/maintenance.md)
      * [5 Actions](manual/web_interface/frontend_sections/configuration/actions.md)
      * [6 Event correlation](manual/web_interface/frontend_sections/configuration/correlation.md)
      * [7 Discovery](manual/web_interface/frontend_sections/configuration/discovery.md)
      * [8 IT services](manual/web_interface/frontend_sections/configuration/itservices.md)
    * [5 Administration](manual/web_interface/frontend_sections/administration.md)
      * [1 General](manual/web_interface/frontend_sections/administration/general.md)
      * [2 Proxies](manual/web_interface/frontend_sections/administration/proxies.md)
      * [3 Authentication](manual/web_interface/frontend_sections/administration/authentication.md)
      * [4 User groups](manual/web_interface/frontend_sections/administration/user_groups.md)
      * [5 Users](manual/web_interface/frontend_sections/administration/users.md)
      * [6 Media types](manual/web_interface/frontend_sections/administration/mediatypes.md)
      * [7 Scripts](manual/web_interface/frontend_sections/administration/scripts.md)
      * [8 Queue](manual/web_interface/frontend_sections/administration/queue.md)

  * [2 User profile](manual/web_interface/user_profile.md)

    * [1 Global notifications](manual/web_interface/user_profile/global_notifications.md)
    * [2 Sound in browsers](manual/web_interface/user_profile/sound.md)

  * [3 Global search](manual/web_interface/global_search.md)

  * [4 Frontend maintenance mode](manual/web_interface/maintenance_mode.md)

  * [5 Page parameters](manual/web_interface/page_parameters.md)

  * [6 Definitions](manual/web_interface/definitions.md)

  * [7 Creating your own theme](manual/web_interface/theming.md)

* [18. API](manual/api.md)

  * [Method reference](manual/api/reference.md)
    * [Action](manual/api/reference/action.md)
      * [&gt; Action object](manual/api/reference/action/object.md)
      * [action.create](manual/api/reference/action/create.md)
      * [action.delete](manual/api/reference/action/delete.md)
      * [action.get](manual/api/reference/action/get.md)
      * [action.update](manual/api/reference/action/update.md)
    * [Alert](https://www.zabbix.com/documentation/3.2/manual/api/reference/alert)
      * [&gt; Alert object](https://www.zabbix.com/documentation/3.2/manual/api/reference/alert/object)
      * [alert.get](https://www.zabbix.com/documentation/3.2/manual/api/reference/alert/get)
    * [API info](https://www.zabbix.com/documentation/3.2/manual/api/reference/apiinfo)
      * [apiinfo.version](https://www.zabbix.com/documentation/3.2/manual/api/reference/apiinfo/version)
    * [Application](https://www.zabbix.com/documentation/3.2/manual/api/reference/application)
      * [&gt; Application object](https://www.zabbix.com/documentation/3.2/manual/api/reference/application/object)
      * [application.create](https://www.zabbix.com/documentation/3.2/manual/api/reference/application/create)
    * [application.delete](https://www.zabbix.com/documentation/3.2/manual/api/reference/application/delete)
    * [application.get](https://www.zabbix.com/documentation/3.2/manual/api/reference/application/get)
    * [application.massadd](https://www.zabbix.com/documentation/3.2/manual/api/reference/application/massadd)
    * [application.update](https://www.zabbix.com/documentation/3.2/manual/api/reference/application/update)
    * [Configuration](https://www.zabbix.com/documentation/3.2/manual/api/reference/configuration)
    * [configuration.export](https://www.zabbix.com/documentation/3.2/manual/api/reference/configuration/export)
    * [configuration.import](https://www.zabbix.com/documentation/3.2/manual/api/reference/configuration/import)
    * [Correlation](https://www.zabbix.com/documentation/3.2/manual/api/reference/correlation)
    * [&gt; Correlation object](https://www.zabbix.com/documentation/3.2/manual/api/reference/correlation/object)
    * [correlation.create](https://www.zabbix.com/documentation/3.2/manual/api/reference/correlation/create)
    * [correlation.delete](https://www.zabbix.com/documentation/3.2/manual/api/reference/correlation/delete)
    * [correlation.get](https://www.zabbix.com/documentation/3.2/manual/api/reference/correlation/get)
    * [correlation.update](https://www.zabbix.com/documentation/3.2/manual/api/reference/correlation/update)
    * [Discovered host](https://www.zabbix.com/documentation/3.2/manual/api/reference/dhost)
    * [&gt; Discovered host object](https://www.zabbix.com/documentation/3.2/manual/api/reference/dhost/object)
    * [dhost.get](https://www.zabbix.com/documentation/3.2/manual/api/reference/dhost/get)
    * [Discovered service](https://www.zabbix.com/documentation/3.2/manual/api/reference/dservice)
    * [&gt; Discovered service object](https://www.zabbix.com/documentation/3.2/manual/api/reference/dservice/object)
    * [dservice.get](https://www.zabbix.com/documentation/3.2/manual/api/reference/dservice/get)
    * [Discovery check](https://www.zabbix.com/documentation/3.2/manual/api/reference/dcheck)
    * [&gt; Discovery check object](https://www.zabbix.com/documentation/3.2/manual/api/reference/dcheck/object)
    * [dcheck.get](https://www.zabbix.com/documentation/3.2/manual/api/reference/dcheck/get)
    * 
  * [Appendix 1. Reference commentary](manual/api/reference_commentary.md)
  * [Appendix 2. Changes from 3.0 to 3.2](manual/api/changes_3.0_-_3.2.md)
  * [Zabbix API changes in 3.2](manual/api/changes_3.2.md)

* [Appendixes](manual/appendix.md)

  * 


