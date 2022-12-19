# Last changed should only depend on `README.md` file

* A **content node** MAY contain files besides `README.md`
* KEG apps MAY synchronize the last modified file system info with **nodes index** entries
* Only the modification of `README.md` SHOULD be considered for last updated
* Changes to other files MUST be accompanied by `touch` to `README.md` to register update

While there is nothing officially specifying how a KEG app should handle the population of the **Changed** field in the **nodes index** entry for any given node, it is expected that most applications will reuse this same information from the file system hosting the content node files. In order to promote common expectations between such applications it is strongly suggested that applications always use the last modified time stamp of the `README.md` file itself and no others. This greatly improves the efficiency when scanning an entire keg for recent updates even though most applications will simply use the `nodes` file itself.
