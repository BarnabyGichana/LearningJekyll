# Installing Jekyll on a Debian System

1. Install Ruby

```bash
sudo apt update && sudo apt install ruby -y
```

2. Check for Jekyll requirements

```bash
ruby -v
gem -v
gcc -v
g++ -v
make -v
```

3. Install Jekyll dependencies

```bash
sudo apt-get install ruby-full build-essential zlib1g-dev -y
```

> __Note!__
>
> Avoid installing RubyGems packages (called gems) as the root user.
> Instead, set up a gem installation directory for your user account.
> The following commands will add environment variables to your
> ~/.bashrc file to configure the gem installation path:
>
> ```bash
> echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
> echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
> echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
> source ~/.bashrc
> ```

4. Install Jekyll and Bundler

```bash
gem install jekyll bundler
```

# Creating a New Site

To create a new site using Jekyll, run the following command where `<site-name>` is the name of your site:

```bash
jekyll new <site-name>
```

In this repository, I created a site named `test_site` with the following command

```bash
jekyll new test_site
```

## Serving a Site

To serve a Jekyll site locally, first navigate into the site's root directory (we shall proceed with the `test_site` example):

```bash
cd ./test_site
```

Then we run one of the two following commands depending on whether or not the site is being served for the first time:

```bash
# Serving a site for the first time
bundle exec jekyll serve
```

or

```bash
# Serving a previously bundled site
jekyll serve
```