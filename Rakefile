# Project tasks.  Run `rake -T` to list them.

DEV  = "_config.yml"
PROD = "_config.yml,_config_prod.yml"

desc "Preview at http://127.0.0.1:4000 with live reload (builds to _site/)"
task :preview do
  sh "bundle exec jekyll serve --livereload --config #{DEV}"
end

desc "Build the production site into docs/ for GitHub Pages"
task :publish do
  sh "JEKYLL_ENV=production bundle exec jekyll build --config #{PROD}"
  puts "\nBuilt to docs/ — #{Dir.glob('docs/**/*').count { |f| File.file?(f) }} files"
end

desc "Delete build output (_site/ and docs/)"
task :clean do
  sh "bundle exec jekyll clean --config #{DEV}"
  sh "bundle exec jekyll clean --config #{PROD}"
end

task default: :publish
