UAL Parser
===========


The unified audit log parser reads the events ingested by ual_fetcher and generates a spreadsheet report for one or more (or all) users or applications. This process is extremely fast as most of the heavy-lifting was already done by ual_fetcher during the log ingestion. Statistics are collected by the ual_fetcher such as how many successful and failed logins each day from each location occurs, or the list of applications registered, inbox rules added, or even MFA devices registered, all broken down for every user or service principal in the tenant. 

The tool would then flag each day having met a certain criteria as "dodgy" and hence flag that user or service pricipal as dodgy. For example, if there is at least one day when the user logged in successfully from at least 4 different countries, that could be considered as dodgy. Likewise, having logged in from more than three Internet Service Providers or ASN at any given day looks dodgy. Similarly, registering a new MFA device would be considered as dodgy too if it happens quite recently.

During client incident response engagements, this will be handy to quickly triage the whole tenant not only to idenify potentially compromised accounts, but also to pinpoint when the compromise may have started.



.. toctree::
   :maxdepth: 2
   :hidden:

   ual_parser/usage


