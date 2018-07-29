# How to Create Terminal Alias to Show/Hide Hidden Files

**Update:** As of macOS Sierra, there is now an easier way to show and hide file names: <kbd>command</kbd> + <kbd>shift</kbd> + <kbd>.</kbd>.

This causes the rest of this article to now be obsolete. If you still want to know how to create terminal aliases this is still a good introduction.

**This is just a transcription of the instructions found online [here](https://ianlunn.co.uk/articles/quickly-showhide-hidden-files-mac-os-x-mavericks/), written by Ian Lunn.**

A Terminal alias is a name or shortcut for one or multiple commands. Using an easy to remember alias, we can turn the above four step process into just one.

An alias can be made temporarily (just for the use of one terminal session) or permanently. As we want this to be a shortcut used now and in the future, let’s make it permanent:

1. Open Terminal
2. Type: `sudo nano ~/.bash_profile`
3. Enter admin password
4. At the bottom of the file enter: `alias showFiles='defaults write com.apple.finder AppleShowAllFiles YES; killall Finder /System/Library/CoreServices/Finder.app'`
5. Below that, enter: `alias hideFiles='defaults write com.apple.finder AppleShowAllFiles NO; killall Finder /System/Library/CoreServices/Finder.app'`
6. Press <kbd>control</kbd> + <kbd>o</kbd> followed by <kbd>return</kbd> to save file
7. Press <kbd>control</kbd> + <kbd>x</kbd> to exit the file
8. In the terminal type `source ~/.bash_profile`

Now, whenever you type `showFiles` into Termial, your Finder will refresh and start showing all the hidden files; alternately `hideFiles` will refresh Finder and stop showing hidden files.