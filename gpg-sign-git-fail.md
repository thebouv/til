I was receiving this error in a new repo. I sign all commits by default, but it was failing:

```
error: gpg failed to sign the data 
fatal: failed to write commit object
```

Looks like the `gpg-agent` was misbehaving as my config was all set up correct for signing. Likely something got updated and the agent needed a restart:

`gpgconf --kill gpg-agent`

As learned from: https://superuser.com/questions/1075404/how-can-i-restart-gpg-agent/1150399#1150399