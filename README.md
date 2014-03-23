dotfiles
========

These are some settings and configurations that make my life easier. I've gathered these from different sources over time, so I can't give much credit. If you want to get more serious about dotfiles, here's the ultimate source of information: [http://dotfiles.github.io/](http://dotfiles.github.io/)

Anyway, you can use these scripts however you prefer. Here's how I make the best use of them:

## Bash
.bash_custom is a script compiled from the other one. I keep the others for easier management, and this one for easier use on remote machines. When I login to a machine I want this script on, I just run this command in home directory:

    curl -L https://raw.github.com/marlek/dotfiles/master/bash/.bash_custom > .bash_custom

and then add this line to .bash_profile, or .profile, or whichever file you system uses:

    source ~/.bash_custom

Make sure you set `my_hostname` variable, since the script uses this one to decide whether to display user and hostname in prompt. I keep local hostname in this variable, so I have a clean prompt on my computer, but when I copy the script to a remote machine I always have user and hostname displayed.
Below 'my_hostname' you can also set the preferred editor for you command line.

## OSX
These are some commands I extracted from: [https://gist.github.com/brandonb927/3195465](https://gist.github.com/brandonb927/3195465)
You only need to run this script once per user on you machine, like this:

    sh ./.osx
