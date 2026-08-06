# Optional local development tasks. Run `rake -T` to list them.
#
# NONE of these publish anything. Publishing happens automatically: push to
# `main` and GitHub Actions builds and deploys. See SETUP.md.

desc "Preview at http://127.0.0.1:4000 with live reload"
task :preview do
  sh "bundle exec jekyll serve --livereload"
end

desc "Run the same production build CI runs, to catch errors early (output: _site/)"
task :build do
  sh "JEKYLL_ENV=production bundle exec jekyll build"
end

desc "Delete local build output (_site/)"
task :clean do
  sh "bundle exec jekyll clean"
end

task default: :preview
