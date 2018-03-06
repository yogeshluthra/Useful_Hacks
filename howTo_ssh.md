## How to secure login to remote machine
- First we need a public key, which should be added to `.ssh/authorized_keys` on host machine (basically the content of `id_rsa.pub` file)
  - If needed, create new ssh key as following:
    - ssh-keygen -t rsa -C "your_email@example.com"
      [visit this webpage](https://confluence.atlassian.com/bitbucketserver/creating-ssh-keys-776639788.html)

- Then update `~/.ssh/config` file, as
  `Host robot
      HostName 192.168.20.195
      User lewis
      Port 22`

- Then simply `ssh robot`
  - where `robot` is the host machine in `.ssh/config` file.

- 
