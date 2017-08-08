INSTALLATIONS
=============

## THE NECESSITIES
==================

* [Iterm2](https://www.iterm2.com/)
* Slack: App Store
* Atom
* Sequel Pro (pancakes)
* Xcode: App Store
* Install X-Code Command Line Tools:
    * type: xcode-select --install
    follow instructions. (This is REQUIRED before the Homebrew install)
* Install Homebrew
   * open iTerm and paste the line below in:
   * ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"     
   * brew install node, git, postgresql, redis
* Install Postgres
    * Go to: http://postgresapp.com
    * Download the zip
    * Unzip the file
    * Place the elephant in the Applications folder
    * Open postgres
    * Make sure run on startup is clicked
* Generate SSH Key:
    * Open iTerm2:
    * ssh-keygen -t rsa -C "your_email@example.com"
    * Just press <Enter> to accept the default location and file name.
    * Enter, and re-enter, a passphrase when prompted.

## RUBY
=======

* Rbenv via iTerm2
  * brew install rbenv
  * echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
  * echo 'eval "$(rbenv init -)"' >> ~/.bash_profile

* Install Ruby-Build
  * brew install ruby-build

* Install Ruby
  * rbenv install 2.3.1
  * rbenv global 2.3.1

* Install Bundler Gem
  * gem install bundler
  * rbenv rehash

* Put postgres in path
  * export PATH=$PATH:/Applications/Postgres.app/Contents/Versions/<postgres version>/bin

## PHP/Laravel
==============
