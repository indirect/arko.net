class Deploy < Thor::Group
  desc "Updates the repo at arko.net with the lastest changes"

  # everything squeezed into one method so it only sshes once
  def run_deploy
    $stdout.sync = true
    system("git push")
    system("ssh arko 'cd /home/arko.net/web && git clean -f && git pull'")
  end
end
