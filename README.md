# authorized_keys

Public SSH keys of my personal machines. One key per line, named by machine in the comment.

Only machines I trust go here. Isolated company laptops never do.

```sh
mkdir -p ~/.ssh && chmod 700 ~/.ssh
curl -fsSL https://raw.githubusercontent.com/ikhrustalev/authorized_keys/main/authorized_keys >> ~/.ssh/authorized_keys
chmod 600 ~/.ssh/authorized_keys
```
