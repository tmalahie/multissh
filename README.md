# multissh
A script to manage multiple load-balanced servers at the same time via ssh

Usage:
```bash
bash./sshm user@host1,user@host2 [-args]
```

Example (no arguments):
```bash
./sshm timothe@example.com,timothe@example.net
```

Example (some arguments):
```bash
./sshm timothe@example.com,timothe@example.net -p 21 -o StrictHostKeyChecking=no
```

This program will launch multiple terminal instances, one terminal per server you connect to.
Then, when you press any key, it will propagate this key to all the terminal instances.

This program is a convenient way to apply the same operations to multiple servers. For example if you have a set of identical load-balanced servers and you want to apply a patch on all the servers. You could ssh to each server individually and apply the patch one by one, but it's longer and boring. This program let you manage all at once, which is way more powerful!

It is very simillar to `clusterssh`, but less heavy (it's a simple python script), and a bit more convenient (it uses your default terminal application to run the program, instead of xterm).
