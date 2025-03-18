# Sen2vm-snap-plugin
Sen2VM SNAP plugin that calls the sen2vm-core standalone jar

### *Prerequisite*

* build sen2vm-core
* create zip archive with the following structure

sen2vm.zip 

  src/main/resources/orekit-data/ 

  sen2vm-snap-plugin/ 

  sen2vm-snap-plugin/sen2vm-core-0.0.1-SNAPSHOT.jar 

  sen2vm-snap-plugin/configuration_example.json 

  sen2vm-snap-plugin/params.json 

### Build from sources

* Build with maven and Java >11 :

  ``mvn clean install``

###  SNAP installation

The bundle installation is not provided for now.
You can distribute the archive with python http.server to serve the zip file on default snap URL

``	python3 -m http.server 8000 ``

Otherwise , you can choose local installation in the SNAP menu bundle installation.



* Install plugin from snap menu: **Tools → Plugins** 

![img](/home/florian/snap_dev/sen2vm-snap-plugin/doc/images/plugin_menu.png) 

 

 

Continue by  **Downloaded → Add Plugins** and search the nbm file in :

sen2vm-snap-plugin/target/sen2vm-snap-plugin-1.0-SNAPSHOT.nbm 

At the end of the plugin installation, choose restart SNAP to taking account the modification.

![img](/home/florian/snap_dev/sen2vm-snap-plugin/doc/images/install_plugin.png) 

At this stage, only the plugin is installed. It have to install the installation bundle -> sen2vm.zip.
At the first execution of plugin, the installation bundle is proposed to the user.
Otherwise, it is possible to install the bundle after the restart in the menu **Tools > Manage Exeternal Tools**

![img](/home/florian/snap_dev/sen2vm-snap-plugin/doc/images/manager_ext_tools_menu.png) 

 

And then, double click on  **sen2vm-snap-plugin**

![image-20250318171215251](/home/florian/snap_dev/sen2vm-snap-plugin/doc/images/manager_ext_tools_view.png)

Continue to  **Bundled Binaries** and proceed to **Download and Install Now** .

![image-20250318171300788](/home/florian/snap_dev/sen2vm-snap-plugin/doc/images/install_bundle_menu.png) 



### Using

The sen2vm-snap-plugin is located in **Optical>Geometric>sen2vm**
