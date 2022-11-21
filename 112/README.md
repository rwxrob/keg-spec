# Why YAML for `keg` info file?

The **keg info file** is the most important file in any **keg**. It identifies the content as being a keg or **KEG Web** site or repo. The `keg` file is the most read and written file of any other on any KEG network. It follows therefore that it should be the easiest to read and write as is.

KEG focuses on the least necessary technology and YAML for the keg info file is just more maintainable and readable by everyone. Unlike the indexes, this file is required in every keg. Therefore, it makes sense to make this feel as easy to read and write as possible. In fact, a **KEG app** can safely just dump the plain text of the `keg` YAML file and be sure that anyone can just read that without further formatting or rendering of any kind.

The **updated** field must also always be at the top of that file ensuring the least amount of tech required to read the first 30 characters of any keg to know if it has been updated. No complicated decryption or even HTTP protocol requests.
