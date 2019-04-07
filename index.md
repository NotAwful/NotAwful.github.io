## Welcome!

Hey, I'm **notawful**. This is the home of my new *engineering journal*. Here you will find small incantations and troubleshooting steps for smaller tasks and problems. You can find my website at [notawful.org](https://notawful.org) and find me on twitter at [awfulyprideful](https://twitter.com/awfulyprideful).

*To myself: This page uses [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).*

## Engineering Journal

### Crouton (Chromebook chroot manager)

Shift back and forth between ChromeOS and graphical chroot
```
Crtl + Alt + Shift + [Forward|Backward]
```

### Vi

Changing modes in Vi

Command | Mode
---|---
`esc` | Exit Insert or Append mode and enter Command mode
`i` | enter Insert mode; insert text before cursor
`shift + i` | enter Insert mode; insert text at start of current line
`a` | enter Append mode; append text after cursor
`shift + a` | enter Append mode; append text to end of line

Actions in Command Mode

Command | Action
----|----
``d`` | Delete this line
``d10000`` | fuck this entire file (assuming file is under 10,000 lines)
``yy`` | cut (yank) this line
``pp`` | put buffer here (paste copied line)
``:read ~/secretkey`` | copy the contents of ~/secretkey to the current line
``^`` | place cursor at start of line (start from the top)
``$`` | place cursor at end of line (collect money at the end)
``/word`` | find next *word*; will also find *broadsword* or *password*
``?word`` | find previous *word*; will also find *broadsword* or *password*
``\<word\>`` | find next complete instance of *word*; does not finds swords or passwords
``?<word\>`` | find previous complete instance of *word*; does not finds swords or passwords
``:q`` | quit
``:q!`` | I SAID GOOD DAY, SIR. (Quit, but shouting and it bypasses save prompts)
``:w`` | write to file (save)
``:wq`` | write to file (save) then quit

### Git

Setting up git on a \*nix prompt. Set up username and email for commits, set to save credentials for repeated commits or cloning repositories over HTTPS.
```
sudo apt install git
git config --global user.name "Name"
git config --global user.email email@mail.example
git config --global core.editor vim
git config --global credential.helper cache
git config --global credential.helper 'cache --timeout==3600'
```
* You can list your current configuration with `git config --list`
* You can also use `git config --local` from within a repository to override `--global` settings for that particular repository.

## Ignore Below
*To myself: General format you should use here*
```markdown
### Topic (ex. ssh)
Cool thing you can do with ssh here
*code block goes here*

Second cool thing you can do with ssh here
*another codeblock goes here*
```
