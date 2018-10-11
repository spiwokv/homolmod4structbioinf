# How to install Modeller

From: [https://salilab.org/modeller/9.20/release.html#deb](https://salilab.org/modeller/9.20/release.html#deb)

The Debian/Ubuntu package should install on any modern .deb-based system. (It was, however, built and tested on
an Ubuntu 14.04 (Trusty Tahr) machine, so may not work on older systems.) If you do not have root access to your
Linux system, or wish to install in a non-standard location, you can use the generic Unix installer instead.

    * Download the correct Debian/Ubuntu package for your architecture.

    * Install the package by running the following command, replacing `XXXX` with the Modeller license key
    (and i386 with x86_64 if you are using the 64-bit installer).
```
sudo env KEY_MODELLER=XXXX dpkg -i modeller_9.20-1_i386.deb
```

    * If you have any version of Python between 2.3 and 3.6 installed on your system, you should be able to
    use Modeller from a regular "python" interpreter. For example, you could run the Modeller script foo.py by
    typing `python foo.py` from a command line (e.g. a GNOME terminal window, KDE Konsole window, etc.).
    Alternatively, you can run Modeller by typing `mod9.20` from a command line. (See below for example scripts.)

    * Documentation and examples can be found in the /usr/lib/modeller9.20/ directory. Note that you will need
    to make a copy of the examples directory in order to use it, e.g. `cp -a /usr/lib/modeller9.20/examples ~`.

    * To uninstall Modeller, run the following command: `sudo apt-get remove modeller`.
    
    
