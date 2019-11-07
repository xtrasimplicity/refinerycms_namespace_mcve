# RefineryCMS - Extension Namespacing
_MCVE for Issue #3242 on RefineryCMS: https://github.com/refinery/refinerycms/issues/3242_


# Background
- Attempting to create an extension which holds multiple related models, with a different namespace to the models themselves, to group the models.

# Steps to reproduce
- Check out this repository
- Create a blank folder for the extension:

  `mkdir -p vendor/extensions/my_group`
- Generate an engine and use this new extension name as a namespace:

  `bundle exec rails g refinery:engine my_model title:string --extension my_group --namespace my_group`


# Output
```bash
Running via Spring preloader in process 41761
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/tasks/rspec.rake
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/tasks/testing.rake
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/Rakefile
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/tmp/routes.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/es.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/it.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/tr.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/fr.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/cs.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/zh-CN.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/ru.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/en.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/nl.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/sk.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/tmp/nb.yml
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/spec/support/factories/refinery/my_models.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/spec/features/refinery/my_group/admin/my_models_spec.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/spec/spec_helper.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/spec/models/refinery/my_group/my_model_spec.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/Gemfile
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/db/migrate/1_create_my_group_my_models.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/refinerycms-my_group.gemspec
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/admin/my_models/_form.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/admin/my_models/new.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/admin/my_models/_records.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/admin/my_models/_my_models.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/admin/my_models/_actions.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/admin/my_models/_sortable_list.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/admin/my_models/edit.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/admin/my_models/_my_model.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/admin/my_models/index.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/my_models/show.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/views/refinery/my_group/my_models/index.html.erb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/models/refinery/my_group/my_model.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/controllers/refinery/my_group/my_models_controller.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/app/controllers/refinery/my_group/admin/my_models_controller.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/script/rails
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/lib/tasks/refinery/my_group.rake
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/lib/generators/refinery/my_group_generator.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/lib/tmp/refinerycms-my_group.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/lib/refinery/my_models.rb
      create  /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/lib/refinery/my_models/engine.rb
Traceback (most recent call last):
        38: from -e:1:in `<main>'
        37: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/2.5.0/rubygems/core_ext/kernel_require.rb:59:in `require'
        36: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/2.5.0/rubygems/core_ext/kernel_require.rb:59:in `require'
        35: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/activesupport-5.1.7/lib/active_support/dependencies.rb:286:in `load'
        34: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/activesupport-5.1.7/lib/active_support/dependencies.rb:258:in `load_dependency'
        33: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/activesupport-5.1.7/lib/active_support/dependencies.rb:286:in `block in load'
        32: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/activesupport-5.1.7/lib/active_support/dependencies.rb:286:in `load'
        31: from /tmp/refinerycms-extension-namespace-mcve/bin/rails:9:in `<top (required)>'
        30: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/activesupport-5.1.7/lib/active_support/dependencies.rb:292:in `require'
        29: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/activesupport-5.1.7/lib/active_support/dependencies.rb:258:in `load_dependency'
        28: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/activesupport-5.1.7/lib/active_support/dependencies.rb:292:in `block in require'
        27: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/activesupport-5.1.7/lib/active_support/dependencies.rb:292:in `require'
        26: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/railties-5.1.7/lib/rails/commands.rb:16:in `<top (required)>'
        25: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/railties-5.1.7/lib/rails/command.rb:44:in `invoke'
        24: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/railties-5.1.7/lib/rails/command/base.rb:63:in `perform'
        23: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor.rb:387:in `dispatch'
        22: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor/invocation.rb:126:in `invoke_command'
        21: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor/command.rb:27:in `run'
        20: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/railties-5.1.7/lib/rails/commands/generate/generate_command.rb:24:in `perform'
        19: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/railties-5.1.7/lib/rails/generators.rb:269:in `invoke'
        18: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor/base.rb:466:in `start'
        17: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor/group.rb:232:in `dispatch'
        16: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor/invocation.rb:133:in `invoke_all'
        15: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor/invocation.rb:133:in `map'
        14: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor/invocation.rb:133:in `each'
        13: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor/invocation.rb:133:in `block in invoke_all'
        12: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor/invocation.rb:126:in `invoke_command'
        11: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/thor-0.20.3/lib/thor/command.rb:27:in `run'
        10: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/generators/refinery/engine/engine_generator.rb:22:in `generate'
         9: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/refinery/extension_generation.rb:113:in `default_generate!'
         8: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/refinery/extension_generation.rb:213:in `merge_existing_files!'
         7: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/refinery/extension_generation.rb:213:in `each'
         6: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/refinery/extension_generation.rb:220:in `block in merge_existing_files!'
         5: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/refinery/extension_generation.rb:364:in `call'
         4: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/refinery/extension_generation.rb:373:in `merge!'
         3: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/refinery/extension_generation.rb:380:in `merged_file_contents'
         2: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/refinery/extension_generation.rb:401:in `merge_yaml'
         1: from /home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/refinery/extension_generation.rb:401:in `read'
/home/xtrasimplicity/.rbenv/versions/2.5.0/lib/ruby/gems/2.5.0/gems/refinerycms-core-4.0.3/lib/refinery/extension_generation.rb:401:in `read': No such file or directory @ rb_sysopen - /tmp/refinerycms-extension-my_group-mcve/vendor/extensions/my_group/config/locales/es.yml (Errno::ENOENT)
```

## Temporary work-around
It looks like the generator is failing to move the files from the `tmp` folders it creates, despite there not being any conflicting files.

Simply moving these files out of their `tmp` folder and into the parent, resolves the issue. i.e.
```bash
cd vendor/extensions/*extension_name*
mv lib/tmp/* lib/
mv config/locales/tmp/* config/locales/
mv config/tmp/* config/
rmdir lib/tmp
rmdir config/locales/tmp
rmdir config/tmp
```
then, re-run the generate command.

You'll end up with some duplicate files (such as DB migrations), but these can easily be removed.