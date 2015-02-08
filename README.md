# transmission-readynas-arm

Latest version is: 2.84-0.06-ssurba-arm

This is a special build of Transmission Bittorrent client as an add-on for NETGEAR ReadyNAS storage systems based on ARM architecture - DUO v2 (RND2000v2), NV+ v2 (RND4000v2).

General notes:

Release notes for Transmission you can read on Transmission developers site: https://trac.transmissionbt.com/wiki/Changes.
This package was tested with version 5.3.11 of the RAIDiator firmware. It will work with newer versions, I recommend upgrading the firmware to the latest version (5.3.11 to the moment of writing).
Only transmission-daemon, client tools and Web interface are included in this package.
After installing you should be able to access web interface in your browser by the following URL: http://[ip_address_of_your_NAS]:9091.
Transmission network share will be created after installation. In most cases you won't need it, it provides access to Transmission configuration file (settings.json), watch directory and other special files.
By default downloaded files are saved to /Media/Torrents. You may later change it in Transmission configuration.
Your NAS should be connected to the Internet while installing this package. Otherwise you may experience delays during the installation and installation process may end up with error due to timeout. This error can be ignored and the package should be installed successfully.
Before installing this version please remove any other builds of Transmission (versions not made by me). But you can keep previous version of my build, newer version will upgrade it.
