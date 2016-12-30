## KSP DMP Server (https://d-mp.org/)

#### TL;DR
```bash
docker run -d -p 6702:6702 \
    -v <data>/Config:/DMPServer/Config \
    -v <data>/Plugins:/DMPServer/Plugins \
    -v <data>/Universe:/DMPServer/Universe \
    -v <data>/logs:/DMPServer/logs \
    hugome/docker-dmp-ksp
```
##### Volumes

- /DMPServer/Config (Config)
- /DMPServer/Plugins (Plugins)
- /DMPServer/Universe (World save)
- /DMPServer/logs (Server logs)

##### Other volumes

- /DMPServer/DMPIPBans.txt (Banned IPS)
- /DMPServer/DMPKeyBans.txt (Banned RSA)
- /DMPServer/DMPModControl.txt (Mods)
- /DMPServer/DMPPlayerBans.txt (Banned pseudos)
