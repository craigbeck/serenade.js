{Build} = require './build'
{Serenade} = require './src/serenade'
fs = require 'fs'

task 'build', 'build the whole thing', ->
  Build.unpacked (content) -> fs.writeFileSync "extras/serenade.#{Serenade.VERSION}.js", content
  Build.minified (content) -> fs.writeFileSync "extras/serenade.#{Serenade.VERSION}.min.js", content
  Build.gzipped  (content) -> fs.writeFileSync "extras/serenade.#{Serenade.VERSION}.min.js.gz", content
