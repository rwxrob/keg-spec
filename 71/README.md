# Subscriptions with encrypt-sign authentication

Content creators can control access to their new content by regular rotating their public key used to encrypt-sign their content. A **follower** who has obtained the new public key is referred to as a **subscriber**. The **subscription** model can be used to limit access and/or monetize any KEG content without requiring any **keg app** beyond the freely available `gpg` and `tar` commands.

::: Note

Note that the subscription model does not prevent anyone with access to previous public keys from accessing previously encrypt-signed content, only access to anything *new*.

:::
