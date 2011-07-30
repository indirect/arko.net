class Deploy < Thor::Group
  desc "Pushes the latest files to arko.net"

  def run_deploy
    $stdout.sync = true
    system("rsync -avz -essh public/ arko:/home/arko.net/web/public/")
  end
end
