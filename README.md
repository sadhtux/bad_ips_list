# Bad IPs feed for BlackList via firewall 

Using the best feeds, I have compiled a final list with over 220 thousand malicious IP addresses to be blocked directly from your firewall solution.

This list is provided as is and you are the only one responsible for the use you may make of it. It is recommended to backup any configuration you are going to modify before applying this list as a blacklist.

greetings 
@sadhtux

# How to implement in most comercial Firewalls:

## FortiGate
- Menu "Security Fabric → External Connectors → Create New → IP Address"
- Take a URL in the "Links" section below
- Then, the lists can be used in "Firewall Policy" as "IP Address Threat Feed" objects.
- Implementation of the full list validated even on the smallest FortiGate 40F appliance
- More information: [Fortinet help page](https://docs.fortinet.com/document/fortigate/6.4.2/administration-guide/891236/external-blocklist-policy)

## Palo Alto
- PA-3200 model and above limited to 150k IP
- lower models limited to 50k IP - More information: [on this page](https://docs.paloaltonetworks.com/pan-os/9-1/pan-os-admin/policy/use-an-external-dynamic-list-in-policy/external-dynamic-list)

## Sophos
- More information: [on this page](https://docs.sophos.com/nsg/sophos-firewall/21.0/Help/en-us/webhelp/onlinehelp/AdministratorHelp/ActiveThreatResponse/ConfigureFeeds/ThirdPartyThreatFeeds/index.html)

## pfSense
- via  [this GitHub repo](https://github.com/jaredhendrickson13/pfsense-api) which allows you to implement an API in pfSense. 
- Be careful, by default the maximum number of objects is 400k. Possibility to increase this value if your pfSense has a lot of RAM. 
- More info [here](https://docs.netgate.com/pfsense/en/latest/firewall/aliases.html#alias-sizing-concerns)

## OPNsense
- via API [Documentation Here](https://docs.opnsense.org/development/api/core/firewall.html) 
- Change the maximum number of entries for an alias: "Firewall -> Settings -> Advanced -> Firewall Maximum Table Entries". 

## IPTables 
- with the "ipset" package installed 
- [tutorial 1](https://www.malekal.com/comment-utiliser-ipset-sur-linux/)   
- [tutorial 2](https://fr-wiki.ikoula.com/fr/Cr%C3%A9er_et_administrer_facilement_une_blacklist_avec_ipset/iptables)   

# To support me
[![A mushroom-head robot drinking bubble tea](https://raw.githubusercontent.com/romainmarcoux/romainmarcoux/main/img/buymeacoffee.png 'Buy me a coffee here')](https://buymeacoffee.com/duarteskorn)

## License
GPL-3.0 license
