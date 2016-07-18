Fast Recover Your macOS
===
From time to time, we might switch to a new machine or factory reset our OS for some reasons. You do not want to install every software from scratch since it is tedious and easy forgetting which app you need. Besides, things only goes worse if you are a developer because a lot of configurations needs to be done.

Last week I experienced this scenario that I installed the public Beta of the latest macOS where a lot of stuff just did not work. I have no choice but recovering. Fortunately, nearly all my important files are text-based so backup to the USB flash drive really fast(I do not use Time Machine since I have that little stuff to store). Finally, gave it a restore.

Then, I follow the following steps then a quite shining and working OS is welcome.

* Remapping ``CAPSLOCK`` to ``CTRL``, and vice-versa if you are a hard core Unix user
* Apply voice announcing the time every 15 min in Date&Time setting
* Apply three finger dragging window
* Remove any spotlight shortcuts then remap as <C-q>
* Install input method and map it with <Cmd-space>
* Go to Mac appstore to download what you have purchased and need
* Open native terminal then activate command-line tool with xcode
* Install ``homebrew`` on native terminal
* Go to Dropbox to copy the backup brew list file then run the restore script
* Open __iterm2__(restore from brew cask) then apply github backup dot files(__vim__, __zprezto__, __gitconfig__, etc.)
* Makes __iterm2__ and __zsh__ default workflow
* Configure __dropbox__ app and ``ln`` to the local directory
* Apply apps settings if settings file(or app preference screenshots) saved in Dropbox
* Install your favorite typeface if necessary
* Finally, configure the login items and you may put your name on your screen(-/-) if necessary

All done, when it comes to automation, do it without manually.

One more thing, I recommend you install Dropbox and soft linking(``ln``) other important directory, then all of the files are syncing amazing!

My backup and recover script is fairly easy as following,

```sh
#!/bin/bash
/path/to/backuped-pkgs | xargs brew install
cat /path/to/backuped-apps | xargs brew cask install
```

```sh
#!/bin/bash
brew ls > /path/to/backuped-pkgs
brew cask ls > /path/to/backuped-apps
```

We can automate a little further, every Friday 12am schedule ``crontab`` triggering the update/backup task,
```sh
# every Friday 12am, update and cleanup then backup
0 12 * * 5 /usr/local/bin/brew update && /usr/local/bin/brew upgrade && /usr/local/bin/brew cask update && /usr/local/bin/brew cleanup && /usr/local/bin/brew cask cleanup && /path/to/backup-script
# at same time update vim plugins
0 12 * * 5 /Applications/MacVim.app/Contents/MacOS/Vim +PlugUpdate +PlugClean +qall
# same with zprezto
0 12 * * 5 /usr/bin/git -C ~/.zprezto pull upstream master
```

that would be great without being aware of it. Note all the paths must be **absolute**.

#### EOF
```json
{
  "tags": ["automation"],
  "render_option": 0,
  "date": "2016-07-18T08:09:17+08:00",
  "weather": "hot",
  "summary": " When it comes to automation, do it without manually.",
  "location": "Shenzhen",
  "background": "recover.png"
}
```