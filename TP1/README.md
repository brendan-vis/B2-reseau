### I. Basics

☀️ Carte réseau WiFi
```
commande : ipconfig /all

MAC : 38-7A-0E-C6-72-0D
IP : 10.33.73.98
Sous reseau : 255.255.240.0/20
```

☀️ Déso pas déso
```
adresse de réseau : 10.33.64.0
adresse de diffusion : 10.33.79.255
nombre d'adresse IP dispo : 4094
```

☀️ Hostname
```
commande : hostname

HP-Brendan
```

☀️ Passerelle du réseau
```
commande : arp -a

adresse IP passerelle du reseau : 10.33.79.254
adresse MAC de la passerelle du reseau : 7c-5a-1c-d3-d8-76
```

☀️ Serveur DHCP et DNS
```
commande : ipconfig /all

adresse IP du serveur DHCP : 10.33.79.254
adresse IP du DNS : 1.1.1.1
```

☀️ Table de routage
```
commande :
netstat -r ou route print -4

route par défaut : 10.33.79.254
```

### II. Go further
☀️ Hosts ?
```
1.1.1.1         b2.hello.brendan

PS C:\Windows\System32\drivers\etc> ping b2.hello.brendan

Envoi d’une requête 'ping' sur b2.hello.brendan [1.1.1.1] avec 32 octets de données :
Réponse de 1.1.1.1 : octets=32 temps=15 ms TTL=55
Réponse de 1.1.1.1 : octets=32 temps=14 ms TTL=55
```

☀️ Go mater une vidéo youtube et déterminer, pendant qu'elle tourne...
```
IP : 91.68.245.81
port : 443
mon port : 50719   ( netstat -a -n -b | Select-String 91.68.245.81: -Context 1,0)
```

☀️ Requêtes DNS
```
commande : nslookup www.thinkerview.com
           nslookup 143.90.88.12

IP : 188.114.96.6
nom de domaine : EAOcf-140p12.ppp15.odn.ne.jp
```

☀️ Hop hop hop
```
PS C:\Users\brend> tracert -d www.ynov.com

Détermination de l’itinéraire vers www.ynov.com [172.67.74.226]
avec un maximum de 30 sauts :

  1     3 ms     1 ms     1 ms  10.33.79.254
  2     3 ms     1 ms     1 ms  195.7.117.145
  3     2 ms     2 ms     1 ms  86.79.195.237
  4     3 ms     2 ms     2 ms  86.65.224.196
  5    11 ms    11 ms    10 ms  194.6.147.164
  6     *        *        *     Délai d’attente de la demande dépassé.
  7    14 ms    14 ms    14 ms  162.158.20.240
  8    14 ms    14 ms    14 ms  172.67.74.226
```

☀️ IP publique
```
ip publique de la passerelle : 195.7.117.146
```

### III. Le requin

☀️ Capture ARP
```
commande : arp -d
[lien wireshark](./captures/arp.pcap)
```

☀️ Capture DNS
```
commande : nslookup google.com

[lien wireshark](./captures/dns.pcap)
```

☀️ Capture TCP
```
commande : curl google.com

[lien wireshark](./captures/tcp.pcap)
```