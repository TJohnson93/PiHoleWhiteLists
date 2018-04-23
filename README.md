# Pi-hole White Lists
This contains my custom whitelists for Pi-hole.

*I borrowed some whitelists from https://discourse.pi-hole.net/t/commonly-whitelisted-domains/212 and https://wally3k.github.io/*

## TODO:
Note to myself to add whitelists from the following sites...
* https://discourse.pi-hole.net/t/commonly-whitelisted-domains/212
* https://wally3k.github.io/

## Google Services

### Google Maps

```
pihole -w clients4.google.com
pihole -w clients2.google.com
```

### YouTube History

```
pihole -w s.youtube.com
pihole -w video-stats.l.google.com
```

### Google Play

```
pihole -w android.clients.google.com
```


## Microsoft

### Windows (Verifies Internet Connectivity)

```
pihole -w www.msftncsi.com
```

### Microsoft Web Pages (Outlook, Office 365, Live, Mic)

```
pihole -w outlook.office365.com
pihole -w products.office.com
pihole -w c.s-microsoft.com
pihole -w i.s-microsoft.com
pihole -w login.live.com
```

### Backup Bitlocker Recovery Key to Microsoft Account
```
pihole -w g.live.com
```

### Windows Store
```
pihole -w dl.delivery.mp.microsoft.com
pihole -w geo-prod.do.dsp.mp.microsoft.com
pihole -w displaycatalog.mp.microsoft.com
```

### XBox Live

This domain is used for sign-ins, creating new accounts and recovering existing Microsoft Accounts *(Confirmed by Microsoft)*.
```
pihole -w clientconfig.passport.net
```

This domain is used for Xbox Live Achievements (confirmed by Microsoft)

```
pihole -w v10.events.data.microsoft.com
```

There are several domains discovered initially on [Reddit](https://discourse.pi-hole.net/clicks/track?url=https%3A%2F%2Fwww.reddit.com%2Fr%2Fxboxone%2Fcomments%2F5khrrl%2Fachievements_not_unlocking%2F&post_id=628&topic_id=212) and [/r/xboxone](https://discourse.pi-hole.net/clicks/track?url=https%3A%2F%2Fwww.reddit.com%2Fr%2Fxboxone%2Fcomments%2F5l7bm1%2Ftech_piholeother_dns_users_additional_whitelist%2F&post_id=628&topic_id=212), which were also confirmed by Microsoft as being required by Xbox Live for full functionality.

```
pihole -w xbox.ipv6.microsoft.com
pihole -w device.auth.xboxlive.com
pihole -w www.msftncsi.com
pihole -w title.mgt.xboxlive.com
pihole -w xsts.auth.xboxlive.com
pihole -w title.auth.xboxlive.com
pihole -w ctldl.windowsupdate.com
pihole -w attestation.xboxlive.com
pihole -w xboxexperiencesprod.experimentation.xboxlive.com
pihole -w xflight.xboxlive.com
pihole -w cert.mgt.xboxlive.com
pihole -w xkms.xbolive.com
pihole -w def-vef.xboxlive.com
pihole -w notify.xboxlive.com
pihole -w help.ui.xboxlive.com
pihole -w licensing.xboxlive.com
pihole -w eds.xboxlive.com
pihole -w www.xboxlive.com
pihole -w v10.vortex-win.data.microsoft.com
pihole -w settings-win.data.microsoft.com
```

### Skype

```
pihole -w s.gateway.messenger.live.com
pihole -w ui.skype.com
pihole -w pricelist.skype.com
pihole -w apps.skype.com
pihole -w m.hotmail.com
pihole -w s.gateway.messenger.live.com
pihole -w sa.symcb.com s{1..5}.symcb.com
```
