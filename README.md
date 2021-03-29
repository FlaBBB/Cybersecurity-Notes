# Cybersecurity Notes
My Markdown notes for all things cybersecurity

## Installing Obsidian

### On Windows

Go to [the download page](https://obsidian.md/download)... and click Download

### On Kali

Go to [the download page](https://obsidian.md/download), and download the AppImage. Put it in any directory you want (I went with `~/Applications`)

You can either double click the file to run it, or run it with `/path/to/Obsidian-0.11.9.AppImage`

You may get the following error while running:

```bash
┌──(mac㉿kali)-\[~/Applications\]  
└─$ ./Obsidian-0.11.9.AppImage  
\[2122:0327/193255.690087:FATAL:setuid\_sandbox\_host.cc(158)\] The SUID sandbox helper binary was found, but is not configured correctly. Rather than run without sandboxing I'm aborting now. You need to make sure that /tmp/.mount\_Obsidi1nvAuD/chrome-sandbox is owned by root and has mode 4755.  
Trace/breakpoint trap
```

To fix this, run obsidian with the `--no-sandbox` flag

I setup this alias in `~/.bashrc`:

```bash
alias obsidian="~/Applications/Obsidian-0.11.9.AppImage --no-sandbox"
```

Finally, if Obsidian stops responding on launch, update Kali:

```bash
sudo apt update
sudo apt full-upgrade -y
```

## Using Obsidian

It is easy to share individual notes from within the vault, as they are just markdown files - this lets you disseminate stuff as required, and move notes into public repositories etc.

For example, you can have a public vault of notes, linked to a public repository, where you can move writeups to as the boxes retire. This helps keep your public notes sanitised.

It also lets you push/pull down between virtual machines. OneDrive will back the notes up to the Cloud, but they will also be on Git.

Git history can show people how a collection of notes develops over time - pretty interesting, especially when putting together a cheatsheet!

As of 29/03/21, merging this vault into my main Personal Vault (so I can make links to Cyber-related notes) and using this vault as a public set of notes. Will move across any notes to be publicly shared, such as cheatsheets and writeups for retired boxes.

### Links

[Obsidian Help (Docs)](https://help.obsidian.md/Index)

[Features Overview](https://obsidian.md/features)

[Medium Guide](https://medium.com/swlh/take-better-notes-with-this-free-note-taking-app-that-wants-to-be-your-second-brain-1a97909a677b)

[What exactly is a Vault?](https://forum.obsidian.md/t/what-exactly-is-a-vault/4369/2)

[Working with Multiple Vaults](https://help.obsidian.md/How+to/Working+with+multiple+vaults)

[Referencing a Vault from another Vault](https://www.reddit.com/r/ObsidianMD/comments/hhat70/reference_a_vault_in_another_valut/)

[Single-Vault Philosophy](https://forum.obsidian.md/t/one-vault-vs-multiple-vaults/1445)

[Zettelkasten Method](https://medium.com/@rebeccawilliams9941/the-zettelkasten-method-examples-to-help-you-get-started-8f8a44fa9ae6)

[Toggling Checklists Hotkeys](https://forum.obsidian.md/t/set-hotkeys-for-creating-unordered-lists-ordered-lists-and-task-lists/4332/25)

[Key Mapping Diagram](https://keycombiner.com/collections/obsidian/winlinux/)

[Hotkeysplus Repo](https://github.com/argenos/hotkeysplus-obsidian)