# -*- coding: utf-8 -*-

C ||= CONFIG = {}

C[:REPOS] ||= ENV['REPOS'].split(/[ ,;]/) || ['bookbase', 'book']

desc 'Build images'
task :build do |t|
  C[:REPOS].map{|d|
    Dir.chdir(d) do
      sh 'rake build'
    end
  }
end

desc 'Remove images'
task :clean do |t|
  C[:REPOS].map{|d|
    Dir.chdir(d) do
      sh 'rake clean'
    end
  }
end

task :default => :build
