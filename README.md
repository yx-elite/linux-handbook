# Linux Handbook

![Linux](https://img.shields.io/badge/Linux-system_administration-FCC624?logo=linux&logoColor=white) ![Bash](https://img.shields.io/badge/Bash-shell_%26_scripting-4EAA25?logo=gnubash&logoColor=white) ![Red Hat family](https://img.shields.io/badge/Red_Hat_family-dnf_%2F_rpm-EE0000?logo=redhat&logoColor=white) ![Debian family](https://img.shields.io/badge/Debian_family-apt_%2F_deb-A81D33?logo=debian&logoColor=white)

A personal reference for Linux system administration: **notes**, **hands-on labs** and **reusable scripts**. Everything is organised **by topic, not by source**, so what I learn from courses, docs, books or real work all ends up in the same place.

> [!NOTE]
> Personal study notes, written in my own words. Third-party materials belong to their authors and are not stored in this repo.

[Topics](#topics) · [Lab environment](#lab-environment) · [Find things](#how-to-find-things) · [Templates](#templates) · [VS Code setup](#writing-notes-in-vs-code) · [License](#license)

## Repository layout

Notes, labs and scripts each have their own folder. Every topic and lab folder has a `README.md` index and keeps its screenshots in `attachments/`.

```text
linux-handbook/
├── README.md                 ← you are here
├── LICENSE
├── .vscode/                  ← shared editor settings
├── notes/                    ← topic notes (main content)
│   ├── 01-getting-started/
│   │   ├── README.md         ← topic index
│   │   ├── installing-linux.md
│   │   └── attachments/      ← screenshots
│   ├── 02-filesystem/
│   └── ...
├── labs/                     ← hands-on exercises
│   └── 01-almalinux-vm-apple-silicon/
│       ├── README.md
│       └── attachments/
├── scripts/                  ← reusable shell scripts
└── templates/                ← starting points for new files
    └── note.md
```

## Topics

Numbered in learning order, from the first login to running services. Each topic links to an index of its notes.

1. **[Getting Started](notes/01-getting-started/README.md)** → Linux distributions, installing Linux in a VM, and logging in.
2. **[Filesystem](notes/02-filesystem/README.md)** → How Linux lays out files, and how to move around, list, find and manage them.
3. **[The Shell](notes/03-shell/README.md)** → Working in the shell: commands, help, redirection, variables, history and shortcuts.
4. **[Text and Editors](notes/04-text-and-editors/README.md)** → Reading, searching, comparing and editing text files.
5. **[Permissions](notes/05-permissions/README.md)** → Who can read, write and run what — normal and special permissions.
6. **[Processes and Scheduling](notes/06-processes-and-scheduling/README.md)** → Running, watching and stopping processes, and running jobs on a schedule.
7. **[Users and Groups](notes/07-users-and-groups/README.md)** → Creating and managing users and groups, and running commands as someone else.
8. **[Package Management](notes/08-package-management/README.md)** → Installing and updating software on RPM-based and Debian-based distros.
9. **[Boot and Logging](notes/09-boot-and-logging/README.md)** → What happens when Linux starts, and where the system writes its logs.
10. **[Storage](notes/10-storage/README.md)** → Disks, partitions, filesystems and LVM.
11. **[Networking](notes/11-networking/README.md)** → IP basics, DNS, DHCP, troubleshooting, SSH and moving files between machines.
12. **[Shell Scripting](notes/12-shell-scripting/README.md)** → Writing Bash scripts to automate work.
13. **[Services](notes/13-services/README.md)** → Installing and running common server software.

## Lab environment

Where I practise and test the commands in these notes.

- **Local:** VMware Fusion Pro on a MacBook (Apple Silicon)
- **Cloud:** AWS EC2 instances
- **Red Hat family:** AlmaLinux *version* (main), Amazon Linux
- **Debian family:** Ubuntu

## How to find things

Browse by topic, skim a note, or search across everything.

- **Browse:** open a topic folder → its `README.md` lists every note.
- **Skim:** every note uses the same headings — *Key ideas, Examples, Related, References* — so you can jump straight to the part you need. Each topic's `README.md` also has a *Quick reference* listing every command in that topic.
- **Search in VS Code:** <kbd>Cmd + Shift + F</kbd> → searches every note at once.
- **Search on GitHub:** type `repo:yx-elite/linux-handbook chmod` in the top search bar.
- **Search from the terminal:** run this in the repo folder.

```bash
grep -rn --include='*.md' 'chmod' notes/ labs/
```

## Templates

Start every new note from a template, so it already has the standard headings.

- [`templates/note.md`](templates/note.md) → a topic note: *Key ideas, Examples, Related, References*.

To use it, copy it into the topic folder, rename it and replace the placeholder text:

```bash
cp templates/note.md notes/05-permissions/umask.md
```

Then add the note to the topic's `README.md`.

## Writing notes in VS Code

The repo includes VS Code settings (`.vscode/settings.json`) and recommended extensions (`.vscode/extensions.json`). Open the folder and install the extensions when VS Code asks. Then:

- **Paste a screenshot:** <kbd>Cmd + V</kbd> in a note → VS Code saves it into `attachments/` and writes the image link for you.
- **Preview like GitHub:** <kbd>Cmd + Shift + V</kbd> → preview, or <kbd>Cmd + K V</kbd> → side-by-side.
- **Move or rename a note** → links that point to it update automatically.

## License

[MIT License](LICENSE) — free to reuse the notes and scripts with credit. Third-party materials are not included and belong to their authors.

All diagrams are drawn in [Miro](https://miro.com).
