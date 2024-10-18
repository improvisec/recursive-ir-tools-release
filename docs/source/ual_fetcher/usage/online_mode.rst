Online Ingestion
================

The Unified Audit Log fetcher uses *Search-UnifiedAuditLog* PowerShell commandlet to retrieve audit logs from an M365 tenant. These steps are really straight forward.

1. When prompted, enter the path or folder where the log files will be stored into. This folder will also contain the database that will store the events for processing.


.. image:: /images/logpath1.jpg
   :alt: log path1
   :scale: 60

2. You will be prompted to adjust the database size if there's not enough space left on the device. Enter the desired percentage of the free space remaining. 
   
   Some tenants store more than several gigabytes of M365 audit logs in a day, others within just a few hours. Ideally, you'll be running this tool on a forensics machine with an ample storage space.

.. image:: /images/logpath.jpg
   :alt: log path
   :scale: 60

3. Next, enter the duration in days for your audit log search. The default is provided within square brackets so just hit enter to accept it. Otherwise, specify a starting date using the given format and add "+ n" days to specify how many days starting from the date specified to search for. 


.. image:: /images/duration.jpg
   :alt: duration
   :scale: 60

4. Enter the M365 credentials that will be used for searching. This will be cached locally (encrypted of course) so it can be re-used when using other commandlets. MFA prompt will appear if it is enabled on the tenant.

.. image:: /images/login.jpg
   :alt: login
   :scale: 60

5. From here on, log searching is performed. Search intervals are automatically adjusted to account for limits imposed by Microsoft (e.g., maximum 5000 events per page, or 50,000 events per search).

.. image:: /images/logsearch.jpg
   :alt: login
   :scale: 50

