# Description

In a rootless jailbreak environment, you might encounter errors while attempting to access app container folders, even when running SSH as a root user. This issue arises due to the binaries lacking the necessary entitlements.

# Usage

## Modify with ldid

1. For exemple, you can place the `entitlements.xml` file in the following directory: `/var/mobile/Documents/`

2. To modify `ls` binary, run the following command:

```shell
ldid -S/var/mobile/Documents/entitlements.xml /var/jb/usr/bin/ls
```

3. To modify `bash` binary, run this command:
   
```shell
ldid -S/var/mobile/Documents/entitlements.xml /var/jb/usr/bin/bash
```
## Download modified

Alternatively you can download in releases some binaries which I modified and place in `/var/mobile/Documents/`.

## References

- [Broken Permissions in iOS](https://www.reddit.com/r/jailbreak/comments/13rxm9t/question_broken_permissions_in/)
- [Error running cd or ls commands](https://www.reddit.com/r/jailbreak/comments/14wgy3k/comment/jrlyvir/)
- [Ldid on iPhoneDev Wiki](https://iphonedev.wiki/Ldid)

