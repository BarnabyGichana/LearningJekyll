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