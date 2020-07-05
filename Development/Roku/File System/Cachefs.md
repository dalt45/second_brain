# Cachefs
Developers can use the cachefs: file system to allow applications to cache data to volatile or persistent storage instead of tmp:. End-users can add an external SD card to their device which will preserve the data even after a system reboot and improve performance. Users without extended storage also benefit from the use of a shared in-memory cache that is automatically managed by the system to optimize for the most recently used assets.

Note that the OS can evict the data at any time, such as when another channel decides to write so much data that space is required. Thus, a channel should always check for the existence of the file they wrote to before relying on the data cache.

Depending on your application's requirements, you can choose one of these options. Interfaces to the registry are documented at roRegistry. Interfaces to files are described below.

