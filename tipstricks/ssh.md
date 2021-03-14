## Github and SSH
# Set custom SSH key for repo
Clone the repository with following command:
git clone -c core.sshCommand="/usr/bin/ssh -i /home/me/.ssh/id_rsa_foo" git@github.com:me/repo.git

The key file in the command will be saved to the repository .git/config file and used automatically in the future.
