require 'rake'

task :doc do
  system 'rocco lib/moonshine/couchdb.rb -o doc'
  system 'yard doc --title "Moonshine::Couchdb" README.markdown lib/moonshine/couchdb.rb'
end

task :clean do
  system 'rm -r doc/*'
end
