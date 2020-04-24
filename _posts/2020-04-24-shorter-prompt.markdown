---
layout: post
title:  "Personalizar el Prompt"
date:   2020-04-24 08:00:00 -0500
categories: Debian Terminal Bash Conda
tags: moc debian sid m4a ffmpeg
sidebar: my_sidebar
summary: "Cansado de que el prompt de mi acostumbrada terminal saturara casi todo el ancho de mi pantalla, me aventuré a probar difentes opciones de visualización del mismo."
#author: kinichi
#permalink: "/debian/MOC/"
#{{page.categories | capitalize | join: ', '}}
---


{% highlight bash%}
conda config --set auto_activate_base false
{%endhighlight%}


{% highlight bash%}
PROMPT_DIRTRIM=1
{%endhighlight%}

{% highlight bash %}
if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]kinichi\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
else
    PS1='${debian_chroot:+($debian_chroot)}kinichi:\w\$ '
fi
{% endhighlight %}
