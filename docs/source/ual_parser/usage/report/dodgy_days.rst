Dodgy Days
==========

The first tab called "dodgy_days" breaks down events occuring each day and identifies days where suspicious activities are recorded for a user or service principal. This is quite handy specially during incident response investigations where it is critical to identify the compromised accounts or backdoor applications or service principals as soon as possible to perform immediate containment. 

Any particular day that meets the criteria for being "dodgy" is flagged along with highlighting these criteria as seen from this example:

.. image:: /images/dodgy_days.jpg
   :alt: log path
   :scale: 30


These are currently what consist of the dodgy criteria. These are hard-coded at the moment but will be made configurable in future releases:


In any given day, if there is at least any of the following, then that day is considered dodgy, and so is the user or service principal:

* 4 MFA login failures (i.e., user failing the MFA challenge)
* 1 MFA device registered
* 1 new internal app registered
* 1 new external app registered
* 1 new inbox rule created
* 1 new user created
* 1 new user deleted
* 1 new app owner assigned
* 1 new role assigned
* 1 new consented application 
* 1 new application secret added
* 1 successful login from at least two countries
* 1 successful login from at least three ISPs
* 1 successful login from one country but at least 3 ISPs
        


