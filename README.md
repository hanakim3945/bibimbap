# bibimbap

GestaltHax on T8012 Mac

### Background

Based on my experience, T2 macs cannot generate the Gestalt Cache themself.
It can only validates an existing cache and if it's recognized as valid, it reads the configuration from it (also the faked chip fusion state and demotion).

### Howto

1. Create the required gestalt cache folder in
`/var/containers/Shared/SystemGroup/systemgroup.com.apple.mobilegestaltcache/Library/Caches`
2. Place file according to your bridgeOS version into this folder with filename
   `com.apple.MobileGestalt.plist`

### Support

For each bridgeOS version, we need to create an individual cache.

Currently, following bridgeOS versions are supported:

→ bridgeOS 9.2 22P2093

→ bridgeOS 9.2 22P3060 

→ bridgeOS 9.3 22P3051

→ bridgeOS 9.4 22P4248
