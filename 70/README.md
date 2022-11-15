# Creator authentication and encryption

Content creator authentication and encryption use the widely supported OpenPGP standard. An **authenticated keg** is one that includes one or more files signed by the content creator or that has been signed in its entirety and distributed as a `.keg` file (gzipped, tarred, signed).

* A **content creator** MUST publish authoritative `user.pubkey` in primary **user keg**.
* A **content creator** MAY include `user.pubkey` in one or more kegs (for convenience),
* A **content creator** MUST keep `user.pubkey` identical in all authenticated kegs.
* If defined, a `user.pubkey` MUST contain ASCII-armored body of a PGP/GPG public key.
* A **content creator** MAY detach-sign one or more content files with `gpg -b` (effectively).
* A **detach-signed file** MUST have an identically named file with `.sig` suffix.
* A **content creator** MAY encrypt-sign one or more content files with `gpg -s` (effectively).
* An **encrypt-signed file** MUST end with `.gpg` suffix (and unencrypted version removed).
* A **keg app** MAY optionally support content creator authentication and encryption.
* A **keg app** with authentication support MUST support binary `.gpg` and `.sig` files.
* A **keg app** with authentication support MUST support re-signing all signed files.
* A **content creator** MUST NOT use `.gpg` or `.sig` suffix on any file except for authentication.
* A **content creator** MAY distribute keg as optionally signed, gzipped tar ball.
* When creating gzipped tarballs the reserved `.keg` suffix should be used.
* A **content creator** MAY detach-sign or encrypt-sign a `.keg` distribution file.
* An encrypt-signed `.keg` file MUST also have a `.keg` suffix (not `.gpg`).
* A **keg app** just distinguish between `.keg` files that are or are not encrypted.
* A **content creator** MAY use regular, rotating encrypt-signing for [subscriptions](/71).

User information in the `keg` file of a **user keg** includes an optional public key that can be used to authenticate any **signed keg content** that the user has created. This authentication is optional and creates a dependency on **keg apps** but is available for those who wish it. The public key can also be kept secret and only given to other trusted users to provide encryption as well.

In order to use authentication a **content creator** must sign every file within a given keg for which they wish to provide proof that it came from them. Signing any file is trivial from the command line and very easy for **keg apps** since KEG uses cryptographic standards that have been established (and maintained) for decades.

To sign a file using just `gpg` all that is needed is either the `gpg -b` (detached) or `gpg -s` (encrypted) command which produces either a file with the same name as the signed file but with the `.sig` suffix or a full encrypted copy in a new file ending with `.gpg`. These file suffixes are reserved for authentication. Usually, when encrypt-signing creators delete the original, unencrypted file. 

::: Note

Note that the `.sig` file is *not* the ASCII armored version. Transport methods used to transfer KEG content are required to maintain the integrity of this binary file as is without any armoring.

:::


