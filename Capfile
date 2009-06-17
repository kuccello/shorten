load 'deploy' if respond_to?(:namespace) # cap2 differentiator
 
set :application, "code2cash.com"
set :domain,      "code2cash.com"
set :deploy_to,   "/home/kuccello/Development/vhosts/#{application}"

set :scm, :git
set :repository, "git://github.com/kuccello/shorten.git"

server domain, :web, :app
 
# Specific to Rails Machine
set :app_server, :passenger
set :user, "kuccello"
set :runner, user
set :admin_runner, user
default_run_options[:pty] = true
 
namespace :deploy do
  task :restart do
    run "touch #{current_path}/tmp/restart.txt"
  end
end
