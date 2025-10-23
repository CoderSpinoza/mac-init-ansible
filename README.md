# mac-init-ansible

Ansible playbook for initializing a new Mac with automated setup and configuration.

## Prerequisites

### Install Homebrew

Homebrew is a package manager for macOS that makes it easy to install and manage software.

1. Open Terminal and run the following command:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Follow the on-screen instructions to complete the installation.

3. After installation, you may need to add Homebrew to your PATH. The installer will provide specific commands based on your Mac's architecture (Intel or Apple Silicon). For example:

   - **Apple Silicon (M1/M2/M3):**
     ```bash
     echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
     eval "$(/opt/homebrew/bin/brew shellenv)"
     ```

4. Verify the installation:

```bash
brew --version
```

### Install Ansible

Once Homebrew is installed, you can install Ansible:

1. Install Ansible using Homebrew:

```bash
brew install ansible
```

2. Verify the installation:

```bash
ansible --version
```

## Usage

To run the playbook:

```bash
ansible-playbook playbook.yml
```

To run with elevated privileges (if needed):

```bash
ansible-playbook playbook.yml --ask-become-pass
```