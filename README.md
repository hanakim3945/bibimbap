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

→ bridgeOS 9.3 22P3051

→ bridgeOS 9.3 22P3060 

→ bridgeOS 9.4 22P4248

→ bridgeOS 9.5 22P5072


### Known issues
- When creating caches for new bridgeOS versions, there can be touchbar issues as we have to manually adjust the size of CacheData inside the plist. Those manually added bytes require lots of testing until we find the perfect configuration. There is probably a smarter method out there, but i didn't find it yet.
- Remoted panics and mac reboots after a few minutes because of a watchdog timeout. Same reason as with the touchbar, the CacheData is mysterious...
