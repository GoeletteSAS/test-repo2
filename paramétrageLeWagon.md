Last login: Mon Oct  7 10:22:56 on ttys004
baudouindebayser@MacBook-Pro-de-Baudouin ~ % sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
Cloning Oh My Zsh...
remote: Enumerating objects: 1407, done.
remote: Counting objects: 100% (1407/1407), done.
remote: Compressing objects: 100% (1347/1347), done.
remote: Total 1407 (delta 36), reused 1128 (delta 32), pack-reused 0 (from 0)
Réception d'objets: 100% (1407/1407), 3.26 Mio | 8.45 Mio/s, fait.
Résolution des deltas: 100% (36/36), fait.
Depuis https://github.com/ohmyzsh/ohmyzsh
 * [nouvelle branche] master     -> origin/master
la branche 'master' est paramétrée pour suivre 'origin/master'.
Déjà sur 'master'
/Users/baudouindebayser

Looking for an existing zsh config...
Using the Oh My Zsh template file and adding it to /Users/baudouindebayser/.zshrc.

         __                                     __   
  ____  / /_     ____ ___  __  __   ____  _____/ /_  
 / __ \/ __ \   / __ `__ \/ / / /  /_  / / ___/ __ \ 
/ /_/ / / / /  / / / / / / /_/ /    / /_(__  ) / / / 
\____/_/ /_/  /_/ /_/ /_/\__, /    /___/____/_/ /_/  
                        /____/                       ....is now installed!


Before you scream Oh My Zsh! look over the `.zshrc` file to select plugins, themes, and options.

• Follow us on X: https://x.com/ohmyzsh
• Join our Discord community: https://discord.gg/ohmyzsh
• Get stickers, t-shirts, coffee mugs and more: https://shop.planetargon.com/collections/oh-my-zsh

➜  ~ gh auth login -s 'user:email' -w
? What is your preferred protocol for Git operations on this host? SSH
? Upload your SSH public key to your GitHub account? /Users/baudouindebayser/.ssh/id_rsa.pub
? Title for your SSH key: public-key-github

! First copy your one-time code: 29F3-2269
Press Enter to open github.com in your browser... 
✓ Authentication complete.
- gh config set -h github.com git_protocol ssh
✓ Configured git protocol
✓ SSH key already existed on your GitHub account: /Users/baudouindebayser/.ssh/id_rsa.pub
✓ Logged in as GoeletteSAS
➜  ~ 
➜  ~ gh auth status
github.com
  ✓ Logged in to github.com account GoeletteSAS (keyring)
  - Active account: true
  - Git operations protocol: ssh
  - Token: gho_************************************
  - Token scopes: 'admin:public_key', 'gist', 'read:org', 'repo', 'user:email'
➜  ~ export GITHUB_USERNAME=`gh api user | jq -r '.login'`
echo $GITHUB_USERNAME
GoeletteSAS
➜  ~ mkdir -p ~/code/$GITHUB_USERNAME && cd $_
gh repo fork lewagon/dotfiles --clone
✓ Created fork GoeletteSAS/dotfiles
Clonage dans 'dotfiles'...
remote: Enumerating objects: 957, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 957 (delta 3), reused 3 (delta 1), pack-reused 947 (from 1)
Réception d'objets: 100% (957/957), 216.10 Kio | 740.00 Kio/s, fait.
Résolution des deltas: 100% (440/440), fait.
Depuis github.com:lewagon/dotfiles
 * [nouvelle branche] master     -> upstream/master
✓ Cloned fork
! Repository lewagon/dotfiles set as the default repository. To learn more about the default repository, run: gh repo set-default --help
➜  GoeletteSAS cd ~/code/$GITHUB_USERNAME/dotfiles
zsh install.sh
-----> Symlinking your new /Users/baudouindebayser/.aliases
-----> Symlinking your new /Users/baudouindebayser/.gitconfig
-----> Symlinking your new /Users/baudouindebayser/.irbrc
-----> Symlinking your new /Users/baudouindebayser/.pryrc
-----> Symlinking your new /Users/baudouindebayser/.rspec
-----> Moved your old /Users/baudouindebayser/.zprofile config file to /Users/baudouindebayser/.zprofile.backup
-----> Symlinking your new /Users/baudouindebayser/.zprofile
-----> Moved your old /Users/baudouindebayser/.zshrc config file to /Users/baudouindebayser/.zshrc.backup
-----> Symlinking your new /Users/baudouindebayser/.zshrc
-----> Installing zsh plugin 'zsh-syntax-highlighting'...
Clonage dans 'zsh-autosuggestions'...
remote: Enumerating objects: 2564, done.
remote: Counting objects: 100% (179/179), done.
remote: Compressing objects: 100% (93/93), done.
remote: Total 2564 (delta 109), reused 132 (delta 83), pack-reused 2385 (from 1)
Réception d'objets: 100% (2564/2564), 588.40 Kio | 7.00 Mio/s, fait.
Résolution des deltas: 100% (1640/1640), fait.
Clonage dans 'zsh-syntax-highlighting'...
remote: Enumerating objects: 7107, done.
remote: Counting objects: 100% (193/193), done.
remote: Compressing objects: 100% (111/111), done.
remote: Total 7107 (delta 102), reused 117 (delta 70), pack-reused 6914 (from 1)
Réception d'objets: 100% (7107/7107), 1.53 Mio | 10.25 Mio/s, fait.
Résolution des deltas: 100% (4778/4778), fait.
-----> Moved your old /Users/baudouindebayser/Library/Application Support/Code/User/settings.json config file to /Users/baudouindebayser/Library/Application Support/Code/User/settings.json.backup
-----> Symlinking your new /Users/baudouindebayser/Library/Application Support/Code/User/settings.json
-----> Symlinking your new /Users/baudouindebayser/Library/Application Support/Code/User/keybindings.json
-----> Moved your old /Users/baudouindebayser/.ssh/config config file to /Users/baudouindebayser/.ssh/config.backup
-----> Symlinking your new /Users/baudouindebayser/.ssh/config
/Users/baudouindebayser/.ssh/id_ed25519: No such file or directory
➜  dotfiles git:(master) gh api user/emails | jq -r '.[].email'
baud2bsr@hotmail.fr
➜  dotfiles git:(master) cd ~/code/$GITHUB_USERNAME/dotfiles && zsh git_setup.sh
Type in your first and last name (no accent or special characters - e.g. 'ç'): 
Baudouin deBayser             
Type in your email address (the one used for your GitHub account): 
baud2bsr@hotmail.fr
[master b400a6b] My identity for @lewagon in the gitconfig
 1 file changed, 3 insertions(+)
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 371 bytes | 371.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:GoeletteSAS/dotfiles.git
   54a90f9..b400a6b  master -> master
error: remote upstream already exists.
👌 Awesome, all set.
➜  dotfiles git:(master) exec zsh
➜  dotfiles git:(master) rvm implode && sudo rm -rf ~/.rvm
# Si tu vois apparaître « zsh: command not found: rvm », continue. Cela signifie que `rvm` n’est pas installé
# sur ton ordinateur, et c’est qu’on veut !

sudo rm -rf $HOME/.rbenv /usr/local/rbenv /opt/rbenv /usr/local/opt/rbenv
zsh: command not found: rvm
Password:
➜  dotfiles git:(master) brew uninstall --force rbenv ruby-build
exec zsh
➜  dotfiles git:(master) brew install rbenv
==> Downloading https://formulae.brew.sh/api/formula.jws.json
############################################################################################################################################################### 100.0%
==> Downloading https://formulae.brew.sh/api/cask.jws.json
############################################################################################################################################################### 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/rbenv/manifests/1.3.0-1
############################################################################################################################################################### 100.0%
==> Fetching dependencies for rbenv: autoconf, libyaml, pkg-config and ruby-build
==> Downloading https://ghcr.io/v2/homebrew/core/autoconf/manifests/2.72-1
############################################################################################################################################################### 100.0%
==> Fetching autoconf
==> Downloading https://ghcr.io/v2/homebrew/core/autoconf/blobs/sha256:c3674a4dfa3794e022b1adbcd9c954c91192d38822080c7162d073d6609b903a
############################################################################################################################################################### 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/libyaml/manifests/0.2.5
############################################################################################################################################################### 100.0%
==> Fetching libyaml
==> Downloading https://ghcr.io/v2/homebrew/core/libyaml/blobs/sha256:98c0cf81bcdf7577d5fdc8cc18732970b9ae7e0e7423a733f88f0f566ba483ad
############################################################################################################################################################### 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/pkg-config/manifests/0.29.2_3
############################################################################################################################################################### 100.0%
==> Fetching pkg-config
==> Downloading https://ghcr.io/v2/homebrew/core/pkg-config/blobs/sha256:7b59abc0b5381065b1eab174217307af9324e0d02edf903171b29250ae58aeaf
############################################################################################################################################################### 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/ruby-build/manifests/20240917
############################################################################################################################################################### 100.0%
==> Fetching ruby-build
==> Downloading https://ghcr.io/v2/homebrew/core/ruby-build/blobs/sha256:a69d04a25971f1f19d4cc2893adafc60e472dbb2fca2799ebf6de25d2e5e1658
############################################################################################################################################################### 100.0%
==> Fetching rbenv
==> Downloading https://ghcr.io/v2/homebrew/core/rbenv/blobs/sha256:8c1ae8d76748e0140a458cd4c83b2f6ed83da17777940f7878ce5348ede8aeff
############################################################################################################################################################### 100.0%
==> Installing dependencies for rbenv: autoconf, libyaml, pkg-config and ruby-build
==> Installing rbenv dependency: autoconf
==> Downloading https://ghcr.io/v2/homebrew/core/autoconf/manifests/2.72-1
Already downloaded: /Users/baudouindebayser/Library/Caches/Homebrew/downloads/1b54b8d75974d006eb6be1db91a6ec040791ac751f25271fcd5a1d78cb361afd--autoconf-2.72-1.bottle_manifest.json
==> Pouring autoconf--2.72.arm64_sonoma.bottle.1.tar.gz
🍺  /opt/homebrew/Cellar/autoconf/2.72: 72 files, 3.6MB
==> Installing rbenv dependency: libyaml
==> Downloading https://ghcr.io/v2/homebrew/core/libyaml/manifests/0.2.5
Already downloaded: /Users/baudouindebayser/Library/Caches/Homebrew/downloads/5f6b0af1730aa1bc02f8021c90ed7ffe988eeba95eec83e6c828f77332ba6406--libyaml-0.2.5.bottle_manifest.json
==> Pouring libyaml--0.2.5.arm64_sonoma.bottle.tar.gz
🍺  /opt/homebrew/Cellar/libyaml/0.2.5: 11 files, 354.9KB
==> Installing rbenv dependency: pkg-config
==> Downloading https://ghcr.io/v2/homebrew/core/pkg-config/manifests/0.29.2_3
Already downloaded: /Users/baudouindebayser/Library/Caches/Homebrew/downloads/ac691fc7ab8ecffba32a837e7197101d271474a3a84cfddcc30c9fd6763ab3c6--pkg-config-0.29.2_3.bottle_manifest.json
==> Pouring pkg-config--0.29.2_3.arm64_sonoma.bottle.tar.gz
🍺  /opt/homebrew/Cellar/pkg-config/0.29.2_3: 12 files, 679.3KB
==> Installing rbenv dependency: ruby-build
==> Downloading https://ghcr.io/v2/homebrew/core/ruby-build/manifests/20240917
Already downloaded: /Users/baudouindebayser/Library/Caches/Homebrew/downloads/7447723f460499987a50d5eaea45085cbb99517a5fa41a36eec4e30e96a7cbfb--ruby-build-20240917.bottle_manifest.json
==> Pouring ruby-build--20240917.all.bottle.tar.gz
🍺  /opt/homebrew/Cellar/ruby-build/20240917: 625 files, 342.7KB
==> Installing rbenv
==> Pouring rbenv--1.3.0.all.bottle.1.tar.gz
==> Caveats
zsh completions have been installed to:
  /opt/homebrew/share/zsh/site-functions
==> Summary
🍺  /opt/homebrew/Cellar/rbenv/1.3.0: 36 files, 73.6KB
==> Running `brew cleanup rbenv`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
==> Caveats
==> rbenv
zsh completions have been installed to:
  /opt/homebrew/share/zsh/site-functions
➜  dotfiles git:(master) rbenv install 3.3.5
ruby-build: using openssl@3 from homebrew
==> Downloading ruby-3.3.5.tar.gz...
-> curl -q -fL -o ruby-3.3.5.tar.gz https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.gz
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 21.1M  100 21.1M    0     0  11.8M      0  0:00:01  0:00:01 --:--:-- 11.8M
==> Installing ruby-3.3.5...
ruby-build: using libyaml from homebrew
-> ./configure "--prefix=$HOME/.rbenv/versions/3.3.5" --with-openssl-dir=/opt/homebrew/opt/openssl@3 --enable-shared --with-libyaml-dir=/opt/homebrew/opt/libyaml --with-ext=openssl,psych,+
-> make -j 8
-> make install
==> Installed ruby-3.3.5 to /Users/baudouindebayser/.rbenv/versions/3.3.5

NOTE: to activate this Ruby version as the new default, run: rbenv global 3.3.5
➜  dotfiles git:(master) rbenv global 3.3.5
➜  dotfiles git:(master) exec zsh
➜  dotfiles git:(master) ruby -v
ruby 3.3.5 (2024-09-03 revision ef084cc8f4) [arm64-darwin23]
➜  dotfiles git:(master) gem update bundler
Updating installed gems
Updating bundler
Fetching bundler-2.5.21.gem
Successfully installed bundler-2.5.21
Parsing documentation for bundler-2.5.21
Installing ri documentation for bundler-2.5.21
Done installing documentation for bundler after 2 seconds
Parsing documentation for bundler-2.5.21
Done installing documentation for bundler after 0 seconds
Gems updated: bundler
➜  dotfiles git:(master) gem install colored faker http pry-byebug rake rails:7.1.3.4 rest-client rspec rubocop-performance sqlite3:1.7.3 activerecord:7.1.3.2
Fetching colored-1.2.gem
Successfully installed colored-1.2
Parsing documentation for colored-1.2
Installing ri documentation for colored-1.2
Done installing documentation for colored after 0 seconds
Fetching faker-3.4.2.gem
Fetching concurrent-ruby-1.3.4.gem
Fetching i18n-1.14.6.gem
Successfully installed concurrent-ruby-1.3.4
PSA: I18n will be dropping support for Ruby < 3.2 in the next major release (April 2025), due to Ruby's end of life for 3.1 and below (https://endoflife.date/ruby). Please upgrade to Ruby 3.2 or newer by April 2025 to continue using future versions of this gem.
Successfully installed i18n-1.14.6
Successfully installed faker-3.4.2
Parsing documentation for concurrent-ruby-1.3.4
Installing ri documentation for concurrent-ruby-1.3.4
Parsing documentation for i18n-1.14.6
Installing ri documentation for i18n-1.14.6
Parsing documentation for faker-3.4.2
Installing ri documentation for faker-3.4.2
Done installing documentation for concurrent-ruby, i18n, faker after 1 seconds
Fetching ffi-1.17.0-arm64-darwin.gem
Fetching ffi-compiler-1.3.2.gem
Fetching llhttp-ffi-0.5.0.gem
Fetching http-form_data-2.3.0.gem
Fetching domain_name-0.6.20240107.gem
Fetching http-cookie-1.0.7.gem
Fetching public_suffix-6.0.1.gem
Fetching addressable-2.8.7.gem
Fetching http-5.2.0.gem
Successfully installed ffi-1.17.0-arm64-darwin
Successfully installed ffi-compiler-1.3.2
Building native extensions. This could take a while...
Successfully installed llhttp-ffi-0.5.0
Successfully installed http-form_data-2.3.0
Successfully installed domain_name-0.6.20240107
Successfully installed http-cookie-1.0.7
Successfully installed public_suffix-6.0.1
Successfully installed addressable-2.8.7
Successfully installed http-5.2.0
Parsing documentation for ffi-1.17.0-arm64-darwin
Installing ri documentation for ffi-1.17.0-arm64-darwin
Parsing documentation for ffi-compiler-1.3.2
Installing ri documentation for ffi-compiler-1.3.2
Parsing documentation for llhttp-ffi-0.5.0
Installing ri documentation for llhttp-ffi-0.5.0
Parsing documentation for http-form_data-2.3.0
Installing ri documentation for http-form_data-2.3.0
Parsing documentation for domain_name-0.6.20240107
Installing ri documentation for domain_name-0.6.20240107
Parsing documentation for http-cookie-1.0.7
Installing ri documentation for http-cookie-1.0.7
Parsing documentation for public_suffix-6.0.1
Installing ri documentation for public_suffix-6.0.1
Parsing documentation for addressable-2.8.7
Installing ri documentation for addressable-2.8.7
Parsing documentation for http-5.2.0
Installing ri documentation for http-5.2.0
Done installing documentation for ffi, ffi-compiler, llhttp-ffi, http-form_data, domain_name, http-cookie, public_suffix, addressable, http after 1 seconds
Fetching pry-byebug-3.10.1.gem
Fetching method_source-1.1.0.gem
Fetching coderay-1.1.3.gem
Fetching pry-0.14.2.gem
Fetching byebug-11.1.3.gem
Successfully installed method_source-1.1.0
Successfully installed coderay-1.1.3
Successfully installed pry-0.14.2
Building native extensions. This could take a while...
Successfully installed byebug-11.1.3
Successfully installed pry-byebug-3.10.1
Parsing documentation for method_source-1.1.0
Installing ri documentation for method_source-1.1.0
invalid options: -SNw2
(invalid options are ignored)
Parsing documentation for coderay-1.1.3
Installing ri documentation for coderay-1.1.3
Parsing documentation for pry-0.14.2
Installing ri documentation for pry-0.14.2
Parsing documentation for byebug-11.1.3
Installing ri documentation for byebug-11.1.3
Parsing documentation for pry-byebug-3.10.1
Installing ri documentation for pry-byebug-3.10.1
Done installing documentation for method_source, coderay, pry, byebug, pry-byebug after 3 seconds
Fetching rake-13.2.1.gem
Successfully installed rake-13.2.1
Parsing documentation for rake-13.2.1
Installing ri documentation for rake-13.2.1
Done installing documentation for rake after 0 seconds
Fetching zeitwerk-2.6.18.gem
Fetching thor-1.3.2.gem
Fetching webrick-1.8.2.gem
Fetching rack-3.1.7.gem
Fetching rackup-2.1.0.gem
Fetching tzinfo-2.0.6.gem
Fetching connection_pool-2.4.1.gem
Fetching activesupport-7.1.3.4.gem
Fetching nokogiri-1.16.7-arm64-darwin.gem
Fetching crass-1.0.6.gem
Fetching loofah-2.22.0.gem
Fetching rails-html-sanitizer-1.6.0.gem
Fetching rails-dom-testing-2.2.0.gem
Fetching rack-test-2.1.0.gem
Fetching rack-session-2.0.0.gem
Fetching erubi-1.13.0.gem
Fetching builder-3.3.0.gem
Fetching actionview-7.1.3.4.gem
Fetching actionpack-7.1.3.4.gem
Fetching railties-7.1.3.4.gem
Fetching marcel-1.0.4.gem
Fetching activemodel-7.1.3.4.gem
Fetching activerecord-7.1.3.4.gem
Fetching globalid-1.2.1.gem
Fetching activejob-7.1.3.4.gem
Fetching activestorage-7.1.3.4.gem
Fetching actiontext-7.1.3.4.gem
Fetching mini_mime-1.1.5.gem
Fetching mail-2.8.1.gem
Fetching actionmailer-7.1.3.4.gem
Fetching actionmailbox-7.1.3.4.gem
Fetching websocket-extensions-0.1.5.gem
Fetching rails-7.1.3.4.gem
Fetching websocket-driver-0.7.6.gem
Fetching nio4r-2.7.3.gem
Fetching actioncable-7.1.3.4.gem
Successfully installed zeitwerk-2.6.18
Successfully installed thor-1.3.2
Successfully installed webrick-1.8.2
Successfully installed rack-3.1.7
Successfully installed rackup-2.1.0
Successfully installed tzinfo-2.0.6
Successfully installed connection_pool-2.4.1
Successfully installed activesupport-7.1.3.4
Successfully installed nokogiri-1.16.7-arm64-darwin
Successfully installed crass-1.0.6
Successfully installed loofah-2.22.0
Successfully installed rails-html-sanitizer-1.6.0
Successfully installed rails-dom-testing-2.2.0
Successfully installed rack-test-2.1.0
Successfully installed rack-session-2.0.0
Successfully installed erubi-1.13.0
Successfully installed builder-3.3.0
Successfully installed actionview-7.1.3.4
Successfully installed actionpack-7.1.3.4
Successfully installed railties-7.1.3.4
Successfully installed marcel-1.0.4
Successfully installed activemodel-7.1.3.4
Successfully installed activerecord-7.1.3.4
Successfully installed globalid-1.2.1
Successfully installed activejob-7.1.3.4
Successfully installed activestorage-7.1.3.4
Successfully installed actiontext-7.1.3.4
Successfully installed mini_mime-1.1.5
Successfully installed mail-2.8.1
Successfully installed actionmailer-7.1.3.4
Successfully installed actionmailbox-7.1.3.4
Successfully installed websocket-extensions-0.1.5
Building native extensions. This could take a while...
Successfully installed websocket-driver-0.7.6
Building native extensions. This could take a while...
Successfully installed nio4r-2.7.3
Successfully installed actioncable-7.1.3.4
Successfully installed rails-7.1.3.4
Parsing documentation for zeitwerk-2.6.18
Installing ri documentation for zeitwerk-2.6.18
Parsing documentation for thor-1.3.2
Installing ri documentation for thor-1.3.2
Parsing documentation for webrick-1.8.2
Installing ri documentation for webrick-1.8.2
Parsing documentation for rack-3.1.7
Installing ri documentation for rack-3.1.7
Parsing documentation for rackup-2.1.0
Installing ri documentation for rackup-2.1.0
Parsing documentation for tzinfo-2.0.6
Installing ri documentation for tzinfo-2.0.6
Parsing documentation for connection_pool-2.4.1
Installing ri documentation for connection_pool-2.4.1
Parsing documentation for activesupport-7.1.3.4
Couldn't find file to include 'activesupport/README.rdoc' from lib/active_support.rb
Installing ri documentation for activesupport-7.1.3.4
Parsing documentation for nokogiri-1.16.7-arm64-darwin
Installing ri documentation for nokogiri-1.16.7-arm64-darwin
Parsing documentation for crass-1.0.6
Installing ri documentation for crass-1.0.6
Parsing documentation for loofah-2.22.0
Installing ri documentation for loofah-2.22.0
Parsing documentation for rails-html-sanitizer-1.6.0
Installing ri documentation for rails-html-sanitizer-1.6.0
Parsing documentation for rails-dom-testing-2.2.0
Installing ri documentation for rails-dom-testing-2.2.0
Parsing documentation for rack-test-2.1.0
Installing ri documentation for rack-test-2.1.0
Parsing documentation for rack-session-2.0.0
Installing ri documentation for rack-session-2.0.0
Parsing documentation for erubi-1.13.0
Installing ri documentation for erubi-1.13.0
Parsing documentation for builder-3.3.0
Installing ri documentation for builder-3.3.0
Parsing documentation for actionview-7.1.3.4
Couldn't find file to include 'actionview/README.rdoc' from lib/action_view.rb
Installing ri documentation for actionview-7.1.3.4
Parsing documentation for actionpack-7.1.3.4
Installing ri documentation for actionpack-7.1.3.4
Parsing documentation for railties-7.1.3.4
Installing ri documentation for railties-7.1.3.4
Parsing documentation for marcel-1.0.4
Installing ri documentation for marcel-1.0.4
Parsing documentation for activemodel-7.1.3.4
Couldn't find file to include 'activemodel/README.rdoc' from lib/active_model.rb
Installing ri documentation for activemodel-7.1.3.4
Parsing documentation for activerecord-7.1.3.4
Couldn't find file to include 'activerecord/README.rdoc' from lib/active_record.rb
Installing ri documentation for activerecord-7.1.3.4
Parsing documentation for globalid-1.2.1
Installing ri documentation for globalid-1.2.1
Parsing documentation for activejob-7.1.3.4
Couldn't find file to include 'activejob/README.md' from lib/active_job.rb
Installing ri documentation for activejob-7.1.3.4
Parsing documentation for activestorage-7.1.3.4
Couldn't find file to include 'activestorage/README.md' from lib/active_storage.rb
Installing ri documentation for activestorage-7.1.3.4
Parsing documentation for actiontext-7.1.3.4
Couldn't find file to include 'actiontext/README.md' from lib/action_text.rb
Installing ri documentation for actiontext-7.1.3.4
Parsing documentation for mini_mime-1.1.5
Installing ri documentation for mini_mime-1.1.5
Parsing documentation for mail-2.8.1
Installing ri documentation for mail-2.8.1
Parsing documentation for actionmailer-7.1.3.4
Couldn't find file to include 'actionmailer/README.rdoc' from lib/action_mailer.rb
Installing ri documentation for actionmailer-7.1.3.4
Parsing documentation for actionmailbox-7.1.3.4
Couldn't find file to include 'actionmailbox/README.md' from lib/action_mailbox.rb
Installing ri documentation for actionmailbox-7.1.3.4
Parsing documentation for websocket-extensions-0.1.5
Installing ri documentation for websocket-extensions-0.1.5
Parsing documentation for websocket-driver-0.7.6
Installing ri documentation for websocket-driver-0.7.6
Parsing documentation for nio4r-2.7.3
Installing ri documentation for nio4r-2.7.3
Parsing documentation for actioncable-7.1.3.4
Couldn't find file to include 'actioncable/README.md' from lib/action_cable.rb
Installing ri documentation for actioncable-7.1.3.4
Parsing documentation for rails-7.1.3.4
Installing ri documentation for rails-7.1.3.4
Done installing documentation for zeitwerk, thor, webrick, rack, rackup, tzinfo, connection_pool, activesupport, nokogiri, crass, loofah, rails-html-sanitizer, rails-dom-testing, rack-test, rack-session, erubi, builder, actionview, actionpack, railties, marcel, activemodel, activerecord, globalid, activejob, activestorage, actiontext, mini_mime, mail, actionmailer, actionmailbox, websocket-extensions, websocket-driver, nio4r, actioncable, rails after 12 seconds
Fetching rest-client-2.1.0.gem
Fetching netrc-0.11.0.gem
Fetching mime-types-data-3.2024.1001.gem
Fetching mime-types-3.6.0.gem
Fetching http-accept-1.7.0.gem
Successfully installed netrc-0.11.0
Successfully installed mime-types-data-3.2024.1001
Successfully installed mime-types-3.6.0
Successfully installed http-accept-1.7.0
Successfully installed rest-client-2.1.0
Parsing documentation for netrc-0.11.0
Installing ri documentation for netrc-0.11.0
Parsing documentation for mime-types-data-3.2024.1001
Installing ri documentation for mime-types-data-3.2024.1001
Parsing documentation for mime-types-3.6.0
Installing ri documentation for mime-types-3.6.0
Parsing documentation for http-accept-1.7.0
unknown encoding name "header" for lib/http/accept.rb, skipping
Installing ri documentation for http-accept-1.7.0
Parsing documentation for rest-client-2.1.0
Installing ri documentation for rest-client-2.1.0
Done installing documentation for netrc, mime-types-data, mime-types, http-accept, rest-client after 1 seconds
Fetching rspec-3.13.0.gem
Fetching rspec-support-3.13.1.gem
Fetching diff-lcs-1.5.1.gem
Fetching rspec-mocks-3.13.2.gem
Fetching rspec-expectations-3.13.3.gem
Fetching rspec-core-3.13.1.gem
Successfully installed rspec-support-3.13.1
Successfully installed diff-lcs-1.5.1
Successfully installed rspec-mocks-3.13.2
Successfully installed rspec-expectations-3.13.3
Successfully installed rspec-core-3.13.1
Successfully installed rspec-3.13.0
Parsing documentation for rspec-support-3.13.1
Installing ri documentation for rspec-support-3.13.1
Parsing documentation for diff-lcs-1.5.1
Installing ri documentation for diff-lcs-1.5.1
Parsing documentation for rspec-mocks-3.13.2
Installing ri documentation for rspec-mocks-3.13.2
Parsing documentation for rspec-expectations-3.13.3
Installing ri documentation for rspec-expectations-3.13.3
Parsing documentation for rspec-core-3.13.1
Installing ri documentation for rspec-core-3.13.1
Parsing documentation for rspec-3.13.0
Installing ri documentation for rspec-3.13.0
Done installing documentation for rspec-support, diff-lcs, rspec-mocks, rspec-expectations, rspec-core, rspec after 1 seconds
Fetching ast-2.4.2.gem
Fetching parser-3.3.5.0.gem
Fetching rubocop-ast-1.32.3.gem
Fetching unicode-display_width-2.6.0.gem
Fetching ruby-progressbar-1.13.0.gem
Fetching regexp_parser-2.9.2.gem
Fetching rainbow-3.1.1.gem
Fetching parallel-1.26.3.gem
Fetching rubocop-performance-1.22.1.gem
Fetching language_server-protocol-3.17.0.3.gem
Fetching rubocop-1.66.1.gem
Successfully installed ast-2.4.2
Successfully installed parser-3.3.5.0
Successfully installed rubocop-ast-1.32.3
Successfully installed unicode-display_width-2.6.0
Successfully installed ruby-progressbar-1.13.0
Successfully installed regexp_parser-2.9.2
Successfully installed rainbow-3.1.1
Successfully installed parallel-1.26.3
Successfully installed language_server-protocol-3.17.0.3
Successfully installed rubocop-1.66.1
Successfully installed rubocop-performance-1.22.1
Parsing documentation for ast-2.4.2
Installing ri documentation for ast-2.4.2
Parsing documentation for parser-3.3.5.0
Installing ri documentation for parser-3.3.5.0
Parsing documentation for rubocop-ast-1.32.3
Installing ri documentation for rubocop-ast-1.32.3
Parsing documentation for unicode-display_width-2.6.0
Installing ri documentation for unicode-display_width-2.6.0
Parsing documentation for ruby-progressbar-1.13.0
Installing ri documentation for ruby-progressbar-1.13.0
Parsing documentation for regexp_parser-2.9.2
Installing ri documentation for regexp_parser-2.9.2
Parsing documentation for rainbow-3.1.1
Installing ri documentation for rainbow-3.1.1
Parsing documentation for parallel-1.26.3
Installing ri documentation for parallel-1.26.3
Parsing documentation for language_server-protocol-3.17.0.3
Installing ri documentation for language_server-protocol-3.17.0.3
Parsing documentation for rubocop-1.66.1
Installing ri documentation for rubocop-1.66.1
Parsing documentation for rubocop-performance-1.22.1
Installing ri documentation for rubocop-performance-1.22.1
Done installing documentation for ast, parser, rubocop-ast, unicode-display_width, ruby-progressbar, regexp_parser, rainbow, parallel, language_server-protocol, rubocop, rubocop-performance after 20 seconds
Fetching sqlite3-1.7.3-arm64-darwin.gem
Successfully installed sqlite3-1.7.3-arm64-darwin
Parsing documentation for sqlite3-1.7.3-arm64-darwin
Installing ri documentation for sqlite3-1.7.3-arm64-darwin
Done installing documentation for sqlite3 after 0 seconds
Fetching activerecord-7.1.3.2.gem
Fetching activesupport-7.1.3.2.gem
Fetching activemodel-7.1.3.2.gem
Successfully installed activesupport-7.1.3.2
Successfully installed activemodel-7.1.3.2
Successfully installed activerecord-7.1.3.2
Parsing documentation for activesupport-7.1.3.2
Couldn't find file to include 'activesupport/README.rdoc' from lib/active_support.rb
Installing ri documentation for activesupport-7.1.3.2
Parsing documentation for activemodel-7.1.3.2
Couldn't find file to include 'activemodel/README.rdoc' from lib/active_model.rb
Installing ri documentation for activemodel-7.1.3.2
Parsing documentation for activerecord-7.1.3.2
Couldn't find file to include 'activerecord/README.rdoc' from lib/active_record.rb
Installing ri documentation for activerecord-7.1.3.2
Done installing documentation for activesupport, activemodel, activerecord after 2 seconds
81 gems installed

A new release of RubyGems is available: 3.5.16 → 3.5.21!
Run `gem update --system 3.5.21` to update your installation.

➜  dotfiles git:(master) curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | zsh
exec zsh
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 15037  100 15037    0     0    97k      0 --:--:-- --:--:-- --:--:--   97k
=> Downloading nvm from git to '/Users/baudouindebayser/.nvm'
=> Cloning into '/Users/baudouindebayser/.nvm'...
remote: Enumerating objects: 378, done.
remote: Counting objects: 100% (378/378), done.
remote: Compressing objects: 100% (326/326), done.
remote: Total 378 (delta 43), reused 181 (delta 25), pack-reused 0 (from 0)
Receiving objects: 100% (378/378), 375.87 KiB | 5.97 MiB/s, done.
Resolving deltas: 100% (43/43), done.
* (HEAD detached at FETCH_HEAD)
  master
=> Compressing and cleaning up git repository

=> nvm source string already in /Users/baudouindebayser/.zshrc
=> bash_completion source string already in /Users/baudouindebayser/.zshrc
=> Close and reopen your terminal to start using nvm or run the following to use it now:

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && . "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
➜  dotfiles git:(master) nvm -v
0.39.1
➜  dotfiles git:(master) nvm install 20.17.0
Downloading and installing node v20.17.0...
Downloading https://nodejs.org/dist/v20.17.0/node-v20.17.0-darwin-arm64.tar.xz...
############################################################################################################################################################### 100.0%
Computing checksum with shasum -a 256
Checksums matched!
Now using node v20.17.0 (npm v10.8.2)
Creating default alias: default -> 20.17.0 (-> v20.17.0)
➜  dotfiles git:(master) node -v
v20.17.0
➜  dotfiles git:(master) nvm cache clear
nvm cache cleared.
➜  dotfiles git:(master) corepack enable
yarn set version stable
! Corepack is about to download https://registry.yarnpkg.com/yarn/-/yarn-1.22.22.tgz
? Do you want to continue? [Y/n] Y

! Corepack is about to download https://repo.yarnpkg.com/4.5.0/packages/yarnpkg-cli/bin/yarn.js
? Do you want to continue? [Y/n] Y

➤ YN0000: Done in 0s 3ms
➜  dotfiles git:(master) ✗ yarn -v
4.5.0
➜  dotfiles git:(master) ✗ brew install sqlite
==> Downloading https://formulae.brew.sh/api/formula.jws.json

==> Downloading https://formulae.brew.sh/api/cask.jws.json

Warning: sqlite 3.46.1 is already installed and up-to-date.
To reinstall 3.46.1, run:
  brew reinstall sqlite
➜  dotfiles git:(master) ✗ sqlite3 -version
3.43.2 2023-10-10 13:08:14 1b37c146ee9ebb7acd0160c0ab1fd11017a419fa8a3187386ed8cb32b709aapl (64-bit)
➜  dotfiles git:(master) ✗ brew install postgresql@15 libpq
brew link --force libpq
==> Downloading https://ghcr.io/v2/homebrew/core/postgresql/15/manifests/15.8-1
############################################################################################################################################################### 100.0%
==> Fetching dependencies for postgresql@15: krb5
==> Downloading https://ghcr.io/v2/homebrew/core/krb5/manifests/1.21.3
############################################################################################################################################################### 100.0%
==> Fetching krb5
==> Downloading https://ghcr.io/v2/homebrew/core/krb5/blobs/sha256:c7e8ec4458b77cb3bdc1bea7b6db6f6dfa6bb6c377cc0e6bd48f6d3f89d98f6b
############################################################################################################################################################### 100.0%
==> Fetching postgresql@15
==> Downloading https://ghcr.io/v2/homebrew/core/postgresql/15/blobs/sha256:3faba25b019841450c38dc20fbb0e2df2f80773e8bc078dda91aaee9d3cbc6cd
############################################################################################################################################################### 100.0%
==> Downloading https://ghcr.io/v2/homebrew/core/libpq/manifests/17.0
############################################################################################################################################################### 100.0%
==> Fetching libpq
==> Downloading https://ghcr.io/v2/homebrew/core/libpq/blobs/sha256:85f7d3d183a0959b8fec6f888b5b69f409281da844499e8ac32ba4ec7d6a2ed9
############################################################################################################################################################### 100.0%
==> Installing dependencies for postgresql@15: krb5
==> Installing postgresql@15 dependency: krb5
==> Downloading https://ghcr.io/v2/homebrew/core/krb5/manifests/1.21.3
Already downloaded: /Users/baudouindebayser/Library/Caches/Homebrew/downloads/c5793441ca90aa09420dddd84f19d4aaf86da4f0b3f60c84940d77b1cb4c6863--krb5-1.21.3.bottle_manifest.json
==> Pouring krb5--1.21.3.arm64_sonoma.bottle.tar.gz
🍺  /opt/homebrew/Cellar/krb5/1.21.3: 163 files, 5.6MB
==> Installing postgresql@15
==> Pouring postgresql@15--15.8.arm64_sonoma.bottle.1.tar.gz
==> /opt/homebrew/Cellar/postgresql@15/15.8/bin/initdb --locale=C -E UTF-8 /opt/homebrew/var/postgresql@15
==> Caveats
This formula has created a default database cluster with:
  initdb --locale=C -E UTF-8 /opt/homebrew/var/postgresql@15

postgresql@15 is keg-only, which means it was not symlinked into /opt/homebrew,
because this is an alternate version of another formula.

If you need to have postgresql@15 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/postgresql@15/bin:$PATH"' >> ~/.zshrc

For compilers to find postgresql@15 you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/postgresql@15/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/postgresql@15/include"

For pkg-config to find postgresql@15 you may need to set:
  export PKG_CONFIG_PATH="/opt/homebrew/opt/postgresql@15/lib/pkgconfig"

To start postgresql@15 now and restart at login:
  brew services start postgresql@15
Or, if you don't want/need a background service you can just run:
  LC_ALL="C" /opt/homebrew/opt/postgresql@15/bin/postgres -D /opt/homebrew/var/postgresql@15
==> Summary
🍺  /opt/homebrew/Cellar/postgresql@15/15.8: 3,706 files, 62.8MB
==> Running `brew cleanup postgresql@15`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
==> Pouring libpq--17.0.arm64_sonoma.bottle.tar.gz
==> Caveats
libpq is keg-only, which means it was not symlinked into /opt/homebrew,
because conflicts with postgres formula.

If you need to have libpq first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/libpq/bin:$PATH"' >> ~/.zshrc

For compilers to find libpq you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/libpq/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/libpq/include"

For pkg-config to find libpq you may need to set:
  export PKG_CONFIG_PATH="/opt/homebrew/opt/libpq/lib/pkgconfig"
==> Summary
🍺  /opt/homebrew/Cellar/libpq/17.0: 2,387 files, 32.3MB
==> Running `brew cleanup libpq`...
==> Caveats
==> postgresql@15
This formula has created a default database cluster with:
  initdb --locale=C -E UTF-8 /opt/homebrew/var/postgresql@15

postgresql@15 is keg-only, which means it was not symlinked into /opt/homebrew,
because this is an alternate version of another formula.

If you need to have postgresql@15 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/postgresql@15/bin:$PATH"' >> ~/.zshrc

For compilers to find postgresql@15 you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/postgresql@15/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/postgresql@15/include"

For pkg-config to find postgresql@15 you may need to set:
  export PKG_CONFIG_PATH="/opt/homebrew/opt/postgresql@15/lib/pkgconfig"

To start postgresql@15 now and restart at login:
  brew services start postgresql@15
Or, if you don't want/need a background service you can just run:
  LC_ALL="C" /opt/homebrew/opt/postgresql@15/bin/postgres -D /opt/homebrew/var/postgresql@15
==> libpq
libpq is keg-only, which means it was not symlinked into /opt/homebrew,
because conflicts with postgres formula.

If you need to have libpq first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/libpq/bin:$PATH"' >> ~/.zshrc

For compilers to find libpq you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/libpq/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/libpq/include"

For pkg-config to find libpq you may need to set:
  export PKG_CONFIG_PATH="/opt/homebrew/opt/libpq/lib/pkgconfig"
Linking /opt/homebrew/Cellar/libpq/17.0... 381 symlinks created.

If you need to have this software first in your PATH instead consider running:
  echo 'export PATH="/opt/homebrew/opt/libpq/bin:$PATH"' >> ~/.zshrc
➜  dotfiles git:(master) ✗ brew services start postgresql@15
==> Tapping homebrew/services
Cloning into '/opt/homebrew/Library/Taps/homebrew/homebrew-services'...
remote: Enumerating objects: 3328, done.
remote: Counting objects: 100% (475/475), done.
remote: Compressing objects: 100% (153/153), done.
remote: Total 3328 (delta 376), reused 326 (delta 321), pack-reused 2853 (from 1)
Receiving objects: 100% (3328/3328), 957.30 KiB | 8.78 MiB/s, done.
Resolving deltas: 100% (1617/1617), done.
Tapped 2 commands (49 files, 1.1MB).
==> Successfully started `postgresql@15` (label: homebrew.mxcl.postgresql@15)
➜  dotfiles git:(master) ✗ psql -d postgres
psql (17.0, server 15.8 (Homebrew))
Type "help" for help.

postgres=# \q
➜  dotfiles git:(master) ✗ exec zsh
➜  dotfiles git:(master) ✗ curl -Ls https://raw.githubusercontent.com/lewagon/setup/master/check.rb > _.rb && ruby _.rb && rm _.rb || rm _.rb
Checking shell...
[OK] Your default shell is zsh
Checking ruby version...
[OK] Your default ruby version is 3.3.5
Checking git version...
[OK] Your default git version is 2.46.2
Checking git/Github email matching...
Please go to https://github.com/settings/emails and make sure that
the following email is listed on that page:
👉  baud2bsr@hotmail.fr
Is that the case? (y/n + <Enter>)
> y
[OK] git email is included in Github emails
Checking GitHub profile picture...
Your username on GitHub is GoeletteSAS, checking your profile picture now...
[OK] Thanks for uploading a GitHub profile picture 📸
Checking git editor setup...
[OK] VS Code is your default git editor
Checking ruby gems...
[OK] Everything's fine

🚀  Awesome! Your computer is now ready!
➜  dotfiles git:(master) ✗ curl -s https://kitt.lewagon.com/camps/1811/setup_script/GoeletteSAS | bash
Cloning into 'fullstack-challenges'...
remote: Enumerating objects: 80029, done.
remote: Counting objects: 100% (31/31), done.
remote: Compressing objects: 100% (30/30), done.
remote: Total 80029 (delta 5), reused 15 (delta 1), pack-reused 79998 (from 1)
Receiving objects: 100% (80029/80029), 115.36 MiB | 13.03 MiB/s, done.
Resolving deltas: 100% (35297/35297), done.
Updating files: 100% (16193/16193), done.
[master 2a2e90d86] I am so ready
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 READY
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 274 bytes | 274.00 KiB/s, done.
Total 3 (delta 1), reused 1 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:GoeletteSAS/fullstack-challenges.git
   ac9fa739b..2a2e90d86  master -> master
➜  dotfiles git:(master) ✗          
