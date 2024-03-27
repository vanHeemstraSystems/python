# 300 - Building Our Application

**Temporary solution**
Just enter this in your git shell on windows - > ```alias python='winpty python.exe'```, that is all and you are going to have alias to the python executable. This alias will be valid for the duration of the shell session.

[winpty](https://github.com/rprichard/winpty) is a Windows software package providing an interface similar to a Unix pty-master for communicating with Windows console programs.

**Permanent solution**
Add the command to your ```.bashrc``` in the users home directory. You can use the CLI or a text editor:

**Using CLI**
This can be accomplished from git bash like so:

```
echo "alias python='winpty python.exe'" >> ~/.bashrc
```

which will create ```.bashrc``` in the current users home directory if the file doesn't exist or append the alias to the end of ```.bashrc``` if it does.

**Using a text editor**
Alternatively, you could first create a ```.bashrc```. Depending on your file manager, this may be easier to accomplish in git bash like so:

```
cd ~
touch .bashrc
```

At which point you can open ```.bashrc``` in your prefered text editor and add it there.

To apply the change, either use the command source ```.bashrc``` or restart the shell.

**Update**
Newer versions of Git no longer use ```.bashrc``` but instead use ```.bash_profile```. Conda also uses this profile when initializing, so be sure not to overwrite or delete the initialization block. See more here: [Git for Windows doesn't execute my ```.bashrc``` file](https://stackoverflow.com/questions/32186840/git-for-windows-doesnt-execute-my-bashrc-file/32189255#32189255).
