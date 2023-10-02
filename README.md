# ldidentitlements

**Description**: Modify entitlements for specific binaries to access container folders.

## Example of Use

1. Place the `entitlements.xml` file in the following directory:

/var/mobile/Documents/

2. To modify the `ls` binary, run the following command:

```shell
ldid -S/var/mobile/Documents/entitlements.xml /var/jb/usr/bin/ls

To modify the bash binary, run this command:

ldid -S/var/mobile/Documents/entitlements.xml /var/jb/usr/bin/bash
