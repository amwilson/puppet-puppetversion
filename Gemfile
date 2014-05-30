source ENV['GEM_SOURCE'] || "http://rubygems.org"

group :test do
  gem "rake"
  gem "puppet", ENV['PUPPET_VERSION'] || '~> 3.4.0'
  gem "puppet-lint"
  gem "rspec-puppet", :git => 'https://github.com/rodjek/rspec-puppet.git'
  gem "puppet-syntax"
  gem "puppetlabs_spec_helper"
  gem "beaker", :git => 'https://github.com/liamjbennett/beaker', :branch => 'windows_fixes'
  gem "beaker-rspec", :git => 'https://github.com/liamjbennett/beaker-rspec', :branch => 'windows_fixes'
  gem "serverspec", '~> 1.6.0'
  gem "specinfra", '~> 1.11.0'
  gem "winrm"
end

group :development do
  gem "travis"
  gem "travis-lint"
  gem "vagrant-wrapper"
  gem "puppet-blacksmith"
  gem "guard-rake"
end
