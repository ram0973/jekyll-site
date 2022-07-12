---
title: Install minimal Debian Testing
date: 2022-07-12 09:16:47 Z
categories:
- debian
layout: post
---

/etc/apt/sources.list - 1 line - add contrib non-free and change to mirror.yandex.ru

{% highlight bash %}
sudo apt-mark hold gnome-games libreoffice-core firefox-esr
sudo apt install gnome-core
{% endhighlight %}

/etc/network/interfaces # тут закомментировать всё

/etc/NetworkManager/NetworkManager.conf содержит:

[main]

plugins=ifupdown,keyfile

[ifupdown]

managed=true

-------

wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -

sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'

sudo apt update && sudo apt install google-chrome-stable

-------

sudo apt install gnome-tweaks

Extensions - User themes - on, Removable Drive Menu - on

Go to Gnome Extensions website - install plugin "Gnome Shell integration"

Reload page

Install:

Dash to Panel

Bring Out Submenu Of Power Off/Logout button

Dash to Panel settings - Width 42px - Opacity 50

Override panel theme color to desirable (dark red)

-------

Terminal - Enable the menu accelerator key -disable

colors - tango dark/tango

size - 132 x 32

-------

Download && Install Jetbrains mono fonts
{% highlight bash %}
sudo apt install fonts-jetbrains-mono
{% endhighlight %}
Interface - set Nimbus

-------

Install Jetbrains Toolbox App

Download and:

sudo tar -xzf jetbrains-toolbox-* -C /opt

Install Jetbrains Idea community

sudo apt install ttf-mscorefonts-installer

sudo apt install papirus-icon-theme

Change fonts to PT Sans regular & Jetbrains Mono

Change icons to papirus

Change wallpaper (Second is good)

TITLE BARS - MAX, MIN

Ant theme - ggsettings set org.gnome.desktop.wp.preferences theme Ant

Ant theme - ggsettings set org.gnome.desktop.interface gtk-theme Ant

-------

Anydesk

wget -qO - https://keys.anydesk.com/repos/DEB-GPG-KEY | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/anydesk.com.gpg

echo "deb http://deb.anydesk.com/ all main" | sudo tee /etc/apt/sources.list.d/anydesk-stable.list
{% highlight bash %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
