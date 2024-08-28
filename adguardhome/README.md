# AdguardHome

Initally, I wanted to use the AdguardHome docker image which they provide. However after looking into the setup, I decided to use their script to install AdguardHome onto my raspberry pi.

From their [wiki](https://adguard-dns.io/kb/adguard-home/getting-started/) and their [Github](https://github.com/AdguardTeam/AdGuardHome#getting-started) I ran:

```bash
curl -s -S -L https://raw.githubusercontent.com/AdguardTeam/AdGuardHome/master/scripts/install.sh | sh -s -- -v
# Needs to run as root
sudo ./AdGuardHome
```

Doing so this way means I did not have to mess around with any docker networking and any potential conflicts with port 53. And what can be seen as a benefit or a drawback, I can update from the dashboard with just a click instead of pulling a new image and potentially using WatchTower.
