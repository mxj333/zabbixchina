# [Zabbix documentation](https://www.zabbix.com/documentation/3.2/start)

* [Zabbix Manual](https://www.zabbix.com/documentation/3.2/manual)

  * [1. Introduction](https://www.zabbix.com/documentation/3.2/manual/introduction)
  * [2. Zabbix concepts](https://www.zabbix.com/documentation/3.2/manual/concepts)
  * [3. Installation](https://www.zabbix.com/documentation/3.2/manual/installation)
    * [1 Getting Zabbix](https://www.zabbix.com/documentation/3.2/manual/installation/getting_zabbix)
    * [2 Requirements](https://www.zabbix.com/documentation/3.2/manual/installation/requirements)
    * [3 Installation from packages](https://www.zabbix.com/documentation/3.2/manual/installation/install_from_packages)
      * [1 Repository installation](https://www.zabbix.com/documentation/3.2/manual/installation/install_from_packages/repository_installation)
      * [2 Server installation with MySQL database](https://www.zabbix.com/documentation/3.2/manual/installation/install_from_packages/server_installation_with_mysql)
      * [3 Server installation with PostgreSQL database](https://www.zabbix.com/documentation/3.2/manual/installation/install_from_packages/server_installation_with_postgresql)
      * [4 Agent installation](https://www.zabbix.com/documentation/3.2/manual/installation/install_from_packages/agent_installation)
      * [5 Proxy installation](https://www.zabbix.com/documentation/3.2/manual/installation/install_from_packages/proxy_installation)
    * [4 Installation from sources](https://www.zabbix.com/documentation/3.2/manual/installation/install)
    * [5 Installation from containers](https://www.zabbix.com/documentation/3.2/manual/installation/containers)
    * [6 Upgrade procedure](https://www.zabbix.com/documentation/3.2/manual/installation/upgrade)
    * [7 Known issues](https://www.zabbix.com/documentation/3.2/manual/installation/known_issues)
    * [8 Template changes](https://www.zabbix.com/documentation/3.2/manual/installation/template_changes)
    * [9 Upgrade notes for 3.2.0](https://www.zabbix.com/documentation/3.2/manual/installation/upgrade_notes_320)
    * [10 Upgrade notes for 3.2.2](https://www.zabbix.com/documentation/3.2/manual/installation/upgrade_notes_322)
    * [11 Upgrade notes for 3.2.3](https://www.zabbix.com/documentation/3.2/manual/installation/upgrade_notes_323)
    * [12 Upgrade notes for 3.2.4](https://www.zabbix.com/documentation/3.2/manual/installation/upgrade_notes_324)
  * [4. Quickstart](https://www.zabbix.com/documentation/3.2/manual/quickstart)
    * [1 Login and configuring user](https://www.zabbix.com/documentation/3.2/manual/quickstart/login)
    * [2 New host](https://www.zabbix.com/documentation/3.2/manual/quickstart/host)
    * [3 New item](https://www.zabbix.com/documentation/3.2/manual/quickstart/item)
    * [4 New trigger](https://www.zabbix.com/documentation/3.2/manual/quickstart/trigger)
    * [5 Receiving problem notification](https://www.zabbix.com/documentation/3.2/manual/quickstart/notification)
    * [6 New template](https://www.zabbix.com/documentation/3.2/manual/quickstart/template)
  * [5. Zabbix appliance](https://www.zabbix.com/documentation/3.2/manual/appliance)
    * [6. Configuration](https://www.zabbix.com/documentation/3.2/manual/config)
      * [1 Hosts and host groups](https://www.zabbix.com/documentation/3.2/manual/config/hosts)
        * [1 Configuring a host](https://www.zabbix.com/documentation/3.2/manual/config/hosts/host)
        * [2 Inventory](https://www.zabbix.com/documentation/3.2/manual/config/hosts/inventory)
        * [3 Mass update](https://www.zabbix.com/documentation/3.2/manual/config/hosts/hostupdate)
      * [2 Items](https://www.zabbix.com/documentation/3.2/manual/config/items)
        * [1 Creating an item](https://www.zabbix.com/documentation/3.2/manual/config/items/item)
          * [1 Item key](https://www.zabbix.com/documentation/3.2/manual/config/items/item/key)
          * [2 Custom intervals](https://www.zabbix.com/documentation/3.2/manual/config/items/item/custom_intervals)
        * [2 Item types](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes)
          * [1 Zabbix agent](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/zabbix_agent)
            * [Windows-specific item keys](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/zabbix_agent/win_keys)
          * [2 SNMP agent](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/snmp)
            * [2 Special OIDs](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/snmp/special_mibs)
            * [6.1 Dynamic indexes](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/snmp/dynamicindex)
          * [3 SNMP traps](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/snmptrap)
          * [4 IPMI checks](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/ipmi)
          * [5 Simple checks](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/simple_checks)
            * [1 VMware monitoring item keys](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/simple_checks/vmware_keys)
          * [6 Log file monitoring](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/log_items)
          * [7 Calculated items](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/calculated)
          * [8 Internal checks](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/internal)
          * [9 SSH checks](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/ssh_checks)
          * [10 Telnet checks](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/telnet_checks)
          * [11 External checks](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/external)
          * [12 Aggregate checks](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/aggregate)
          * [13 Trapper items](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/trapper)
          * [14 JMX monitoring](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/jmx_monitoring)
          * [15 ODBC monitoring](https://www.zabbix.com/documentation/3.2/manual/config/items/itemtypes/odbc_checks)
        * [3 History and trends](https://www.zabbix.com/documentation/3.2/manual/config/items/history_and_trends)
        * [4 User parameters](https://www.zabbix.com/documentation/3.2/manual/config/items/userparameters)
          * [1 Extending Zabbix agents](https://www.zabbix.com/documentation/3.2/manual/config/items/userparameters/extending_agent)
        * [5 Loadable modules](https://www.zabbix.com/documentation/3.2/manual/config/items/loadablemodules)
        * [6 Windows performance counters](https://www.zabbix.com/documentation/3.2/manual/config/items/perfcounters)
        * [6.7 Mass update](https://www.zabbix.com/documentation/3.2/manual/config/items/itemupdate)
        * [8 Value mapping](https://www.zabbix.com/documentation/3.2/manual/config/items/mapping)
        * [9 Applications](https://www.zabbix.com/documentation/3.2/manual/config/items/applications)
        * [10 Queue](https://www.zabbix.com/documentation/3.2/manual/config/items/queue)
        * [11 Value cache](https://www.zabbix.com/documentation/3.2/manual/config/items/value_cache)
      * [3 Triggers](https://www.zabbix.com/documentation/3.2/manual/config/triggers)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [1 Configuring a trigger](https://www.zabbix.com/documentation/3.2/manual/config/triggers/trigger)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [2 Trigger expression](https://www.zabbix.com/documentation/3.2/manual/config/triggers/expression)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [3 Trigger dependencies](https://www.zabbix.com/documentation/3.2/manual/config/triggers/dependencies)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [4 Trigger severity](https://www.zabbix.com/documentation/3.2/manual/config/triggers/severity)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [5 Customising trigger severities](https://www.zabbix.com/documentation/3.2/manual/config/triggers/customseverities)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [6 Unit symbols](https://www.zabbix.com/documentation/3.2/manual/config/triggers/suffixes)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [7 Mass update](https://www.zabbix.com/documentation/3.2/manual/config/triggers/update)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [8 Predictive trigger functions](https://www.zabbix.com/documentation/3.2/manual/config/triggers/prediction)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/joinbottom.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [9 Event tags](https://www.zabbix.com/documentation/3.2/manual/config/triggers/event_tags)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        [![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/minus.gif)](javascript: indexmenu_3375628257f69b0b3e631.o(95);)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/folderhopen.gif)

        [4 Events](https://www.zabbix.com/documentation/3.2/manual/config/events)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [1 Event sources](https://www.zabbix.com/documentation/3.2/manual/config/events/sources)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/joinbottom.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [2 Manual closing of problems](https://www.zabbix.com/documentation/3.2/manual/config/events/manual_close)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/folderh.gif)

        [5 Event correlation](https://www.zabbix.com/documentation/3.2/manual/config/event_correlation)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        [![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/minus.gif)](javascript: indexmenu_3375628257f69b0b3e631.o(99);)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/folderhopen.gif)

        [6 Visualisation](https://www.zabbix.com/documentation/3.2/manual/config/visualisation)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        [![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/minus.gif)](javascript: indexmenu_3375628257f69b0b3e631.o(100);)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/folderhopen.gif)

        [1 Graphs](https://www.zabbix.com/documentation/3.2/manual/config/visualisation/graphs)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [1 Simple graphs](https://www.zabbix.com/documentation/3.2/manual/config/visualisation/graphs/simple)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [2 Custom graphs](https://www.zabbix.com/documentation/3.2/manual/config/visualisation/graphs/custom)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/joinbottom.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [3 Ad-hoc graphs](https://www.zabbix.com/documentation/3.2/manual/config/visualisation/graphs/adhoc)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        [![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/minus.gif)](javascript: indexmenu_3375628257f69b0b3e631.o(104);)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/folderhopen.gif)

        [2 Network maps](https://www.zabbix.com/documentation/3.2/manual/config/visualisation/maps)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [1 Configuring a network map](https://www.zabbix.com/documentation/3.2/manual/config/visualisation/maps/map)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/joinbottom.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [2 Link indicators](https://www.zabbix.com/documentation/3.2/manual/config/visualisation/maps/links)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        [![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/minus.gif)](javascript: indexmenu_3375628257f69b0b3e631.o(107);)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/folderhopen.gif)

        [3 Screens](https://www.zabbix.com/documentation/3.2/manual/config/visualisation/screens)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/joinbottom.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [1 Screen elements](https://www.zabbix.com/documentation/3.2/manual/config/visualisation/screens/elements)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/joinbottom.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [4 Slide shows](https://www.zabbix.com/documentation/3.2/manual/config/visualisation/slides)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        [![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/minus.gif)](javascript: indexmenu_3375628257f69b0b3e631.o(110);)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/folderhopen.gif)

        [7 Templates](https://www.zabbix.com/documentation/3.2/manual/config/templates)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [1 Configuring a template](https://www.zabbix.com/documentation/3.2/manual/config/templates/template)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/join.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [2 Linking/unlinking](https://www.zabbix.com/documentation/3.2/manual/config/templates/linking)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/line.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/joinbottom.gif)

        ![](https://www.zabbix.com/documentation/3.2/lib/plugins/indexmenu/images/thread/page.gif)

        [3 Nesting](https://www.zabbix.com/documentation/3.2/manual/config/templates/nesting)



