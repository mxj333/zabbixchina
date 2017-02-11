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
    * [Alert](manual/api/reference/alert.md)
      * [&gt; Alert object](manual/api/reference/alert/object.md)
      * [alert.get](manual/api/reference/alert/get.md)
    * [API info](manual/api/reference/apiinfo.md)
      * [apiinfo.version](manual/api/reference/apiinfo/version.md)
    * [Application](manual/api/reference/application.md)
      * [&gt; Application object](manual/api/reference/application/object.md)
      * [application.create](manual/api/reference/application/create.md)
      * [application.delete](manual/api/reference/application/delete.md)
      * [application.get](manual/api/reference/application/get.md)
      * [application.massadd](manual/api/reference/application/massadd.md)
      * [application.update](manual/api/reference/application/update.md)
    * [Configuration](manual/api/reference/configuration.md)
      * [configuration.export](manual/api/reference/configuration/export.md)
      * [configuration.import](manual/api/reference/configuration/import.md)
    * [Correlation](manual/api/reference/correlation.md)
      * [&gt; Correlation object](manual/api/reference/correlation/object.md)
      * [correlation.create](manual/api/reference/correlation/create.md)
      * [correlation.delete](manual/api/reference/correlation/delete.md)
      * [correlation.get](manual/api/reference/correlation/get.md)
      * [correlation.update](manual/api/reference/correlation/update.md)
    * [Discovered host](manual/api/reference/dhost.md)
      * [&gt; Discovered host object](manual/api/reference/dhost/object.md)
      * [dhost.get](manual/api/reference/dhost/get.md)
    * [Discovered service](manual/api/reference/dservice.md)
      * [&gt; Discovered service object](manual/api/reference/dservice/object.md)
      * [dservice.get](manual/api/reference/dservice/get.md)
    * [Discovery check](manual/api/reference/dcheck.md)
      * [&gt; Discovery check object](manual/api/reference/dcheck/object.md)
      * [dcheck.get](manual/api/reference/dcheck/get.md)
    * [Discovery rule](manual/api/reference/drule.md)
      * [&gt; Discovery rule object](manual/api/reference/drule/object.md)
      * [drule.create](manual/api/reference/drule/create.md)
      * [drule.delete](manual/api/reference/drule/delete.md)
      * [drule.get](manual/api/reference/drule/get.md)
      * [drule.isreadable](manual/api/reference/drule/isreadable.md)
      * [drule.iswritable](manual/api/reference/drule/iswritable.md)
      * [drule.update](manual/api/reference/drule/update.md)
    * [Event](manual/api/reference/event.md)
      * [&gt; Event object](manual/api/reference/event/object.md)
      * [event.acknowledge](manual/api/reference/event/acknowledge.md)
      * [event.get](manual/api/reference/event/get.md)
    * [Graph](manual/api/reference/graph.md)
      * [&gt; Graph object](manual/api/reference/graph/object.md)
      * [graph.create](manual/api/reference/graph/create.md)
      * [graph.delete](manual/api/reference/graph/delete.md)
      * [graph.get](manual/api/reference/graph/get.md)
      * [graph.update](manual/api/reference/graph/update.md)
    * [Graph item](manual/api/reference/graphitem.md)
      * [&gt; Graph item object](manual/api/reference/graphitem/object.md)
      * [graphitem.get](manual/api/reference/graphitem/get.md)
    * [Graph prototype](manual/api/reference/graphprototype.md)
      * [&gt; Graph prototype object](manual/api/reference/graphprototype/object.md)
      * [graphprototype.create](manual/api/reference/graphprototype/create.md)
      * [graphprototype.delete](manual/api/reference/graphprototype/delete.md)
      * [graphprototype.get](manual/api/reference/graphprototype/get.md)
      * [graphprototype.update](manual/api/reference/graphprototype/update.md)
    * [History](manual/api/reference/history.md)
      * [&gt; History object](manual/api/reference/history/object.md)
      * [history.get](manual/api/reference/history/get.md)
    * [Host](manual/api/reference/host.md)
      * [&gt; Host object](manual/api/reference/host/object.md)
      * [host.create](manual/api/reference/host/create.md)
      * [host.delete](manual/api/reference/host/delete.md)
      * [host.get](manual/api/reference/host/get.md)
      * [host.isreadable](manual/api/reference/host/isreadable.md)
      * [host.iswritable](manual/api/reference/host/iswritable.md)
      * [host.massadd](manual/api/reference/host/massadd.md)
      * [host.massremove](manual/api/reference/host/massremove.md)
      * [host.massupdate](manual/api/reference/host/massupdate.md)
      * [host.update](manual/api/reference/host/update.md)
    * [Host group](manual/api/reference/hostgroup.md)
      * [&gt; Host group object](manual/api/reference/hostgroup/object.md)
      * [hostgroup.create](manual/api/reference/hostgroup/create.md)
      * [hostgroup.delete](manual/api/reference/hostgroup/delete.md)
      * [hostgroup.get](manual/api/reference/hostgroup/get.md)
      * [hostgroup.isreadable](manual/api/reference/hostgroup/isreadable.md)
      * [hostgroup.iswritable](manual/api/reference/hostgroup/iswritable.md)
      * [hostgroup.massadd](manual/api/reference/hostgroup/massadd.md)
      * [hostgroup.massremove](manual/api/reference/hostgroup/massremove.md)
      * [hostgroup.massupdate](manual/api/reference/hostgroup/massupdate.md)
      * [hostgroup.update](manual/api/reference/hostgroup/update.md)
    * [Host interface](manual/api/reference/hostinterface.md)
      * [&gt; Host interface object](manual/api/reference/hostinterface/object.md)
      * [hostinterface.create](manual/api/reference/hostinterface/create.md)
      * [hostinterface.delete](manual/api/reference/hostinterface/delete.md)
      * [hostinterface.get](manual/api/reference/hostinterface/get.md)
      * [hostinterface.massadd](manual/api/reference/hostinterface/massadd.md)
      * [hostinterface.massremove](manual/api/reference/hostinterface/massremove.md)
      * [hostinterface.replacehostinterfaces](manual/api/reference/hostinterface/replacehostinterfaces.md)
      * [hostinterface.update](manual/api/reference/hostinterface/update.md)
    * [Host prototype](manual/api/reference/hostprototype.md)
      * [&gt; Host prototype object](https://www.zabbix.com/documentation/3.2/manual/api/reference/hostprototype/object)

      * [hostprototype.create](https://www.zabbix.com/documentation/3.2/manual/api/reference/hostprototype/create)

      * [hostprototype.delete](https://www.zabbix.com/documentation/3.2/manual/api/reference/hostprototype/delete)

      * [hostprototype.get](https://www.zabbix.com/documentation/3.2/manual/api/reference/hostprototype/get)

      * [hostprototype.isreadable](https://www.zabbix.com/documentation/3.2/manual/api/reference/hostprototype/isreadable)

      * [hostprototype.iswritable](https://www.zabbix.com/documentation/3.2/manual/api/reference/hostprototype/iswritable)

      * [hostprototype.update](https://www.zabbix.com/documentation/3.2/manual/api/reference/hostprototype/update)

  * [Appendix 1. Reference commentary](manual/api/reference_commentary.md)

  * [Appendix 2. Changes from 3.0 to 3.2](manual/api/changes_3.0_-_3.2.md)

  * [Zabbix API changes in 3.2](manual/api/changes_3.2.md)

* [Appendixes](manual/appendix.md)

  * 



