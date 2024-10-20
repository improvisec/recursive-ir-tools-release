Offline Ingestion
=================

UAL fetcher can ingest unified audit log files in json format. It is possible to process say, one year or more worth of audit logs to identify suspicious activities which happened in a given tenant further back in time. 
This is essential for large scale investigations where determining the extent of the compromise and the real exposure window is critical specially for breaches involving advanced persistent threat actors.

The tool processes input data in chunks and distributes them to a pool of workers utilizing multiple cpu cores (if available) to speed up the log ingestion.

.. image:: /images/parallel.jpg
   :alt: log path
   :scale: 50





