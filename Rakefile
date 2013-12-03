desc "Pushes the latest files to arko.net"
task :deploy do
  sh "git push"
  opts = "-avz -essh --exclude-from=.gitignore --delete-after"
  source = "public/"
  target = "arko:/home/arko.net/web/public/"
  sh "rsync #{opts} #{source} #{target}"
end
