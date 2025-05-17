# Ansible Website

A modern, visually appealing website for learning and exploring Ansible automation. This project provides resources, guides, and examples to help users automate IT infrastructure using Ansible.

## Features

- **Beautiful, Responsive UI**: Clean design with mobile support and modern CSS.
- **Quick Start Example**: YAML playbook sample for instant understanding.
- **Feature Highlights**: Automation, repeatability, modularity, and agentless operation.
- **How-To Section**: Step-by-step workflow for defining, configuring, executing, and maintaining Ansible automation.
- **Resource Links**: Easy access to guides, installation, YAML syntax, inventory, roles, and playbooks.
- **Use Cases**: Real-world automation scenarios (web server setup, firewall, reverse proxy, cron jobs, multi-server deployment).
- **Newsletter Signup**: Stay updated with the latest Ansible tips and tutorials.

## Project Structure

```
ansible/
├── index.html                # Main website HTML
├── README.md                 # Project documentation
└── assets/
    ├── css/
    │   └── style.css         # Main stylesheet
    └── img/                  # Images and icons
```

## Getting Started

1. **Clone the repository**
   ```zsh
   git clone <your-repo-url>
   cd ansible
   ```
2. **Open `index.html` in your browser**
   - No build step required. All assets are static.

## Customization

- Update images in `assets/img/` as needed.
- Edit `index.html` to add or change content.
- Modify `assets/css/style.css` for custom styles.

## Example Ansible Playbook

```yaml
- hosts: all
  become: true
  tasks:
    - name: Install Traefik
      get_url:
        url: https://yourname.github.io/traefik
        dest: /tmp/traefik.tar.gz
    - name: Extract Traefik
      unarchive:
        src: /tmp/traefik.tar.gz
        dest: /usr/local/bin
        remote_src: yes
        extra_opts: [--strip-components=1]
    - name: Run Traefik
      command: /usr/local/bin/traefik --entrypoints.web.address=:80
```

## About

This project is maintained by a team passionate about IT automation and Ansible. Our goal is to make automation accessible, practical, and visually engaging for everyone.

---

&copy; Ansible 2025. All rights reserved.
