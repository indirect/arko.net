class Deploy < Thor::Group
  desc "Updates the repo at arko.net with the lastest changes"

  def run_deploy
    $stdout.sync = true
    system("git push")
    # everything squeezed into one call so it only sshes once
    system("ssh arko 'cd /home/arko.net/web && git clean -f && git pull'")
  end
end
