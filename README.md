
## Example of Use

1. Place the `entitlements.xml` file in the following directory:

<code>/var/mobile/Documents/</code>

2. To modify `ls` binary, run the following command:

```shell
ldid -S/var/mobile/Documents/entitlements.xml /var/jb/usr/bin/ls
```
To modify `bash` binary, run this command:
```shell
ldid -S/var/mobile/Documents/entitlements.xml /var/jb/usr/bin/bash
```
