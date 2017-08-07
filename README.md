INSTALLATIONS
=============

## THE NECESSITIES

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
     ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"     
   * brew install node, git, postgresql, redis
* Install Postgres
    * Go to: http://postgresapp.com
    Download the zip
    Unzip the file
    Place the elephant in the Applications folder on your harddrive
    Press CMD + Space
    Type: postgresql
    Click the elephant to run Postgres
    Make sure run on startup is clicked
* Generate SSH Key:
    * Open iTerm2:
    ssh-keygen -t rsa -C "your_email@example.com"
    Just press <Enter> to accept the default location and file name.
    Enter, and re-enter, a passphrase when prompted.

## RUBY
