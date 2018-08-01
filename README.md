
# OpenVPN config

OpenVPN config is an OpenVPN web interface built on top of Django that makes OpenVPN admins able to:

* Define networks and corresponding OpenVPN conf files
* Add clients to OpenVPN network
    * Get configuration files
    * Create new certificates
    * Revoke certificates
* Register OpenVPN connections: log active and recent OpenVPN connections

Default uses sqlite but you can use PostgreSQL or other if you want.

OpenVPN is released with AGPLv3 License
Author is Luca Ferroni <fero@befair.it>

It includes easy-rsa which is free software made by OpenVPN technologies Inc. <sales@openvpn.net>


Quick start
-----------

1. Add "openvpnmon" to INSTALLED_APPS:
  `INSTALLED_APPS = {
  ...
  'openvpnmon'
  }`

2. Include the myblog URLconf in urls.py:
  `url(r'^openvpnmon/', include('openvpnmon.urls'))`

3. Run `python manage.py migrate` to create myblog's models.

4. Run the development server and access `http://127.0.0.1:8000/openvpnmon/` to
manage openvpnmon.


