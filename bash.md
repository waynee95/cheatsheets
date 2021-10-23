# Bash

## View content of zip file

```bash
$ zipinfo foo.zip
```

## Find total number of files in current directory

```bash
$ ls | wc -l
```

## Install termite terminal

```bash
curl "https://raw.githubusercontent.com/Corwind/termite-install/master/termite-install.sh" | sh
```

## Install Dropbox

```bash
$ cd ~
$ wget -O dropbox.tar.gz "http://www.dropbox.com/download/?plat=lnx.x86_64"
$ tar -tzf dropbox.tar.gz
$ tar -xvzf dropbox.tar.gz
$ ~/.dropbox-dist/dropboxd
```

## Install Dropbox Cli

```bash
$ mkdir -p ~/bin
$ wget -O ~/bin/dropbox.py "https://www.dropbox.com/download?dl=packages/dropbox.py"
$ chmod +x ~/bin/dropbox.py
```

## Find text in directory

```bash
$ grep -Ril "text-to-find-here"
```

- i stands for ignore case (optional in your case)
- R stands for recursive
- l stands for "show the file name, not the result itself"
- / stands for starting at the root of your machine

## Make teamspeak run from dmenu

```bash
$ sudo ln -s $HOME/Downloads/TeamSpeak3-Client-linux_amd64/ts3client_runscript.sh /bin/teamspeak3
```

## Download yt from list in file

```bash
#!/bin/bash
filename="$1"
while read -r line
do
  youtube-dl $line
done < "$filename"
```

## Download youtube video as mp3

```bash
$ youtube-dl -x --audio-format mp3 "<link>"
```

## Copy command contents to clipboard

```bash
$ cat file | xclip
```

To paste the copied text, you use:

```bash
$ xclip -o
```

## Using sed to replace curly braces

```bash
$ sed -i 's#{test1}#test2#' file
```

You cannot escape curly braces in sed.

## Recursively delete all files of specific extension in current directory

```bash
$ find . -name "*.bak" -type f -delete
```

To see which files will be deleted beforehand, you can use

```bash
$ find . -name "*.bak" -type f
```

Make sure -delete is the last argument. Otherwise, it will delete
**everything**.

## Reverse mouse scrolling

```bash
$ xmodmap -e "pointer = 1 2 3 5 4 7 6 8 9 10"
```

## Watch file and re-compile

This requires entr to be installed.

```bash
$ ls *.tex | entr latex filename.tex
```

## Turn of network connection

```bash
$ nmcli networking off
```

To enable it, replace off with `on`.

## Remove everything except one file

```bash
$ ls | grep -v file.txt | xargs rm
```

-v, --invert-match
Matches everything except the specifed file.

## Run steam apps from the terminal

```bash
$ steam steam://rungameid/363890
```

The ID can be found https://steamdb.info/apps/.

## Search and replace using grep and sed

```bash
$ grep -rl matchstring somedir/ | xargs sed -i 's/string1/string2/g'
```

## Invert mouse scrolling

```bash
$ "xinput set-prop "USB Optical Mouse" "libinput Natural Scrolling Enabled" 1"
```

## Refresh audio

```bash
$ sudo alsa force-reload﻿
```

## Concat all files in folder

```bash
$ cat * > filename
```

## Get word count in a file

```bash
$ wc -w filename
```

## Filter out tree command

```bash
$ tree -I "*.pdf|*.log"
```

## Logout from terminal

```bash
$ sudo pkill -KILL -u waynee95
```

## Run command on all files

```bash
$ find ./**/*.nix | xargs nixfmt -c
```

## Pipe result of command into Vim

```bash
$ echo "hello world!" | vim -
```

## Find command

Find all .txt files recursively starting in current directory.

```bash
$ find . -name "*.txt"
```

To limit the depth use `-maxdepth n`, where `n=1` would be current directory only.

To ignore casing, use `-iname` instead.

Find directory with certain name.

```bash
$ find -type d -name "gradle"
```

Find all haskell files and print the file contents.

```bash
$ find . -maxdepth 3 -name "*.hs" -exec cat {} \;
```

## Download list of PDFs from website using wget

```bash
$ wget -m -p -E -k -K -np http://site/path/
```

## Count all lines of code inside a folder

```bash
$ find . -name "*.js" | xargs wc -l
```

## Install Flatpak Apps

```bash
$ sudo apt install flatpak
$ flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
$ flatpak install flathub com.elsevier.MendeleyDesktop
$ flatpak install flathub ch.openboard.OpenBoard
```

## Install new fonts

```
$ mkdir ~/.fonts/<font-family-name>
$ mv *.ttf ~/.fonts/<font-family-name>
$ fc-cache -f -v
```

## Remove last page from PDF using command line

```
sudo apt install pdftk
pdftk input.pdf cat 1-2 output out.pdf
```

## Convert djvu to pdf

```bash
$ djvups input.djvu | ps2pdf - output.pdf
```
