#!/usr/bin/env rake
require File.expand_path('../config/application', __FILE__)

include Rake::DSL

Gemcutter::Application.load_tasks

desc "Run all tests and features"
task :default => [:test, :cucumber]

desc "Run daily" # Currently time of day is not specifically calibrated
task :daily_cron => %w[gemcutter:downloads:rollover]

# Change this if we ever move to hourly cron
task :cron => :daily_cron
