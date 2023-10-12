# Description

In a rootless jailbreak environment, you might encounter errors while attempting to access app container folders, even when running SSH as a root user. This issue arises due to the binaries lacking the necessary entitlements.

> [!WARNING]  
> Always backup the binaries you want to modify.

# Usage

You have three options to choose from according to your needs. 

## Filza Script (recommended) 

1. First, install [this deb file](https://github.com/pedromopi/ldidentitlements/releases/download/deb/com.pedromopi.containerentitlements_1.0.0_iphoneos-arm64.deb).
2. Open Filza and navigate to `/var/jb/usr/bin`.
3. Locate the binary you want to modify, then follow these steps:

   a. Right-click or tap and hold the binary file.
   b. Select "Scripts" from the context menu.
   c. Choose "Container Entitlement."

   This script performs the following actions:

   - If no container entitlement exists, it will create one and set it to true.
   - If a container entitlement already exists but is set to false, it will change it to true.
   - If a container entitlement exists and is set to true, it will be changed to false.

   This approach allows you to easily revert the action if needed.


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

Alternatively, you can download pre-modified binaries from the 'Releases' section and then place them in `/var/mobile/Documents/`.

## References

- [Broken Permissions in iOS](https://www.reddit.com/r/jailbreak/comments/13rxm9t/question_broken_permissions_in/)
- [Error running cd or ls commands](https://www.reddit.com/r/jailbreak/comments/14wgy3k/comment/jrlyvir/)
- [Ldid on iPhoneDev Wiki](https://iphonedev.wiki/Ldid)


<sub>Thanks to [blanxd](https://www.reddit.com/user/blanxd/) for discovering this.</sub>

