---
title: "Customize Zsh"
date: 2022-09-09T03:38:05+09:00
draft: false
pin: false
tags: ["zsh"]
---

{{< code >}}
typeset -Ug path
path+=(~/bin(N-/) ~/.local/bin(N-/))

typeset -Ug cdpath
cdpath+=(~ ~/git(N-/) ~/src(N-/))

if (( $+commands[tmux] && $+SSH_CONNECTION && ! $+TMUX )); then
    tmux has && exec tmux attach
    exec tmux new
fi
{{< /code >}}
