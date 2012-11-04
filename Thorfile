class Default < Thor
  desc "deploy", "Pushes the latest files to arko.net"
  def deploy
    $stdout.sync = true
    system("git push")
    opts = "-avz -essh"
    opts << " --exclude-from=.gitignore"
    opts << " --delete-after"
    source = "public/"
    target = "arko:/home/arko.net/web/public/"
    cmd = "rsync #{opts} #{source} #{target}"
    puts cmd
    system cmd
  end
end
