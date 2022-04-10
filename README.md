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

1\. Download the APT Signing Key.

```
wget https://www.kicksecure.com/derivative.asc
```

Users can [check Whonix Signing Key](https://www.kicksecure.com/wiki/Signing_Key) for better security.

2\. Add the APT Signing Key..

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add the derivative repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.kicksecure.com bullseye main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
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

See instructions.

NOTE: Replace `generic-package` with the actual name of this package `damngpl`.

* **A)** [easy](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.kicksecure.com)
* [Professional Support](https://www.kicksecure.com/wiki/Professional_Support)

## Donate ##

`damngpl` requires [donations](https://www.kicksecure.com/wiki/Donate) to stay alive!
