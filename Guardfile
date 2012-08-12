# A sample Guardfile
# More info at https://github.com/guard/guard#readme

# Add files and commands to this file, like the example:
#   watch(%r{file/path}) { `command(s)` }
#
guard 'steering', :output_folder => "example_basic/templates" do
 	watch(%r{^example_basic/handlebars/.*\.handlebars$})
end

guard 'steering', :output_folder => "example_partials/templates", :register_partials => true do
 	watch(%r{^example_partials/handlebars/.*\.handlebars$})
end
