namespace :greeting do
  task :hello do
    puts "hello from Rake!"
  end

  task :hola do
    puts 'hola de Rake!'
  end

  desc "just if you are wondering"
  task :here do
    puts "I am here!"
  end
end

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  task :environment do
    require_relative './config/environment'
  end

  desc "seed the database with some placeholder data"
  task seed: :environment do
    require_relative './db/seeds'
  end
end

desc 'them prying eyes'
task :environment do
  require_relative './config/environment'
end
task console: :environment do
  Pry.start
end
