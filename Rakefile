require 'data_mapper'
require './app/chitter.rb'

namespace :db do
  desc 'Create development and test db'
  task :create do
    sh 'chitter_db_development'
    sh 'chitter_db_test'
    puts 'development and test db created'
  end

  desc 'Non destructive upgrade'
  task :auto_upgrade do
    DataMapper.auto_upgrade!
    puts 'Auto-upgrade complete (no data loss)'
  end

  desc 'Destructive upgrade'
  task :auto_migrate do
    DataMapper.auto_migrate!
    puts 'Auto-migrate complete (data was lost)'
  end
end
