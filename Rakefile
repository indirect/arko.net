desc "Pushes the latest files to arko.net"
task :deploy do
  sh "git pull --rebase"
  sh "git push"
  puts "Netlify build running..."
end
