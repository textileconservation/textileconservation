#### fail2ban use

sg textile conservation is a static site of four routes. One of the routes (contact) has a mail form that attracts spam.

Spam detection/banning is accomplished using timing and trap values in the mail form that trigger fail2ban processing.

Banning is logged using the dancer2 'file' logging engine. An additional utility route displays the ban log and enables ban expansion and cancellation.

Ancillary use of fail2ban simplifies the management of ban durations. Durations are configured using separate fail2ban jails for ips and /24 subnets.

#### jail.local
```
.
.
.
#
# HTTP servers
#

[texcon]
enabled  = true
port     = http,https
bantime  = 172800
#2 days

[texcon-subnet]
enabled  = true
port     = http,https
bantime  = 864000
#10 days
.
.
.

```
