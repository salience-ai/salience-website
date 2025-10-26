# Salience AI

Source files for the [salienceai.co](https://salienceai.co) website.

## Setup for Local Development (Ubuntu)

1. Install Ruby Version Manager:
   ```bash
   # install rvm step 1
   gpg --keyserver keyserver.ubuntu.com --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB

   # install rvm step 2
   curl -sSL https://get.rvm.io | bash -s stable
   ```

2. Set GHP compatible versions:
   ```bash
   # use rvm pkg to install openssl1.1
   rvm pkg install openssl

   # install the GH Pages compatible Ruby version
   rvm install 2.7.8 --with-openssl-dir=$HOME/.rvm/usr

   # set it as default
   rvm use 2.7.8 --default

   # update gems (for GH pages compatibility)
   gem install rubygems-update -v 3.3.22
   update_rubygems
   ```   

3. Verify installation:
   ```bash
   ruby -v
   gem -v
   ```

4. Install Bundler:
   ```bash
   gem install bundler
   ```

5. Install project dependencies:
   ```bash
   cd /path/to/project
   bundle install
   ```

## Running Locally

```bash
source ~/.rvm/scripts/rvm
bundle exec jekyll serve
```

Site will be available at http://localhost:4000


