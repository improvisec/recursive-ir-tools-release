Operations and Indicators
=========================

This panel consists of a listing of M365 operations as well as various pre-built indicators that have been enabled in the operations.yml file. Additional operations can be enabled either by modifying the operations.yml file or by searching for it within the application.

Each operation has a checkbox toggle to enable or disable it. When an opereation is enabled, the users on the right panel are filtered and updated to show only those users who performed such opereation. The frequency threshold numeric values on the right of the operations can be modified simply by typing the value and pressing enter. Once set, these frequencies also determine the resulting matching users on the right panel. Explanations about the different indicators and thresholds can be found in the operations.yml file.

When this panel is in focus, a > cursor is visible. A operation search prompt is also displayed in the debug panel so text can be entered at any time.

.. image:: /images/operations_panel.png
   :alt: log path
   :scale: 50


Help menu can be accessed at any time by pressing F1 on the keyboard.

Searching Operations
--------------------

During log ingestion, all operations found in the logs are recorded. They can then be searched for while the operations panel is in focus. Matching operations appear immediately at the bottom of the existing list as soon as you start typing, where the desired additional operation can be enabled. Navigate through the different pages using the left and right arrow keys.

.. image:: /images/search_operation.png
   :alt: log path
   :scale: 50

Searching Indicators
--------------------

During log ingestion, several fields are indexed to enable fast lookups. These fields are mapped to all users having events where the values are found. It's easy for example to identify all users that are associated with say an IP address, or an internet message id. To access the IOC searching feature, hit ctrl+f at any time. The prompt in the debug window will change to [Search IOCs]:. Similar to when searching for operations, the matching users on the right panel are also dynamically updated as soon as you start typing. The debug window will also show what indicators are matching the typed characters.

Pressing enter after typing the filter will cause the application to perform a full database search, meaning it will match all users regardless if they were previously matched by the currently enabled operations.

.. image:: /images/search_ioc.png
   :alt: log path
   :scale: 50


Saving Operations
-----------------

To save the currently toggled operations, hit ctrl+s. This will save the enabled/disabled status back into operations.yml so changes will persist on the next application run. Changing the frequencies/threshold on the other hand automatically persists the changes into the operaitons.yml file.

