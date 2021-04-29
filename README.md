# LR-Tanium-MPE
LogRhythm MPE Rules for Tanium
  
This repository consists of MPE rules in the LogRhythm native XML format, for use with parsing Tanium logs sent via Syslog (sent to LogRhythm via 'Socket', as it is seen in the Tanium Connect UI).
  
The expected log format is LEEF (v1 or v2 should work, but the rules have been tested with v2 only)
Date formats, where customisable, have been set to RFC 3339 format. If you set this to MM/DD/YYYY, it won't affect the time parsing of the logs, but it may cause the entire log not to match the rule.  
  
The following rules are present:

1.. Tanium Discover LEEF: Messages from Tanium Discover. These can be quite a lot, as it will report the details of every interface (ie every IP/host) found on the network on a periodic Discover scan.  
  
3.. Tanium Question History: Logs indicating who has been asking which questions as part of the Interact module (also shows when internal Tanium components have been asking questions, perhaps as a scheduled scan). 
   
5.. Tanium AuditSourceLogs LEEF2: Logs showing logins and login attempts, as well as some user modification activity (eg users synchronised in an LDAP scan).  
  
6.. Tanium Action History: Logs showing where an 'action' has been performed on a set of devices.  
  
7.. Tanium Discover Nfns: Notifications from Tanium Discover - usually when a new device ("interface") has been detected on the network during a Discover scan.  
