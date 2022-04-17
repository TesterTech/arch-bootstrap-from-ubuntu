arch-bootstrap
==============

Bootstrap a base Arch Linux system from Ubuntu specifically.

Preconditions
=======
- Have tested this on 20.04 choosing a minimal installation. 
- Install Ubuntu and keep in mind that you should have a specific partition for Arch Linux. Or else this is not going to work.
- ```sudo apt install -y git vim openssh-server curl zstd arch-install-scripts```


Install
=======

    # install -m 755 arch-bootstrap.sh /usr/local/bin/arch-bootstrap

Examples
=========

Create a base arch distribution in directory 'archroot' (currently running arch by default):

    # arch-bootstrap /opt/archroot
  

Usage
=====

Once the process has finished, chroot to the destination directory (default user: root/root):

    # chroot destination


Postinstall 
=====

echo "Note: automatic fstab in /etc/fstab.auto be sure to change!"
sudo genfstab  -U / > /tmp/fstab.auto
sudo cp /tmp/fstab.auto /mnt/archroot/etc/fstab.auto

    
    


License
=======

This project is licensed under the terms of the MIT license
