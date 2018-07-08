# rbenv

*rbenv* isa a ruby environment

https://github.com/rbenv/rbenv
https://gist.github.com/stonehippo/cc0f3098516fb52390f1

```sh
# install the tools
brew install rbenv ruby-build
# make it available on every start
echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
# make it available in this terminal
source ~/.bash_profile
# list all available versions
rbenv install -l
# install ruby v2.5.1
rbenv install 2.5.1
# make ruby v2.5.1 default and global
rbenv global 2.5.1
# install bundler
# https://bundler.io/
gem install bundler
# install susy
gem install susy
# install breakpoint
gem install breakpoint
# install compass
gem install compass
# install font-awesome-sass v4.3.2.1
gem install font-awesome-sass --version 4.3.2.1
# Check the location where gems are being installed
gem env home
# Lists all Ruby versions with the given command installed
rbenv whence compass
rbenv whence font-awesome-sass --version 4.3.2.1
```