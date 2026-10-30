# authorized_keys

Public SSH keys of my personal machines. One key per line, named by machine in the comment.

Only machines I trust go here. Isolated company laptops never do.

```sh
mkdir -p ~/.ssh && chmod 700 ~/.ssh
curl -fsSL https://raw.githubusercontent.com/ikhrustalev/authorized_keys/main/authorized_keys >> ~/.ssh/authorized_keys
chmod 600 ~/.ssh/authorized_keys
```

## New company laptop

```sh
curl -fsSL https://ilyak.sh | bash
```

`new-mac` installs Homebrew, creates an SSH key, and posts the public key to a one-time ntfy.sh topic. It prints a code. Run `accept-laptop <code>` on a personal Mac to give the laptop read access to my configs repo, and the laptop continues with its setup. The code is a hash of the key, so a swapped key is rejected.
