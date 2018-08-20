# Extract source package info from Debian status files #

damngpl will parse a Debian-style /var/lib/dpkg/status file and extract source
package information about installed packages. This information can be used in
several ways, usually to download source packages.

Multiple input files can be specified on the command line, or piped into
standard input if no files are specified. Results are returned to standard
output.

The name damngpl was chosen as a tongue-in-cheek description of its purpose
(downloading Debian sources for the Finnix project to remain GPL compliant).
Please do not send hate mail to the author, thinking he is anti-GPL. He's not.

See also:
http://blog.finnix.org/2011/08/21/finnix-and-gpl-compliance/
## How to install `damngpl` using apt-get ##

1\. Add [Whonix's Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key).

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg adv --keyserver hkp://ipv4.pool.sks-keyservers.net:80 --recv-keys 916B8D99C38EAF5E8ADC7A2A8D66066A2EEACCDA
```

3\. Add Whonix's APT repository.

```
echo "deb http://deb.whonix.org stretch main" | sudo tee /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `damngpl`.

```
sudo apt-get install damngpl
```

## How to Build deb Package ##

Replace `apparmor-profile-torbrowser` with the actual name of this package with `damngpl` and see [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/apparmor-profile-torbrowser).

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Payments ##

`damngpl` requires [payments](https://www.whonix.org/wiki/Payments) to stay alive!
