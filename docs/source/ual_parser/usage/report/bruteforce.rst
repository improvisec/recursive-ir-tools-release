Password-guessing / Bruteforce
==============================

This is a classic attack scenario. For a user to be flagged, multiple failed login attempts within a given period (say 2 hours) has to be recorded followed by a successful login from the same IP. This user has recorded 36 failed login attempts within an hour followed by a successful login. Whether or not that will prove a successful password guessing is something that needs to be correlated with other indicators. An experienced investigator will surely flag this one as such.


.. image:: /images/bruteforce.png
   :alt: bruteforce report
   :scale: 50


The login activities for this user were quite dodgy. There were days when this user would register several hundreds of failed logins in a single day.

.. image:: /images/bruteforce3.png
   :alt: sample bruteforce 1
   :scale: 50


The day before the potentially successful bruteforce attack was flagged, this user recorded 925 failed login attempts. If that isn't a sign of a bruteforce attack, I don't know what is.

.. image:: /images/bruteforce2.png
   :alt: sample bruteforce 2
   :scale: 50