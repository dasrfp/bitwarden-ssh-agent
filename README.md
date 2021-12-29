# Bitwarden SSH Agent

## Requirements
* You need to have the [Bitwarden CLI tool](https://github.com/bitwarden/cli) installed and available in the `$PATH` as `bw`.
* `ssh-agent` must be running in the current session.

## What does it do?
Fetches SSH keys stored in Bitwarden vault and adds them to `ssh-agent`.

##  How to use it
1. Run
   ```shell
   ./bw_add_sshkeys.py
   ```
2. Enter your Bitwarden credentials, if a Bitwarden vault session is not already set.
3. (optional) Enter your SSH keys' passphrases.

## Storing the keys in BitWarden
1. Create a folder called `ssh-agent` (can be overridden on the command line).
2. Add an new secure note to that folder.
3. Add the private key text as note body.
5. Repeat steps 2-3 for each subsequent key

## Improvements to be made
* make a way to prevent local echo of passphrase
