# gensyn-rl-swam-bug

Selam Arkadaşlar Şu Şekilde Hata Alan arkadaşlarımıız şu işlemleri yapsın

![5774081641524872733](https://github.com/user-attachments/assets/ad3b2607-f1df-4659-98e1-38e058ebbee4)

```
cd
```

```
nano ~/.bashrc
```

FULL KOPYALAYIP İÇİNE YAPIŞTIRIN.

```
# ~/.bashrc: executed by bash(1) for non-login shells.

[ -z "${PS1:-}" ] && return

HISTCONTROL=ignoredups:ignorespace
shopt -s histappend
HISTSIZE=1000
HISTFILESIZE=2000
shopt -s checkwinsize

[ -x /usr/bin/lesspipe ] && eval "$(SHELL=/bin/sh lesspipe)"

if [ -z "$debian_chroot" ] && [ -r /etc/debian_chroot ]; then
    debian_chroot=$(cat /etc/debian_chroot)
fi

case "$TERM" in
    xterm-color) color_prompt=yes;;
esac

#force_color_prompt=yes
if [ -n "$force_color_prompt" ]; then
    if [ -x /usr/bin/tput ] && tput setaf 1 >&/dev/null; then
        color_prompt=yes
    else
        color_prompt=
    fi
fi

if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\$ '
else
    PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
fi

unset color_prompt force_color_prompt

case "$TERM" in
xterm*|rxvt*)
    PS1="\[\e]0;${debian_chroot:+($debian_chroot)}\u@\h: \w\a\]$PS1"
    ;;
*)
    ;;
esac

if [ -x /usr/bin/dircolors ]; then
    test -r ~/.dircolors && eval "$(dircolors -b ~/.dircolors)" || eval "$(dircolors -b)"
    alias ls='ls --color=auto'
    alias grep='grep --color=auto'
    alias fgrep='fgrep --color=auto'
    alias egrep='egrep --color=auto'
fi

alias ll='ls -alF'
alias la='ls -A'
alias l='ls -CF'

if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi

export PATH="$HOME/.yarn/bin:$HOME/.config/yarn/global/node_modules/.bin:$PATH"
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"

# Eğer PS1 tanımlı değilse bir varsayılan ver
if [ -z "$PS1" ]; then
    export PS1="\u@\h:\w\$ "
fi
```

CTRL X Y enter. kaydet çık.




```
source ~/.bashrc
```


# Son Adımda local hatsaı alanlar için.


![Ekran görüntüsü 2025-04-19 215324](https://github.com/user-attachments/assets/d70656fa-48c7-42f9-b77a-716a454c3e8f)



size attığım ssdeki kısmın başına # koyun arkadaşlar.
open http://localhost:3000 başına # koyun.


![Ekran görüntüsü 2025-04-19 215246](https://github.com/user-attachments/assets/5bfa864d-cddb-49b1-80e0-c14c53107eb5)



```
cd
```


```
sudo nano /rl-swarm/run_rl_swarm.sh
```


CTRL X Y enter kaydedin



Ardından Tekrar çalıştırmayı deneyin.
