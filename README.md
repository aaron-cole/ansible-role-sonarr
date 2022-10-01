# ansible-role-sonarr
 
=========

Ansible Role to install sonarr, an automated downloader, watchlist, monitoring program for tv shows.

Requirements
------------

Minimum Ansible version required is Ansible 2.9

Role Variables
--------------
Role variables have good defined defaults, which are located in `defaults/main.yml`.
Current version includes the following variables with default values:

### Defaults
| Name               | Default Value | Description                  |
|--------------------|---------------|------------------------------|
| `sonarr_user`       | sonarr | The primary user to run sonarr     |
| `sonarr_uid`        | *optional* | Commented out by default |
| `sonarr_group`      | media | The primary group for `sonarr_user` |
| `sonarr_group_gid`  | *optional* | Commented out by default |
| `sonarr_base_install_dir` | /opt | Install directory for sonarr |
| `sonarr_config_dir` |  /opt/data/sonarr | Data directory to store configuration |
| `sonarr_download_url` | https://services.sonarr.tv/v1/download/main/latest?version=3&os=linux | Link to the sonarr git hub latest release |
| `sonarr_port` | 8989 | Port in which sonarr operates on, to add to Firewalld |
| `sonarr_packages` | `See defaults/main.yml for complete list` | List of Packages Required to install and run sonarr |

Dependencies
------------

None

Example Playbook
----------------

   - hosts: sonarr_servers
      roles:
        - aaron_cole.ansible_role_sonarr


License
-------

GPLv3

Author Information
------------------

Created by Aaron Cole

