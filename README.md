# r4sp1-config
skinny debian config to get comfortable / up and running

this was the biggest pain in the ass
so heres some notes so i never have such a hard time

## installation
guess you cant install `google-chrome-stable` on arm yet

>	`=> i bet manjaro can`

added `vim` to edit .config(s)

said fuckit, installed `firefox-esr`, heard they have amazing dev tools

couldnt get `brave-browser` to work either

fux'd w/ `raspi-config`, changed: 
should probably do these all from the terminal

-	`1` passwd 
-	`2 1` hostname
-	`3 3` disabled splashscreen
-	`5 2` enabled ssh
-	`7 3` up'd gpu memory split

i installed `i3`
had to `remove / re-add lightdm raspberrypi-ui-mods` to get lightdm settings to reset,
probably could have reset a daemon or something
not entirely comfortable with current settings, looking forward to updating

installed `stterm`, `sudo update-alternatives --config x-terminal-emulator`

edited `~/.config/i3/config`

-	moved bar to top
-	up'd font-size to 16 i believe

now i think im here, 
added an ssh-key

-	`ssh-keygen -t rsa -b 4096 -C "tom@technomad.media"`
-	`eval "$(ssh-agent -s)"`
-	`ssh-add ~/.ssh/id_rsa`
-	`ssh -T git@github.com`

guess i should push this huh

## ++
in pushing, default editor was nano (yuk!)
ran these two, one of them had to work `select-editor` `sudo update-alternatives --config editor`
