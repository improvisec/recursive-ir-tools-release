UAL Fetcher 
===========

Unified Audit Log Fetcher (ual_fetcher) is a handy tool that allows retrieval of audit logs from a Microsoft 365 tenant. If you're working in DFIR space, one of the most common investigations you've likely done before is business email compromise incident in Azure/Microsoft 365. 

The most common collection method is using a PowerShell cmdlet called "Search-UnifiedAuditLog". This presents a number of challenges namely:

1. Microsoft controls server-side resources quite strictly. If you've been doing this for a while now, you're probably aware that:

   * the search-unifiedauditlog cmdlet returns a maximum of 50,000 events per query and using pagination, each page returns a maximum of 5,000 entries
   * although 3 simultaneous PowerShell sessions are allowed, the server implements strict rate limiting and you probably won't benefit from parallel or asynchronous searches (if you can pull it off).

2. The sheer volume of events generated on each tenant specially with big organizations (some tenants generate gigabytes of audit logs in a day), makes log retrieval quite challenging specially if you are aiming for a "forensically sound" acquisition.
3. Microsoft doesn't sort events by default but an experimental support for sorted, larger, result set retrieval is in the works. For now, you have to work with what's available.
4. During searches using the cmdlet, the server may return duplicate entries, the only way to deal with this (if using Excel's de-duplicate function isn't feasible due to high volume of data collected), is to ingest the log data into a database or run it through a script. 
5. When doing an investigation, it is important to be as detailed as possible about all activities related to the incident. All events performed by, or on behalf of the potentially compromised account must be accounted for to have a complete trail of events. 

UAL Fetcher ingests audit logs into a memory-mapped embedded database (LMDB) which uses B-tree algorithm so entries are naturally sorted and de-duplicated upon ingestion. An index is created which links all relevant events performed by, on, or on-behalf-of the principal making event tracking more accurate.

A list of current features supported are listed below:

    * retrieval of audit logs with auto back-offs and retries to deal with server-side rate limiting
    * auto-adjusting search interval to overcome the 50,000/5,000 search result limit
    * resuming of interrupted online log retrieval
    * event sorting and de-duplication
    * event indexing for faster extraction and processing
    * data compression
    * credential caching and log retrieval session management
    * onlined mode supports automatic mapping of GUIDs to user email addresses or service principal display names.
    * offline geo-location enrichment c/o the awesome https://ipinfo.io
    * support parallel processing of data to speed up offline ingestion. No issues ingesting 256GB worth of logs. 




.. toctree::
   :maxdepth: 2
   :hidden:

   ual_fetcher/usage/online_mode
   ual_fetcher/usage/offline_mode
   ual_fetcher/usage/resuming_sessions


