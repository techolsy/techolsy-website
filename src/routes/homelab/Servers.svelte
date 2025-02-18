<h3>Servers</h3>

<p>
  My servers is just 3 pc's acting as "servers". There is one mini pc with an older i5 and 16 gigs of ram(PVE01),
  Then there is a larger server with a newer i3 and 128 gigs of ram(PVE02),
  and the last one runs on a old pentium and 4 gigs of ram(PBS).
</p>

<h5>PVE01</h5>

<p>
  <i>PVE01</i> is an old HP EliteDesk with an i5 6500T CPU and 16 GB of memory, it runs proxmox as an hypervisor.
  It has a 500 GB SSD dish used both as boot drive and vm storage, since it is a weaker system it does not run
  that many virtual machines.
</p>

<h5>PVE02</h5>

<p>
  <i>PVE02</i> is a custom built pc with an i312100 CPU and have 128 GB of memory, it also runs proxmox as an hypervisor.
  For storage it has a 500 GB SSD as a boot drive and a 2 TB nvme for vm storage, it also have additional 4x4 TB HDD 
  configured in a raid5 mdraid. this server all the main services I mostly use on a day to day basis.
</p>

<h5>PBS</h5>

<p>
  <i>PBS</i> is my backup server, it is also a custom built but with scrap parts I could find, so it has an pentium
  and 4 GB of memory, it runs proxmox backup server. it has a 128 GB SSD as a boot drive and one 1 TB for vm backup
  and a 12 TB HDD for file backup.
</p>
