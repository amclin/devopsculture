require 'jekyll'

# Extend string to allow for bold text.
class String
  def bold
    "\033[1m#{self}\033[0m"
  end
end

task :default => :build

# Rake Jekyll tasks
task :build do
  puts 'Building site...'.bold
  Jekyll::Commands::Build.process(profile: true)
end

task :deploy do
  puts 'Deploying site...'.bold
  Jekyll::GitDeployTask.new(:deploy)
end
