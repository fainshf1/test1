hello_2.10-2_amd64.deb is used as a basic Debian package for performing test.

Downloaded using: 
    wget ftp://ftp.de.debian.org/debian/pool/main/h/hello/hello_2.10-2_amd64.deb

Extracted using: 
    dpkg-deb -x ./hello_2.10-2_amd64.deb /home/$USER/Canonical/asssignment/hello
    cd /home/$USER/Canonical/asssignment/hello
    dpkg-deb -e ../hello_2.10-2_amd64.deb

Build using:
    dpkg-deb -b --root-owner-group hello

Files added to the archive:
   ./usr/share/hello/testing.sh ## made executable
   ./DEBIAN/postinst

Installed using:
   cp hello_2.10-2my1_amd64.deb /tmp/ && cd /tmp && sudo dpkg -i ./hello_2.10-2my1_amd64.deb

Verified using:
   TESTCMD=$(dpkg -S testing.sh | awk '{print $2;exit}') && eval $TESTCMD

Output:
asusl@asusl-N550JK:~/Canonical/asssignment$ cp hello_2.10-2my1_amd64.deb /tmp/ && cd /tmp && sudo dpkg -i ./hello_2.10-2my1_amd64.deb

Selecting previously unselected package hello.

(Reading database ... 309975 files and directories currently installed.)

Preparing to unpack ./hello_2.10-2my1_amd64.deb ...

Unpacking hello (2.10-2) ...

Setting up hello (2.10-2) ...

this is a test from Edik Fainshtein

Processing triggers for install-info (6.8-4build1) ...

Processing triggers for man-db (2.10.2-1) ...

asusl@asusl-N550JK:/tmp$ TESTCMD=$(dpkg -S testing.sh | awk '{print $2;exit}') && eval $TESTCMD

this is a test from Edik Fainshtein
