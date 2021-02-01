# svg2icns

macOS tool to convert svg to icns files

## Requirements

This script should run without installing anything extra if you're on a recent macOS.

It requires iconutil and sips, which come with macOS. It requires one of these: qlmanage (included with macOS), svg2png, inkscape, or ImageMagik. If for some reason you don't have qlmanage, you can install one of the others with homebrew (see https://brew.sh to install that)

	brew install svg2png # only install if you don't have qlmanage, you probably do
	brew install inkscape # only install if you don't have qlmanage, you probably do
	brew install imagemagik # only install if you don't have qlmanage, you probably do

I should probably remove everything but qlmanage but I'm leaving it in for now because I just found out about qlmanage and I don't know how common it is. And it's useful to know how the others do it too.

## Install

Install for all users

	curl -o /usr/local/bin/svg2icns https://raw.githubusercontent.com/magnusviri/svg2icns/main/svg2icns
	chmod 755 /usr/local/bin/svg2icns

Install in the current directory

	curl -O https://raw.githubusercontent.com/magnusviri/svg2icns/main/svg2icns
	chmod 755 svg2icns

## The Opposite

Put this in your ~/.zshrc if you want the opposite:

    alias icns2png='sips -s format png \!:1 --out \!:2'

## Credits

This script combines all 3 of these scripts:

http://www.spaziocurvo.com/2015/03/svg-to-icns-script-for-mac-os-x/
https://gist.github.com/zlbruce/883605a635df8d5964bab11ed75e46ad
https://gist.github.com/Canorus/1bc13e4b9ced1df79d396141de6178e4

I added the inkscape line and reorganized everything.