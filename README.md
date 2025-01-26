# bad_ips_list
### Bad IP List - For block using any firewall via group many feeds

#english 

Using the best feeds, I have compiled a final list
with over 220 thousand malicious IP addresses to be blocked
directly from your firewall solution.

This list is provided as is and you
are the only one responsible for the use you may make of it.
It is recommended to backup any configuration you
are going to modify before applying this list as a
blacklist.

greetings
@sadhtux

#spanish

Usando los mejores feeds, he compilado un listado final
con mas de 220 mil direcciones ip maliciosas para ser
bloqueadas directamente desde su solucion de firewall.

Este listado se provee asi tal cual como esta y usted 
es el unico responsable del uso que pueda darle.
Se recomienda respaldar cualquier configuracion que
vaya a modificar antes de aplicar dicho listado como
blacklist.

saludos
@sadhtux


How to integrate these lists into a firewall?

    FortiGate
        Menu "Security Fabric → External Connectors → Create New → IP Address"
        Take a URL in the "Links" section below
        Then, the lists can be used in "Firewall Policy" as "IP Address Threat Feed" objects.
        Implementation of the full list validated even on the smallest FortiGate 40F appliance
        More information: on this page Fortinet help page
    Palo Alto: here. PA-3200 model and above limited to 150k IP (use full-aa.txt only), lower models limited to 50k IP (use full-40k.txt file)
    Sophos : lien.
    pfSense: via this GitHub repo which allows you to implement an API in pfSense. Be careful, by default the maximum number of objects is 400k. Possibility to increase this value if your pfSense has a lot of RAM. More info here here.
    OPNsense : via API (doc. Change the maximum number of entries for an alias: "Firewall -> Settings -> Advanced -> Firewall Maximum Table Entries".
    IPTables with the "ipset" package: tutorial 1 tutorial 2
