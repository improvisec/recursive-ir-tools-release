Installation Guide
==================



**Unified Audit Log Fetcher and Parser**


To use ual_fetcher and ual_parser, the following must be performed. On a Windows 10 (or newer) machine:

1. Download and extract the `latest <https://updates.recursive.improvisec.com/latest>`_ package from https://updates.recursive.improvisec.com/downloads.

2. Download and install Python 3.12.7 from https://www.python.org/downloads/windows/.

3. Install the required python modules found in requirements.txt by running the following command below in the command prompt (from within the extracted package folder).

::

   pip install -r requirements.txt

4. Install the required PowerShell 5.x modules. When running ual_fetcher, you will be prompted to install the required powershell modules if they aren't already installed. 

.. image:: /images/missing_modules1.jpg
   :alt: missing modules
   :align: center
   :scale: 50

.. image:: /images/missing_modules.jpg
   :alt: missing modules
   :align: center
   :scale: 50




*Additional Requirements:*

* Storage - On Windows platform, the OS pre-allocates disk space to be used by an LMDB database. This is currently set at 10GB which is more than enough to store unified audit logs in most investigations.
* Microsoft Office Excel (or anyting that can open an xlsx file) - The program generates .xlsx spreadsheets for individual users or applications. 
* An M365 account with proper permission to perform unified audit log retrieval via Search-UnifiedAuditLog powershell commandlet. Consult Microsoft's `documentation <https://learn.microsoft.com/en-us/powershell/module/exchange/search-unifiedauditlog?view=exchange-ps>`_ for more information.

