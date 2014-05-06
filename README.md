nagios-plugins-osrm
===================

Nagios plugins for osrm

Requirements
============

We use check_json from https://github.com/c-kr/check_json you must
install it to use these plugins

Usage
=====

Use check_http to check all functions in osrm api

* check_osrm

Usage : check_osrm!PORT

* check_osrm_hello

Usage : check_osrm_hello!PORT

* check_osrm_locate

Usage : check_osrm_locate!PORT!LOCATION

* check_osrm_nearest

Usage : check_osrm_nearest!PORT!LOCATION

* check_osrm_viaroute

Usage : check_osrm_viaroute!PORT!LOCATION_1!LOCATION_2

* check_osrm_viaroute_result

Usage : check_osrm_viaroute_result!PORT!LOCATION_1!LOCATION_2

Sample

    define service {
        host_name                       osrm.quiedeville.org
        service_description             trucks
        check_command                   check_osrm_viaroute_result!5002!50.294713,2.782288!50.284294,2.797050
    }




