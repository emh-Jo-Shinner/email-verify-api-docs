.. _Email Hippo: http://www.emailhippo.com
.. _mongoDB: https://www.mongodb.com

Features
========

Confidence In Data Security
---------------------------
With ISO27001:2013 certification, robust technology and clearly defined policies and procedures, you can trust `Email Hippo`_ with your data.

See :doc:`data-privacy` for more information.

> 99.9% Service Availability
----------------------------

Fully load balanced and automatic fail-over systems dispersed across 
multiple data centers in multiple regions deliver enterprise grade resilience.

See :doc:`reliability` for more information on availability and :term:`SLA`.

Multiple Response Formats
-------------------------
Since Version 3 of our services, we set the bar higher for email address verification integration. Whilst most of our competitors 
only offer :term:`JSON`, `Email Hippo`_ goes further with giving our customers more protocol options:

 * :term:`JSON` (industry standard modern text based interchange.)
 * :term:`XML` (industry standard legacy text based interchange. Great for interop with older systems.)
 * :term:`BSON` (industry standard binary based interchange. Ideal for direct sorage in `mongoDB`_.)
 * :term:`protobuf` (Google standard for binary based interchange. Ideal for applications requiring low bandwidth and high performance.)

Easy Integration
----------------
See :doc:`client-libraries` to see how quick and easy it is to integrate with our services from over 19 different technologies and platforms.
 
Fanatical Service Quality Management (SQM)
------------------------------------------
`Email Hippo`_ operational staff obsessively monitor services to 
ensure the best possible uptime and coverage.

Uptime and functional correctness is actively monitored on a minute by 
minute basis from multiple data centers dispersed across North America, Europe and Asia.

Fast, Transparent Response Times
--------------------------------
Every query response includes stopwatch data that shows the time taken to execute the request.

Proprietary Scoring and Risk Assessment
---------------------------------------
 * Send risk assessment scoring based on `Email Hippo`_ proprietary scoring heuristics :sup:`(new)`
 * Spam assessment and block-list risk scoring based on `Email Hippo`_ rules and 3rd party data sources including SpamHaus :sup:`(new)`
 * Overall risk scoring based on Email Hippo assessment of Send Risk combined with spam assessment :sup:`(new)`

Multi Factor Verification and Data Enrichment
---------------------------------------------
Progressive verification using multiple verification processes including:

 * Syntax checking
 * DNS checking
 * Block-list checking (e.g. spamhaus)
 * Web infrastructure checking
 * Mailbox checking
 * Proprietary risk scoring including assessment of risks for receiving email from (spam), sending email to (send score) and overall risk assesment.
 
Unrivalled Coverage
-------------------
With more than 5 years experience and the benefit of owning our own 
software stack, `Email Hippo`_ has evolved its services to provide good coverage not only of the easier :term:`B2B` 
domains but also the more technically challenging :term:`B2C` domains including:

 * Hotmail
 * AOL
 * Yandex

Spam Trap Detection
-------------------
After many years R&D, `Email Hippo`_ has developed technology  
that can effectively identify any probable :term:`Spam Trap`.

Disposable Email Address Detection
----------------------------------
**Advanced Disposable Email Address Detection detection based on Email Hippo multi-vector real-time analysis.**

Features include:

 * Checking against static lists
 * Real-time detection of common :term:`DEA` providers obfuscation techniques (e.g. rotating domains, IP addresses and MX servers)

Gibberish Detection
-------------------
A common vector for persons wishing to remain anonymous is to register or use a pre-existing domain. Finding an available domain is not easy and as such, many 
(unwilling to put the effort in to finding a decent domain) instead opt for a \'Gibberish\' domain such as \`sdfre45321qaxc.com\`.

`Email Hippo`_ detects gibberish in both the user and domain elements of an email address.

Unrivalled Performance
----------------------
Strategic data centers in Europe, aggressive 
caching, global network delivery optimization and cloud based auto-scaling deliver outstanding performance. 
Typical queries are answered between 0.2 to 1.5 seconds.

.. note:: See :doc:`technical-spec`

On Screen Reporting
-------------------
Every account comes with a secure on-line portal for customers to 
view their current and historic usage via simple but powerful, user friendly charts and reports.

Thoughtful Versioning
---------------------
Endpoints are \"versioned\". This means that `Email Hippo`_ 
can continue to release new functionality without \"breaking\" 
existing clients committed to integrating with our systems on legacy endpoints.

What it does
------------
`Email Hippo`_ is used to check email addresses in real-time. 
Not only are syntax and domain checked, but that the user mailbox 
is available too. This is the only way to know for sure if an email address is valid.

Additionally identified as part of the email verification process 
is extra information including:

* :term:`DEA`.
* :term:`Spam Trap`.

How it works
------------
Email addresses are verified using various filters and processes. 
As a high level overview, an email address submitted for verification 
goes thorough the following filters:

Syntax
	A basic inspection of the syntax of the email address to see 
	if it looks valid. Work is done only using server :abbr:`CPU(Central Processing Unit)` 
	based on simple pattern matching algorithms.
	
DNS A
	Verifies a domain exists in :term:`DNS`. Domains that do not 
	exist in :term:`DNS` cannot have mail servers or email boxes.
	
	:term:`DNS` checks are performed over the network.
	
DNS MX
	Verify :term:`MX` records using :term:`DNS`. Domains that do not have 
	:term:`MX` records, have no mail servers and therefore no valid email boxes.
	
	:term:`MX` checks are performed over the network.

MailBox
	Verify email boxes with :term:`SMTP` checks.
	
	Connect to mail server and perform :term:`SMTP` 
	protocol to verify if mailbox exists.
	
	This is the deepest level of verification. It is 
	performed over the network.
