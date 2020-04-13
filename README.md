# r4sp1-config
skinny debian config to get comfortable / up and running  
some notes to have an easier time

## todo .dotfiles

- [ ] .vimrc
- [ ] .vim/
- [ ] .tmux.conf
- [ ] .zshrc
- [ ] esc/caps
- [ ] ctrl/alt
- [ ] i3 mod1 => mod4

## installation

### raspi-config `#do-in-terminal`
	1   passwd 
	2.1 hostname
	3.3 disabled splashscreen
	4.4 set wifi country code
	5.2 enabled ssh
	7.3 upped gpu_memory_split

### sudo apt install

	vim
		select-editor
		update-alternatives --config editor
	i3
		remove lightdm raspberrypi-ui-mods && add lightdm raspberrypi-ui-mods
			# ? reset daemon
		vim ~/.config/i3/config
			font-size: 16
			bar [ top ]
	stterm
		update-alternatives --config x-terminal-emulator
	tmux

### ssh-key
	ssh-keygen -t rsa -b 4096 -C "tom@technomad.media"
	eval "$(ssh-agent -s)"
	ssh-add ~/.ssh/id_rs`
	ssh -T git@github.com

### optional
	firefox-esr
	* looking foward to their dev tools
	awesome awesome-extra
	* looking forward to playing with
	* might be more simple than i3


## maybe-later?

### ARManjaro `#google-chrome-stable` `#brave-browse`

### change user pi `#buggy` `#security_risk`

1. http://unixetc.co.uk/2016/01/07/how-to-rename-the-default-raspberry-pi-user/

    https://thepihut.com/blogs/raspberry-pi-tutorials/how-to-change-the-default-account-username-and-password

    https://www.raspberrypi.org/forums/viewtopic.php?t=233034

    https://www.raspberrypi.org/forums/viewtopic.php?f=63&t=227620#p1396338

    https://raspberrypi.stackexchange.com/questions/12827/change-default-username

