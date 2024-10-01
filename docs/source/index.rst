.. recursive-ir-tools documentation master file, created by
   sphinx-quickstart on Mon Sep 30 18:34:01 2024.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. image:: /images/splash.png
   :alt: recursive logo

**Recursive IR Tools** automate various tasks involved in incident response investigations including artefacts collection, log parsing, evidence analysis, timelining, and reporting. 



.. toctree::
   :maxdepth: 2
   :caption: Recursive IR:

   Installation
   Main_Menu

.. toctree::
   :maxdepth: 2
   :caption: UAL Fetcher:

   ual_fetcher/usage/online_mode
   ual_fetcher/usage/offline_mode
   ual_fetcher/usage/resuming_sessions

.. toctree::
   :maxdepth: 2
   :caption: UAL Parser:

   ual_parser/usage/selection
   ual_parser/usage/reporting
   ual_parser/report/tabs/dodgy_days
   ual_parser/report/tabs/logins
   ual_parser/report/tabs/ISP_stats
   ual_parser/tabs/applications
   ual_parser//tabs/inbox_rules
   report/tabs/created_users
   report/tabs/deleted_user
   report/tabs/new_assigned_roles
   report/tabs/new_consented_apps
   report/tabs/new_added_secrets
   reports/tabs/events
