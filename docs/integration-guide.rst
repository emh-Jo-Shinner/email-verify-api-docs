.. _swagger.io: https://swagger.io
.. _Endpoint Definitions: https://api.hippoapi.com/swagger/
.. _WADL : https://api.hippoapi.com/swagger/v3/swagger.json
.. _IP Ranges : https://www.cloudflare.com/ips/
.. _Cloudflare : https://www.cloudflare.com

.. _Integration Guide:

Schema
======

* `Endpoint Definitions`_
* `WADL`_ (swagger.io)

Return Protocols
================
Email Hippo :term:`API` services can return data in several formats:

* :term:`JSON`
* :term:`XML`
* :term:`BSON`
* :term:`protobuf`

Firewall Rules
==============
If your organization implements internal firewall rule policies, you may need to ask your IT staff to allow access to our API endpoints.

Our :term:`API` services are delivered via `Cloudflare`_. Please see the Cloudflare page "`IP Ranges`_" for a definition of the IP endpoints that are possible when accessing our :term:`API`.