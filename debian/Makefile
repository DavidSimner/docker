default:
	sudo rm -rf build/
	sudo debootstrap --variant=minbase --exclude=apt-transport-https,ca-certificates testing build/
	sudo chroot build/ apt-get purge --yes debconf-i18n gcc-4.8-base liblocale-gettext-perl libtext-charwidth-perl libtext-iconv-perl libtext-wrapi18n-perl
	sudo rm build/run/utmp
	sudo rm -r build/dev/ build/proc/ build/sys/
	sudo rm build/etc/group- build/etc/gshadow- build/etc/passwd- build/etc/shadow- build/etc/subgid- build/etc/subuid-
	sudo rm -r build/var/cache/apt/ build/var/lib/apt/
	sudo rm build/etc/hostname build/etc/resolv.conf
	sudo tar -C build/ -c . | sudo docker import - debian
