class Deploy < Thor::Group
  desc "Pushes the latest files to arko.net"

  def run_deploy
    $stdout.sync = true
    system("git push")
    from = "public/"
    to = "arko:/home/arko.net/web/public/"
    system("rsync -avz -essh --exclude '.DS_Store' #{from} #{to}")
  end
end
