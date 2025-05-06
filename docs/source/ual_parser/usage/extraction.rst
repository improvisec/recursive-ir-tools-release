Extraction
==========


Stored audit logs can be extracted from the databse using the UAL Investigator. All data are de-duplicated already, and with added geo-location information.

The following screenshot shows logs being extracted from one of the databases present. The extraction process is lightning-quick as database entries are memory mapped in the LMDB database.



.. image:: /images/extracting.jpg
   :alt: log path
   :scale: 40

Events relevant to specific users or applications/service principals can also be exported to json from within the UAL Investigator UI.


.. image:: /images/export.jpg
   :alt: export to json
   :scale: 40