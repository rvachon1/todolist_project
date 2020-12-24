require 'bundler/gem_tasks'
require 'rake/testtask'
require 'find'

desc "Find all files w/o `.`"
task :find do
  Find.find('.') do |path|
    puts path if (!(path =~ /\/\./) && File.file?(path))
  end
end

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task default: :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end