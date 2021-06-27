My Helpdesk using Helpy: A Modern Helpdesk Platform
====================================

Helpy is a modern help desk platform written in Ruby on Rails and released under the MIT license.  The goal of Helpy is to power your support email and ticketing, integrate seamlessly with your app, and run an amazing customer helpcenter.

setup in rubymine
====
edit run configuration 2.5.1 (not global)

Ruby SDK and Gem set default bundler 1.17.3

gem uninstall bundler  --version ' 2.0.1'

gem install bundler --version '1.17.3'

can not resolve dependencies......

instead get gemfile and gemfile.lock from current helpy project?

1) bundle install - DONE

development setup
===================
Unpack the Helpy assets and setup your database:

RAILS_ENV=development rake assets:precompile

RAILS_ENV=development rake db:setup

then run the onboarding in the browser

Configure inbound and outbound email! => skip for now (mandrill is an option)

get started! button appears.

production set up the database and secrets files:
======================================
cp config/database.do.yml config/database.yml
rake secret
copy the key to

nano config/secrets.yml

nano config/database.yml

touch /home/deploy/helpy/log/production.log

chmod 0664 /home/deploy/helpy/log/production.log

Unpack the Helpy assets and setup your database:

RAILS_ENV=production rake assets:precompile

RAILS_ENV=production rake db:setup

testing workflow
====
local -> htest-rose github -> server

customize theme flat
======================
files are located in the theme folder


License
=======
Copyright 2021 Mokanova inc.
Helpy Core is released under the MIT open source license.