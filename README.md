INSTALLATIONS
=============

## THE NECESSITIES
==================

* [Iterm2](https://www.iterm2.com/)
* Slack: App Store
* [Atom](https://atom.io/)
* [Sequel Pro (pancakes)](https://www.sequelpro.com/)
* Xcode: App Store
* Install X-Code Command Line Tools:
    * type: xcode-select --install
    follow instructions. (This is REQUIRED before the Homebrew install)
* Install Homebrew
   * open iTerm and paste the line below in:
   * ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"     
   * brew install node, git, postgresql, redis, mysql
   * run brew services start <programs>
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
    * Just press Enter to accept the default location and file name.
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

* [Install Composer](https://getcomposer.org/download/)
  * php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
  * php -r "if (hash_file('SHA384', 'composer-setup.php') === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
  * php composer-setup.php
  * php -r "unlink('composer-setup.php');"
  * mv composer.phar /usr/local/bin/composer
* [Install Valet](https://laravel.com/docs/5.6/valet)
  * brew update
  * brew install homebrew/core/php
  * composer global require laravel/valet
  * In .bash_profile:
  * export PATH="~/.composer/vendor/bin:$PATH"
  * export PATH=$PATH:~/.composer/vendor/bin
  * valet install
  * composer global require "laravel/installer"
  * valet park in Desktop path
  * valet domain <name you want>
* New Projects
  * Create .env file
  * Connect to database
  * Run php artisan key:generate
  * Run composer install
  * Run nmp install
  * Run npm run dev
  * Run php artisan migrate
