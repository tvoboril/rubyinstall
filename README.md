# RUBYINSTALL-MAC

Install Ruby on Mac

## Getting Started

Check Current Version of ruby and rails


* [Ruby](http://www.ruby-lang.org/en/downloads/)
* [Rails](http://rvm.io/)

## Prerequisites

Make sure XCode is installed

```
$ xcode-select --install
```

Make sure Homebrew is up to date
* [Homebrew](http://brew.sh/)

```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```


## Installing

#### Install GPG
You can use Homebrew to install gpg, an encryption program used to check the security of the RVM download. Installing gpg eliminates a warning message which will halt installation of RVM.
```
$ brew install gpg
```
After GPG is installed (or if it is already installed), install the security key for RVM:

```
$ command curl -sSL https://rvm.io/mpapis.asc | gpg --import -
```
If you skip the gpg steps you may not be able to install RVM.



#### Install RVM

```
$ \curl -L https://get.rvm.io | bash -s stable
```
##### Close and Reopen the Terminal
After installing RVM, you must close and reopen the Terminal window.

Alternatively, you can enter this command to refresh the terminal environment:
```
$ source ~/.rvm/scripts/rvm
```

#### Install Ruby
```
$ rvm install ruby-2.5.0
```
You may be asked to enter a password. When you enter the password, type carefully. You will not see the characters you enter.

Sometimes a precompiled version of Ruby is available. If not, it takes a long time (about five minutes) to install Ruby because the computer must compile the source code.

Verify that the newest version of Ruby is installed:
```
$ ruby -v
ruby 2.5.6.
```

Check what version of Ruby is being used as default

```
$ rvm list
   ruby-2.5.1 [ x86_64 ]
=* ruby-2.5.6 [ x86_64 ]

# => - current
# =* - current && default
#  * - default
```

If you need to change from the system or version

either change what is being used
```
$ rvm use 2.5.6
```

or change the default

```
$ rvm --default use 2.5.6
```


Check and update gem 
```
$ gem -v
2.6.10
```
Use gem update --system to upgrade the Ruby gem manager:
```
$ gem update --system
```

#### Install Bundler
```
$ gem install bundler
```
#### Install Nokogiri
```
$ gem install nokogiri
```
#### Install Rails
```
$ gem install rails
```

##### Check Version of Rails
```
$ rails -v
Rails 5.2.0
```
#### Set Auto Completion
Add to the bottom of your .bash_profile
```
[[ -r $rvm_path/scripts/completion ]] && . $rvm_path/scripts/completion
```
