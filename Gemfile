source 'https://rubygems.org'
# Add default group gems to `metasploit-framework.gemspec`:
#   spec.add_runtime_dependency '<name>', [<version requirements>]
gemspec name: 'metasploit-framework'

gem 'bit-struct', git: 'https://github.com/busterb/bit-struct', branch: 'ruby-2.4'
gem 'method_source', git: 'https://github.com/banister/method_source', branch: 'master'
gem 'rubyntlm', git: 'https://github.com/WinRb/rubyntlm', branch: 'master'

# separate from test as simplecov is not run on travis-ci
group :coverage do
  # code coverage for tests
  gem 'simplecov'
end

group :development do
  # Markdown formatting for yard
  gem 'redcarpet'
  # generating documentation
  gem 'yard'
  # for development and testing purposes
  gem 'pry', git: 'https://github.com/pry/pry', branch: 'master'
  # module documentation
  gem 'octokit'
  # metasploit-aggregator as a framework only option for now
  # Metasploit::Aggregator external session proxy
  gem 'metasploit-aggregator'
end

group :development, :test do
  # automatically include factories from spec/factories
  gem 'factory_girl_rails', '>= 4.9.0'
  # Make rspec output shorter and more useful
  gem 'fivemat'
  # running documentation generation tasks and rspec tasks
  gem 'rake'
  # Define `rake spec`.  Must be in development AND test so that its available by default as a rake test when the
  # environment is development
  gem 'rspec-rails', '>= 3.6.0'
end

group :test do
  # cucumber extension for testing command line applications, like msfconsole
  gem 'aruba'
  # cucumber + automatic database cleaning with database_cleaner
  gem 'cucumber-rails', '>= 2.1.0', :require => false
  gem 'shoulda-matchers'
  # Manipulate Time.now in specs
  gem 'timecop'
end
