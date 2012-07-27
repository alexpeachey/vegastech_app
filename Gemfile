source 'https://rubygems.org'

gem 'rails', '3.2.3'

# Bundle edge Rails instead:
# gem 'rails', :git => 'git://github.com/rails/rails.git'

gem 'sqlite3'
gem 'omniauth-twitter'
gem 'twitter'
gem 'twitter-text'
gem 'foreman'

# Gems used only for assets and not required
# in production environments by default.
group :assets do
  gem 'sass-rails',   '~> 3.2.3'
  gem 'coffee-rails', '~> 3.2.1'

  # See https://github.com/sstephenson/execjs#readme for more supported runtimes
  gem 'twitter-bootstrap-rails'
  gem 'therubyracer', :platform => :ruby

  gem 'uglifier', '>= 1.0.3'
end

gem 'jquery-rails'

# To use ActiveModel has_secure_password
# gem 'bcrypt-ruby', '~> 3.0.0'

# To use Jbuilder templates for JSON
# gem 'jbuilder'

# Use unicorn as the app server
# gem 'unicorn'

# Deploy with Capistrano
# gem 'capistrano'

# To use debugger
# gem 'ruby-debug19', :require => 'ruby-debug'

def darwin_only(require_as)
  RUBY_PLATFORM.include?('darwin') && require_as
end

def linux_only(require_as)
  RUBY_PLATFORM.include?('linux') && require_as
end

group :development do
	gem "rspec-rails"
  gem "guard-rspec"
  gem "guard-spork"

  # mac
  gem "rb-fsevent", require: darwin_only('rb-fsevent')
  gem "growl", require: darwin_only('growl')

  # linux
  gem 'rb-inotify', require: linux_only('rb-inotify')
  gem 'libnotify', require: linux_only('libnotify')

  gem 'git-deploy'
end

group :test do
	gem "rspec-rails"
  gem "factory_girl_rails"
  gem "database_cleaner"
  gem "capybara"
end

group :production do
  gem "mysql2"
  gem "unicorn"
end
