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

1\. Download Whonix's Signing Key.

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/derivative.gpg add ~/patrick.asc
```

3\. Add Whonix's APT repository.

```
echo "deb https://deb.whonix.org bullseye main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `damngpl`.

```
sudo apt-get install damngpl
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions. (Replace `generic-package` with the actual name of this package `damngpl`.)

* **A)** [easy](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`damngpl` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
