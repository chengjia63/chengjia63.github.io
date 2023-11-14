# chengjia63.github.io

# MacOS Setup
```
brew update
brew install ruby
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
#brew install rbenv ruby-build
gem install bundle

cd /path/to/repo
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve
```
