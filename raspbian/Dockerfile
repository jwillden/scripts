FROM scratch
ADD ./2021-01-11-raspios-buster-armhf-lite.gz /
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get -y autoremove
RUN apt-get -y autoclean
RUN apt-get -y clean
RUN rm -rf ~/Desktop
RUN rm -rf ~/python_games
RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get -y install vim
RUN apt-get -y purge --autoremove scratch
RUN apt-get --yes purge xserver-common x11-xfs-utils x11-xserver-utils xinit libsmbclient blt gvfs gvfs-backends gvfs-daemons gvfs-fuse idle idle-python2.7 idle3 libaudio2 libice6 liblightdm-gobject-1-0 libpulse0 libqt4-svg libqtgui4 libsdl-image1.2 libsdl-mixer1.2 libsdl-ttf2.0-0 libsdl1.2debian libsm6 libsmpeg0 libwebkitgtk-1.0-0 libwebkitgtk-3.0-0 libxaw7 libxklavier16 libxmu6 libxss1 libxt6 libxtst6 lightdm lightdm-gtk-greeter lxde lxde-core midori nano obconf openbox python-pygame python-tk python3-tk  scratch tk8.5 wpagui x11-common x11-utils x11-xkb-utils xinit xserver-common xserver-xorg xserver-xorg-core xserver-xorg-input-all xserver-xorg-input-evdev xserver-xorg-input-synaptics xserver-xorg-video-fbdev zenity xserver* x11-common x11-utils x11-xkb-utils x11-xserver-utils xarchiver xauth xkb-data console-setup xinit lightdm lxde* obconf openbox gtk* libgtk* alsa* nano python-pygame python-tk python3-tk scratch tsconf desktop-file-utils cifs-utils samba-common smbclient
RUN apt-get --yes purge cups-bsd cups-client fonts-droid fuse gettext-base ghostscript gnome-accessibility-themes gnome-themes-standard-data libasound2 libasprintf0c2 libasyncns0 libaudit0 libcaca0 libcupsimage2 libfile-copy-recursive-perl libflac8 libfm-data libfuse2 libgs9 libgs9-common libid3tag0 libijs-0.35 libjbig2dec0 libmad0 libmenu-cache1 libmtdev1 libogg0 libpaper-utils libpaper1 libpciaccess0 libportmidi0 libqt4-network libqt4-xml libqtdbus4 libsamplerate0 libsndfile1 libutempter0 libvorbis0a libvorbisenc2 libvorbisfile3 libvte-common  libwnck-common poppler-data python-numpy python-support tcl8.5 update-inetd xbitmaps zenity-common aspell aspell-en console-setup-linux cups-common dconf-gsettings-backend dconf-service dictionaries-common fontconfig fontconfig-config gconf2-common glib-networking glib-networking-common glib-networking-services gsettings-desktop-schemas gsfonts hicolor-icon-theme iso-codes libaspell15 libatk1.0-0 libatk1.0-data libavahi-client3 libavahi-common-data libavahi-common3 libavahi-glib1 libbluetooth3 libbluray1 libck-connector0 libcups2 libdatrie1 libdrm2 libenchant1c2a libexif12 libfontconfig1 libfontenc1 libgconf-2-4 libgdk-pixbuf2.0-common  libglapi-mesa libgnome-keyring-common libgnome-keyring0 libjasper1 libjpeg8 liblcms1 liblcms2-2 libltdl7 libmng1 libnettle4 liborc-0.4-0 libpam-ck-connector libpixman-1-0 libpolkit-agent-1-0 libpolkit-backend-1-0  libqtcore4 libthai-data libthai0 sgml-base ttf-dejavu-core xml-core
COPY bashrc /root
RUN mv /root/bashrc /root/.bashrc
RUN apt-get -y autoremove
ENV DEBIAN_FRONTEND=
CMD ["/bin/bash"]

