# transmission-readynas-legacy-arm

Latest version is: legacy-arm-2.84-0.07

This is a special build of Transmission Bittorrent client as an add-on for legacy NETGEAR ReadyNAS storage systems based on ARM architecture - DUO v2 (RND2000v2), NV+ v2 (RND4000v2).

You can download the add-on in the Releases section: https://github.com/ssurba/transmission-readynas-legacy-arm/releases

## General notes:

* You may find release notes for Transmission on Transmission developers site: https://trac.transmissionbt.com/wiki/Changes.

* This package has been tested with version 5.3.11 of the RAIDiator firmware. It will work with newer versions, I recommend upgrading the firmware to the latest version (5.3.11 to the moment of writing).

* Only transmission-daemon, client tools and Web interface are included in this package.

* After installing you should be able to access web interface in your browser by the following URL: http://[ip_address_of_your_NAS]:9091.

* Transmission network share will be created after installation. In most cases you won't need it, it provides access to Transmission configuration file (settings.json), watch directory and other special files.

* By default downloaded files are saved to /Media/Torrents. You may later change it in Transmission configuration.

* Your NAS should be connected to the Internet while installing this package. Otherwise you may experience delays during the installation and installation process may end up with error due to timeout. This error can be ignored and the package should be installed successfully.

**WARNING!** Before installing this version please **uninstall any other builds** of Transmission (versions not made by me) and **delete Transmission share** created by the other build. But you can keep previous version of my build and Transmission share created by it, newer version should use and upgrade them.

# Version changes:

## Version 0.07

* Release for GitHub.

## Version 0.06

* Compiled with uTP support.

## Version 0.05

* Enabled watch directory, by default it is located in Transmission share - \transmission\watch-dir. Put your .torrent files in it to start downloading. 

## Version 0.04b

* Included transmission-cli and other client tools in the build. Some fixes to directory structure that might be preventing original Media share to appear.

## Version 0.03

* Fixed stop.sh script to shutdown Transmission correctly and allow it to save changes to settings.json. (Thanks *Gray75*)

## Version 0.02

* Fixed FTP access problem with proftpd crash by setting correct permissions on /var/log, also moved Transmission log to /var/log/transmission/transmission.log. (Thanks *Torry*)
* Added logrotate.d config for Transmission log files maintenance.
* Put a link to Transmission's web interface URL on Add-on Manager page. The Add-on Manager page is automatically reconfigured on start of Transmission to reflect changes in IP address of the ReadyNAS and/or Transmission web interface port (9091 by default).

## Version 0.01

* Initial release.
