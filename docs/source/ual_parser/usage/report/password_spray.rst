Password Spray Attack
=====================

Users who recorded multiple failed logins from the same Internet Service Provider within the same IP address subnet may indicate a tenant-wide password spraying attack. 

The "potential password sprays" tab provides a list of failed logon events from the user and any other user where the source IP address belongs to the same ISP and part of the same subnet. The assumption is that threat actors often rotate IP infrastructure during password spraying to bypass lockouts and/or detection. 

The duration limit in minutes as well as the minimum number of users within the same group can be configured (e.g., within 120 minutes, if at least 6 other users had failed logins from the same source, then consider this user as being part of a tenant-wide password spray attack.). The good thing about this tool is that you can ingest logs from multiple tenants and cross-correlate events.


.. image:: /images/spray.png
   :alt: log path
   :scale: 50
