# Directory

* This **specification** SHALL NOT require any specific means of content transfer.
* This **specification** SHALL define how content is stored, organized, and authenticated.
* A KEG **directory** MAY be referred to as a **keg** or **keg site**.
* A **keg** MUST include a [**zero node**](/59).
* A **keg** SHOULD contain one [**node**](/39) besides **zero node**.
* A **keg** MUST contain a `keg` [**info file**](/48).
* A **keg** MAY contain a `follow` file with URLs of kegs to follow.
* A **keg** MAY contain an `avoid` file with URLs of kegs to avoid.
* A **keg** MAY contain other files but never secrets.

A KEG **directory** (or "keg") contains a collections of KEG **nodes** where knowledge content is organized into a flat structure with each node focusing on one main idea. A keg also contains information about what other kegs to follow (usually related to this keg) and which to avoid because they have problems of one kind or another and cannot be trusted. This `follow` and `avoid` information is available to anyone who follows the keg and provides consistent way to share knowledge with others by any means possible including, but not limited to, the Internet. A **keg** is structured such that it can easily be compressed and copied onto any storage device and shared "by foot" if necessary as well. This simplicity and portability is what makes KEG particularly special as a method of knowledge management and exchange.

A KEG directory may contain any number of other files, but SHOULD avoid large files.

* [KEG nodes index file](/3)
* [KEG directory schema](/48)
