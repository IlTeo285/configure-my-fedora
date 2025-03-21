# ansible-setup-my-workstation

Ansible Playbook to configure my personal Fedora workstations :rocket:

It will be configured:

- Install programming languages and IDE (Rust);
- Install productivity utilities (flameshot, htop, tilix, iterm2 and others...)
- Terminal prompt with custom theme of ZSH + Starship
    - Prompt Like: https://carlosneto.dev/blog/2024/2024-02-08-starship-zsh
- Configure dconf settings like keybing, shortcuts

```bash
├── files
│   └── dotfiles
│       ├── starship.toml       # custom starship theme
│       └── .zshrc              # custom zsh init file
├── role-install-tools          # configure fusion repos, snapd, rust;
│   └── ...
├── role-setup-terminal         # configure terminal prompt with zsh + starship
│   └── ...
├── playbook.yml                # run all roles
└── Makefile                    # shortcut to setup venv and run the ansible playbook
```

## Requirements

- python >= 3.7
- pip

## How to Run

```shell
# create a venv and install ansible inside it
$ make setup

# install tools and setup terminal
$ make run
```

## Manual Steps: Install Gnome Extensions (only for Fedora)

Install these extensions:

- Dash to Panel: https://extensions.gnome.org/extension/1160/dash-to-panel/
- GSConnect: https://extensions.gnome.org/extension/1319/gsconnect/
- gTile: https://extensions.gnome.org/extension/28/gtile/
- Search Light: https://extensions.gnome.org/extension/5489/search-light/

> [!WARNING]
> Use the Firefox to install these extension.

## References

- https://brew.sh/
- https://carlosneto.dev/blog/2024/2024-02-08-starship-zsh/
- https://docs.rancherdesktop.io/getting-started/installation/#installing-via-rpm-package
- https://github.com/99designs/aws-vault/
- https://github.com/ahmetb/kubectx
- https://github.com/spaceship-prompt/spaceship-prompt
- https://github.com/zsh-users/zsh-autosuggestions/
- https://ohmyz.sh/
- https://spaceship-prompt.sh/
