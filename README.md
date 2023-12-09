# My Specific Workstation Config

Another attempt to combine my workstation setup, configuration and dev config into one giant mess.

## Basics

Using ansible to install as many needed things through roles. Workstation configuration uses Ubuntu LTS, so that is what
all of the ansible configs are based on.

## Set Up

### Configuration

Make sure that the folowing information is configured in the files listed:

    - inventory.ini
        - Set up the Ip Address and SSH port for the system(s) you are configuring
    - configure.yml
        - Set the user name of the system in the remote_user field
    - .become.pass
        - Put the remote user sudo password in this file. It is ignored

### Roles and Tasks
    - Code Repositorires
        - Set up any git repositories that you want included in group_vars/workstations/repositories.yml
        - Configure paths for your stuff in group_vars/workstations/paths.yml
    - PHP
        - Set the php packages in group_vars/workstations/php.yml
        - Default php version can be changed
        - Additional packages can be installed or more versions of php with the php_packages array
    - Composer
        - If you need or don't need packages, group_vars/workstations/composer.yml

# TODO List
  - [x] Clone Code Repos ( this should work correctly if you are forwarding your agent )
    - [x] Sites
    - [x] Ansible
    - [x] Others
  - [ ] Configure Dev Environment
    - [x] Install PHP
    - [x] Install Composer
      - [x] Include valet as a global package
    - [ ] Install MySQL
    - [ ] Install Dependencies
      - [ ] IBM driver
      - [ ] Microsoft Sql Driver
    - [ ] Install NodeJS
  - [ ] Configure Shell
    - [ ] Install Packages
        - [ ] Cargo Packages
        - [ ] Neovim
    - [ ] Change Shell
  - [ ] Configure Kde Plasmas
    - [ ] Update to latest Version
    - [ ] Install Packages

