Logins
===========

Geo-location information is probably the single most important enrichment that can be added to audit log events. Microsoft keeps track of the locations where the users are signing in from when these login activities are viewed in the Azure AD/Entra ID portal but these enrichments do not make it to the audit logs retrieved via Search-UnifiedAuditLog cmdlet.

With the unified audit log fetcher, geo-location information is added to every event during the log ingestion. Login activities are tracked per country, ASN, or per IP address for every user or service principal each day. It is quite easy to spot any given day when the user had multiple failed login attempts signifying potential account brute force activities or even one that is successful.

The geo-location enrichment uses a maxmind database freely availble from https://ipinfo.io. At present, only country and ASN information are added which should be enough for most investigations or triaging. The lookups are performed locally so no data is ever sent to any third party.


.. image:: /images/logins.jpg
   :alt: log path
   :scale: 50
