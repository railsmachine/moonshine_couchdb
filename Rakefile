require 'rake'

task :doc do
  system 'rocco lib/moonshine/couchdb.rb -o doc'
  system 'bluecloth README.markdown > doc/index.html'
end
