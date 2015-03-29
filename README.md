loning Our Dotfiles to Another Machine

Ultimately, we’re going to come to a point where we want to use our customized dotfiles on another server or workstation. That is, after all, one of the primary benefits of using Git to manage our dotfiles. To do this, it’s as simple as running the following command from our home directory:

git clone git://github.com/<mygithubusername>/dotfiles.git

Once the repository has been cloned to our home directory, simply change to the dotfiles directory, make the makesymlinks.sh script executable, and run the script, like so:

cd ~/dotfiles
chmod +x makesymlinks.sh
./makesymlinks.sh

Warning: If you’re running Debian Linux, this will most likely install zsh on your system if it isn’t already installed. This is a feature I added to my script to automate things as much as possible. If for some reason you don’t want zsh to be installed on your computer (e.g. you’re on somebody else’s server), remove the install_zsh line from makesymlinks.sh. This will cause it to set up all of your dotfiles without attempting to install zsh.

That’s it! If the settings don’t take effect right away, we can just log out and log back in (this will re-source our dotfiles).
============
