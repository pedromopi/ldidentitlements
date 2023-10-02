
## Example of Use

# Modify with ldid

1. Place the `entitlements.xml` file in the following directory: `/var/mobile/Documents/`

2. To modify `ls` binary, run the following command:

```shell
ldid -S/var/mobile/Documents/entitlements.xml /var/jb/usr/bin/ls
```

3. To modify `bash` binary, run this command:
   
```shell
ldid -S/var/mobile/Documents/entitlements.xml /var/jb/usr/bin/bash
```
# Download modified

Alternatively you can download in releases some binaries which I modified.
