.. _RFC821: https://tools.ietf.org/html/rfc821
.. _RFC2821: https://www.ietf.org/rfc/rfc2821.txt

Special Providers
=================

The :term:`SMTP` protocol is clearly defined in :term:`RFC` standards:

* `RFC821`_
* `RFC2821`_

Most email providers and infrastructure conform to these standards. Unfortunately, however, there are some providers that do not adhere to standards.

Consequences of lack of compliance to standards can result in:

* Deliver-ability issues
* Issues with :term:`SMTP` email verification processes

In this document, we identify known providers that create issues due to lack of compliance to :term:`RFC` standards.


Office 365
----------
**Standards Violations**: 

* `RFC821`_ section 3.1. MAIL *If the recipient is unknown the receiver-SMTP returns a 550 Failure reply.*

Since mid 2016, Email Hippo customers have reported some Office 365 hosted domains as reporting 250 OK during email verification processing. Subsequently, on customers attempting to send emails to these email addresses, Office 365 has responded with hard bounce :term:`NDR`.

For our customers that rely on integrity of our email verification processing to determine deliver-ability quality, receiving hard bounces on mail send is unacceptable.

Email Hippo therefore, in the interests of reporting accurately, has taken the decision to label all Office 365 hosted domains as Unverifiable / UpredictableSystem.


Yahoo!
------
**Standards Violations**: 

* `RFC821`_ section 3.1. MAIL *If the recipient is unknown the receiver-SMTP returns a 550 Failure reply.*

Yahoo mail services attempt to manage incoming spam with a blended approach of:

* Repuation based assesment
* Non-standard imlementations of the :term:`SMTP` protocol
* Velocity and traffic management
* Proprietary white-listing

Sending email to Yahoo! or performing email verification processes can be problematic based on the non-standard Yahoo! implementations of the :term:`SMTP` protocol and ancillary services.

Email Hippo delivery partial coverage of Yahoo! based email addresses. However, due to reasons stated above, we are unable to state or underwrite any specific coverage statistics for this domain.