Suspicious Query / Downloaded Files
===================================

This indicator triggers when a user performs Sharepoint lookups using search query strings found within a list of keywords. The list of keywords and the minimum number of queries made within a day is configurable. In this screenshot below, the threat actor is obviously looking for anything that has "password" in it, as well as "sms".


.. image:: /images/query.png
   :alt: bruteforce report
   :scale: 50


A similar worksheet is also created for file downloads performed by a user where the filename contains keywords found in the pre-defined list. 