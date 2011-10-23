class Deploy < Thor::Group
  desc "Pushes the latest files to arko.net"

  def run_deploy
    $stdout.sync = true
    system("git push")
    opts = "-avz -essh"
    opts << " --exclude '.DS_Store'"
    opts << " --delete-after"
    source = "public/"
    target = "arko:/home/arko.net/web/public/"
    system("rsync #{opts} #{source} #{target}")
  end
end
