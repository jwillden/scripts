FROM scratch
ADD ./2021-01-11-raspios-buster-armhf-lite.gz /
RUN apt-get purge --auto-remove scratch debian-reference-en dillo idle3 python3-tk idle python-pygame python-tk lightdm gnome-themes-standard gnome-icon-theme raspberrypi-artwork gvfs-backends gvfs-fuse desktop-base lxpolkit zenity xdg-utils mupdf gtk2-engines alsa-utils  lxde lxtask menu-xdg gksu midori xserver-xorg xinit xserver-xorg-video-fbdev libraspberrypi-dev libraspberrypi-doc dbus-x11 libx11-6 libx11-data libx11-xcb1 x11-common x11-utils lxde-icon-theme gconf-service gconf2-common
RUN sudo apt-get --yes purge xserver-common x11-xfs-utils x11-xserver-utils xinit libsmbclient blt gvfs gvfs-backends gvfs-daemons gvfs-fuse idle idle-python2.7 idle-python3.2 idle3 libaudio2 libice6 liblightdm-gobject-1-0 libobrender27 libpulse0 libqt4-svg libqtgui4 libsdl-image1.2 libsdl-mixer1.2 libsdl-ttf2.0-0 libsdl1.2debian libsm6 libsmpeg0 libwebkitgtk-1.0-0 libwebkitgtk-3.0-0 libxaw7 libxklavier16 libxmu6 libxss1 libxt6 libxtst6 lightdm lightdm-gtk-greeter lxde lxde-core midori nano obconf openbox python-pygame python-tk python3-tk  scratch tk8.5 wpagui x11-common x11-utils x11-xkb-utils xinit xserver-common xserver-xorg xserver-xorg-core xserver-xorg-input-all xserver-xorg-input-evdev xserver-xorg-input-synaptics xserver-xorg-video-fbdev zenity xserver* x11-common x11-utils x11-xkb-utils x11-xserver-utils xarchiver xauth xkb-data console-setup xinit lightdm libx{composite,cb,cursor,damage,dmcp,ext,font,ft,i,inerama,kbfile,klavier,mu,pm,randr,render,res,t,xf86}* lxde* lx{input,menu-data,panel,polkit,randr,session,session-edit,shortcut,task,terminal} obconf openbox gtk* libgtk* alsa* nano python-pygame python-tk python3-tk scratch tsconf desktop-file-utils cifs-utils samba-common smbclient
RUN apt --yes autoremove
RUN apt --yes autoclean
RUN apt --yes clean
RUN rm -r ~/Desktop
RUN rm -r ~/python_games
RUN apt --yes update
RUN apt --yes upgrade

CMD ["/bin/bash"]

