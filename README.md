nagios-plugins-osrm
===================

Nagios plugins for osrm

Requirements
============

All commands uses the **check_http** standard command, except
**check_osrm_viaroute_result** which uses **check_json** from
https://github.com/c-kr/check_json.


Usage
=====

* check_osrm!PORT

* check_osrm_hello!PORT

* check_osrm_locate!PORT!LOCATION

* check_osrm_nearest!PORT!LOCATION

* check_osrm_viaroute!PORT!LOCATION_1!LOCATION_2

* check_osrm_viaroute_result!PORT!LOCATION_1!LOCATION_2

Sample

    define service {
        host_name                       osrm.quiedeville.org
        service_description             trucks
        check_command                   check_osrm_viaroute_result!5002!50.294,2.782!50.281,2.792
    }

Variables
=========

* **PORT** : the tcp port on which osrm listen

* **LOCATION** : coordinate as lat,lon as OSRM 



