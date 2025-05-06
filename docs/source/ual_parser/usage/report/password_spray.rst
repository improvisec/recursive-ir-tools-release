AiTM / Session Hijacking
========================

During Adversary in The Middle (AiTM) attacks, attackers would hijack the victim user's session through the stolen session token. Since the attacker would use this token from a different source IP address, it is quite easy to spot a user that has become a victim of such attack. Within a given duration, say 60 minutes, if the user re-uses a token from a different IP address, this user is flagged as a potential victim of session hijacking, possibly through adversary in the middle. Unfortunately in digital forensics, nothing is easy to prove. There will always be false positives, but if you combine this indicator with other indicators seen for this user, your initial assumption might very well be true.


.. image:: /images/hijack.png
   :alt: log path
   :scale: 50
