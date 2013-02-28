# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "mymoip"
  gem.homepage = "http://github.com/Irio/mymoip"
  gem.license = "MIT"
  gem.summary = "MoIP transactions in a gem to call your own."
  gem.description = "Provides a implementation of MoIP's transparent checkout."
  gem.email = "irio.musskopf@caixadeideias.com.br"
  gem.authors = ["Irio Irineu Musskopf Junior"]
  gem.add_dependency "activemodel"
  gem.add_dependency "builder"
  gem.add_dependency "httparty"
  gem.add_development_dependency "bundler"
  gem.add_development_dependency "jeweler"
  gem.add_development_dependency "mocha"
  gem.add_development_dependency "rdoc"
  gem.add_development_dependency "turn"
  gem.add_development_dependency "vcr"
  gem.add_development_dependency "webmock"
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

task :default => :test

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "mymoip #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
