﻿#Configuration view

The configuration view displays file synchronization settings and lets you to modify them:

![Figure 1. Studio. Configuration view](images/configuration-view.png)  

##File conflict resolution

It sets the default built-in conflict resolver. You can choose one of the following option:

![Figure 2. Studio. Configuration view. Resolvers](images/configuration-view-resolvers.png)  

##Max number of synchronizations per destination

The synchronization limits the number of concurrent synchronization operations to a single destination file system. By default it allows
to perform `5` synchronizations simultaneously. Read [File locking](../../synchronization/how-it-works#file-locking-and-synchronization-timeout) for details.

##Synchronization lock timeout

The file is locked during the synchronization and cannot be modified. However to avoid potential deadlock there is the configurable timeout value
which specifies the max synchronization duration. Consider to increase this value if you work with very large files.
Read more about [the synchronization timeout](../../synchronization/how-it-works#file-locking-and-synchronization-timeout).

