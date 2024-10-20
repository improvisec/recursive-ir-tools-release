Reporting
=========

The Unified Audit Log parser produces .xlsx spreadsheets to break down and group related events together for every user or aplication. Without breaking these events into per individual users, the resulting document would be too large for Microsoft Excel to even open. 

Excel spreadsheet format was particularly chosen to take advantage of native tools available so the user doesn't have to set up more complex workflows but still have the ability to slice and disect the data any way preferred e.g., creating pivot tables, complex graphs, charts, vlookups, nicely formatted tables, or even just the basic highlighting or colorizing of rows. All these will be handy when it's time to write your investigation report - imagine doing all these in a SIEM. 

The spreadsheet contains several tabs including the last one (events) which contains all events associated with the user or service principal. 

This section covers different reports.

.. toctree::
   :maxdepth: 2

   report/dodgy_days
   report/logins
   report/ISP_stats
   report/applications
   report/new_mfa_devices
   report/inbox_rules
   report/created_users
   report/deleted_users
   report/new_app_owners
   report/new_assigned_roles
   report/new_consented_apps
   report/new_added_secrets
   report/events


