<h3>Services</h3>

<h5>DNS</h5>

<p>
  I have 2 DNS server set up, one on each hypervisor, the software of choise is dnsmasq, so it reads all it entries for
  the hosts file. I dont have a need for something more powerfull like Bind9 or PowerDNS, since all I need is a couple
  of A records I feel perfectly fine running something simple like dnsmasq. Everyone else is using something like pihole
  anyways which is just a fancy interface for dnsmasq. I also felt the need to have one IP for DNS so I am using
  vrrp with keepalived to make my DNS higly available with one IP address. To sync the hosts file between the I just 
  created a simple script that runs on the secondary DNS and checks to see if there been any change on the primary, 
  if there have been a change it will copy the hosts from from the primary server to itself.
</p>

<h5>NTP</h5>

<p>
  I have 2 NTP server, one on each hypervisore, I set up ntpd to serve ntp to all my clients and use systemd-timesyncd
  on all my clients to connect to my ntp servers. The ntp pool the servers are connected to are the se debian pool.
</p>

<h5>ACME</h5>

<p>
  I have set up STEP to act like a acme server, and to serve my web servers with ssl certificates. I use lego-acme as 
  a client on my servers to requests certificates from my acme server, and I have created a script that I use that you 
  can find <a href="https://github.com/techolsy/lego-wrapper" target="_blank">here</a>
</p>

<h5>ZABBIX</h5>

<p>
  I user Zabbix for monitoring, it sends me emails when something on a server is wrong and a notification to my phone
  through gotify.
</p>

<h5>Gotify</h5>

<p>
  Gotify is a push notification service is use to send notification to my phone, mostly only use it with Zabbix
  to send notificaions when something is wrong on a server
</p>

<h5>Vaultwarden</h5>

<p>
  I use vaultwarden as a password manager, I can use the bitwarden browser extension to connect to vaultwarden
  and have easy access to my password.
</p>

<h5>Homeassistant</h5>

<p>
  I use homeassistand for some simple automation stuff, not much just a couple for temp sensord and outlets to control
  some lights and humidifers, so I can stay a bit lazy turn off my light without having to get up.
</p>

<h5>Fileserver</h5>

<p>
  It is what it sounds like, just my fileserver that I use for storage, here I save all my media and pictures.
  I set up samba on it to be able to serve files to most clients (Win/Mac/Linux).
</p>

<h5>Emby</h5>

<p>
  Emby is my media server, I use it to watch my media, and because it keeps track on what episode I am on.
  It has a cifs mount to my fileserver to get access to all media.
</p>

<h5>immich</h5>

<p>
  I use immich to sync all photos from my phone to my server, it actually has a really nice interface and
  AI features for those that like that.
</p>

<h5>Pterodactyl</h5>

<p>
  I use pterodactyl to manage my game servers, right now I only host a minecraft server, and pterodactyl
  makes it so much eacher to manage.
</p>

<h5>Miniflux</h5>

<p>
  Miniflux is a web based RSS reader, I use to track RSS feeds on github release pages to see when software I
  host gets updates.
</p>

<h5>Homepage</h5>

<p>
  Homepage is just a fancy dashboard I use instead of just bookmarking websites like other normal people.
</p>

<h5>Navidrome</h5>

<p>
  Navidrome is a music streaming service, I use it to listen to all my music that I keep stored on my fileserver.
</p>

<h5>Beszel</h5>

<p>
  Beszel is like a super simple graph server to keep simple server graphs like CPU MEM and others. It is not super 
  featureful or customizable like grafana, but it shows enough for a simple homelab.
</p>

<h5>Gitlab</h5>

<p>
  You probably already know what Gitlab is, I use host my own gitlab so I can store my private project on my own
  server.
</p>

<h5>Pritunl</h5>

<p>
  Pritunl is a VPN solution, I use it to be able to connect to my homelab when I am out and about and touching grass.
</p>

<h5>UniFi</h5>

<p>
  I have unifi server that I use to manage my singular access point. 
</p>
