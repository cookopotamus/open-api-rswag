# frozen_string_literal: true

source 'https://rubygems.org'

# Allow the rails version to come from an ENV setting so Travis can test multiple versions.
# See http://www.schneems.com/post/50991826838/testing-against-multiple-rails-versions/
rails_version = ENV['RAILS_VERSION'] || '5.2.3'

gem 'rails', rails_version.to_s

case rails_version.split('.').first
when '3'
  gem 'strong_parameters'
when '4', '5', '6'
  gem 'responders'
end

gem 'sqlite3', '~> 1.3.6'

gem 'open_api-rswag-api', path: './rswag-api'
gem 'open_api-rswag-ui', path: './rswag-ui'

group :test do
  gem 'capybara'
  gem 'capybara-webkit'
  gem 'generator_spec'
  gem 'rspec-rails'
  gem 'open_api-rswag-specs', path: './rswag-specs'
  gem 'test-unit'
end

group :development do
  gem 'guard-rspec', require: false
  gem 'open_api-rswag-specs', path: './rswag-specs'
  gem 'rubocop'
end

group :assets do
  gem 'therubyracer'
  gem 'uglifier'
end

gem 'byebug'
gem 'puma'
