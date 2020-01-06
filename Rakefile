# frozen_string_literal: true

# Copyright (c) 2019 Danil Pismenny <danil@brandymint.ru>

# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require_relative 'config/application'

Rails.application.load_tasks

require 'rubocop/rake_task'

RuboCop::RakeTask.new(:rubocop) do |t|
  t.options = ['--display-cop-names']
  t.fail_on_error = true
end

task default: %i[test rubocop]
