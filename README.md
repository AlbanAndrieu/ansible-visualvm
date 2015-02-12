## alban.andrieu.visualvm

[![Travis CI](http://img.shields.io/travis/AlbanAndrieu/ansible-visualvm.svg?style=flat)](http://travis-ci.org/AlbanAndrieu/ansible-visualvm) [![Branch](http://img.shields.io/github/tag/AlbanAndrieu/ansible-visualvm.svg?style=flat-square)](https://github.com/AlbanAndrieu/ansible-visualvm/tree/master) [![Donate](https://img.shields.io/gratipay/AlbanAndrieu.svg?style=flat)](https://www.gratipay.com/AlbanAndrieu)  [![Ansible Galaxy](http://img.shields.io/badge/galaxy-alban.andrieu.visualvm-blue.svg?style=flat)](https://galaxy.ansible.com/list#/roles/2731) [![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)

Ensures that visualvm is properly installed and configured

### Installation

This role requires at least Ansible `v1.6.3`. 

To install it, run:

    ansible-galaxy install alban.andrieu.visualvm



### Role variables

List of default variables available in the inventory:

```yaml
        visualvm_enabled: yes                       # Enable module
    
    #user: 'albandri' #please override me
    user: "{{ lookup('env','USER') }}"
    visualvm_owner: "{{ user }}"
    visualvm_group: "{{ visualvm_owner }}"
    #home: '~' #please override me
    home: "{{ lookup('env','HOME') }}"
    visualvm_owner_home: "{{ home }}"
    visualvm_base_dir: "/usr/local/visualvm"
    #visualvm_home_dir: "/usr/share/visualvm"
    visualvm_home_dir: "{{ home }}/.visualvm"
    visualvm_home_version: "1.3.8"
    visualvm_configuration: "{{ visualvm_home_dir }}/{{ visualvm_home_version }}/repository"
    visualvm_remote_hosts_enable: no
    
    visualvm_remote_hosts:
      # Additional properties: 'serverip, servername, serverfile'.
      - {serverip: "82.231.208.223", serverhostname: "home.nabla.mobi", servername: "albandri", serverjstatdport: "2020", serverposition: "4"}
    
    visualvm_dir_tmp: "/tmp" # or override with "{{ tempdir.stdout }} in order to have be sure to download the file"
    
    visualvm_version: "138"
    
    visualvm_name: "visualvm_{{ visualvm_version }}"
    visualvm_archive: "{{ visualvm_name }}.zip"
    visualvm_url: "https://java.net/projects/visualvm/downloads/download/release{{ visualvm_version }}/{{ visualvm_archive }}"
```


### Detailed usage guide

Describe how to use in more detail...


### Authors and license

`alban.andrieu.visualvm` role was written by:
- [Alban Andrieu](fr.linkedin.com/in/nabla/) | [e-mail](mailto:alban.andrieu@free.fr) | [Twitter](https://twitter.com/AlbanAndrieu) | [GitHub](https://github.com/AlbanAndrieu)
- License: [GPLv3](https://tldrlegal.com/license/gnu-general-public-license-v3-%28gpl-3%29)

### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/AlbanAndrieu/ansible-visualvm/issues)!

***

README generated by [Ansigenome](https://github.com/nickjj/ansigenome/).
