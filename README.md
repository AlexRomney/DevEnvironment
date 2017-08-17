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

* Install Composer
  * php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
  * php -r "if (hash_file('SHA384', 'composer-setup.php') === '669656bab3166a7aff8a7506b8cb2d1c292f042046c5a994c43155c0be6190fa0355160742ab2e1c88d40d5be660b410') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
  * php composer-setup.php
  * php -r "unlink('composer-setup.php');"
  * mv composer.phar /usr/local/bin/composer
* Install Valet
  * brew update
  * brew install homebrew/php/php71
  * composer global require laravel/valet
  * In .bashrc:
  * export PATH="~/.composer/vendor/bin:$PATH"
  * export PATH=$PATH:~/.composer/vendor/bin
  * valet install
  * composer global require "laravel/installer"
  * valet park in Desktop path
* New Projects
  * Copy .env.example and paste in new .env file
  * Run php artisan key:generate
  * Run composer install
  * Run nmp install 
