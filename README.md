# ipdyn

This simple python script manages IP-tables entries by replacing IP-addresses 
with actual addresses from a DNS lookup. The DNS names are stored in IP-tables comment section.

Example:

iptables -A INPUT -p tcp -s 0.0.0.0 -j ACCEPT -m comment --comment "DYN:myaddress.dyndns.org=0.0.0.0"

The script replaces the "0.0.0.0" with the actual IP-Address.
I suggest running the script within a cronjob.