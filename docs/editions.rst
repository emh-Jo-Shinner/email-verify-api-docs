.. _Endpoint Details: https://api.hippoapi.com/swagger

About Editions
==============
There are three editions of endpoints.

* Basic
* Block Lists
* More

Each varies in functionality and performance.

The schema across all editions remains consistent which delivers the following benefits:

* Consistent integration with a consistent entity model
* Easily change between editions based on data depth versus performance requirements.


Basic
-----
Basic level performs simple, compute only email address syntax checks.

This is the fastest performing end point.

**Performance:** Fastest

Block Lists
-----------
Performs Basic level checks plus:

* DNS Lookups
* Checking of email infrastructure against Email Hippo and third party lists for :term:`DEA` and spam or other anti-social behavior.

**Performance:** Medium

More
----
The most thorough analysis and data enrichment.

Performs Basic and Block Lists levels plus:

* Deep mail box verification
* Web site PING
* Social enrichment
* Spam scoring
* :term:`Spam Trap` analysis
* Send Scoring
* Hippo Trust Scoring


**Performance:** Least Fast


For more information on performance and features see `Endpoint Details`_.