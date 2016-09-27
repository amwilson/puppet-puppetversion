source ENV['GEM_SOURCE'] || "https://rubygems.org"

def location_for(place, fake_version = nil)
  if place =~ /^(git[:@][^#]*)#(.*)/
    [fake_version, { :git => $1, :branch => $2, :require => false }].compact
  elsif place =~ /^file:\/\/(.*)/
    ['>= 0', { :path => File.expand_path($1), :require => false }]
  else
    [place, { :require => false }]
  end
end

if RUBY_VERSION =~ /^1\./
  gem 'rake', '10.5.0' # still supports 1.8
  gem 'rspec-core', '= 3.1.7'
else
  gem 'rake'
end

if RUBY_VERSION =~ /^1\.9/
  gem 'json_pure', '<=2.0.1'
  gem 'json', '<2.0.0'
  # rubocop 0.42.0 requires ruby >=2; 1.8 is not supported
  # gem 'rubocop', '0.41.2'
elsif RUBY_VERSION =~ /^1\.8/
  gem 'json_pure', '< 2.0.0'
else
  # gem 'rubocop'
  gem 'rubocop-rspec', '~> 1.6' if RUBY_VERSION >= '2.3.0'
end

group :test do
  gem 'rspec-puppet',                                               :git => 'https://github.com/rodjek/rspec-puppet.git'
  gem 'puppet-lint',                                                :require => false, :git => 'https://github.com/rodjek/puppet-lint.git'
  gem 'metadata-json-lint',                                         :require => false
  gem 'rspec-puppet-facts',                                         :require => false
  gem 'rspec',                                                      :require => false
  gem 'puppet-blacksmith',                                          :require => false, :git => 'https://github.com/voxpupuli/puppet-blacksmith.git'
  gem 'voxpupuli-release',                                          :require => false, :git => 'https://github.com/voxpupuli/voxpupuli-release-gem.git'
  gem 'rubocop', '0.37.0',                                          :require => false
  gem 'rspec-puppet-utils',                                         :require => false
  gem 'puppetlabs_spec_helper',                                     :require => false
  gem 'puppet-lint-absolute_classname-check',                       :require => false
  gem 'puppet-lint-leading_zero-check',                             :require => false
  gem 'puppet-lint-trailing_comma-check',                           :require => false
  gem 'puppet-lint-version_comparison-check',                       :require => false
  gem 'puppet-lint-classes_and_types_beginning_with_digits-check',  :require => false
  gem 'puppet-lint-unquoted_string-check',                          :require => false
  gem 'puppet-lint-variable_contains_upcase',                       :require => false
  gem 'puppet', '>= 3.3.0', '< 4.0.0'
end

# group :development do
#   gem 'travis',       :require => false
#   gem 'travis-lint',  :require => false
#   gem 'guard-rake',   :require => false
# end
#
# group :system_tests do
#   gem 'beaker',                        :require => false
#   if beaker_version = ENV['BEAKER_VERSION']
#     gem 'beaker', *location_for(beaker_version)
#   end
#   if beaker_rspec_version = ENV['BEAKER_RSPEC_VERSION']
#     gem 'beaker-rspec', *location_for(beaker_rspec_version)
#   else
#     gem 'beaker-rspec',  :require => false
#   end
#   gem 'beaker-puppet_install_helper',  :require => false
# end
#
#
#
# if facterversion = ENV['FACTER_GEM_VERSION']
# gem 'facter', facterversion.to_s, :require => false, :groups => [:test]
# else
# gem 'facter', :require => false, :groups => [:test]
# end

# ENV['PUPPET_VERSION'].nil? ? puppetversion = '3.8.4' : puppetversion = ENV['PUPPET_VERSION'].to_s
# gem 'puppet', puppetversion, :require => false, :groups => [:test]

# vim:ft=ruby
