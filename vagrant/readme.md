# Vagrant IAC

## Description

Vagrant IaC for RHEL 8.

## Assumptions

End-user has functioing Vagrant installation on any Operating System.

## Instructions

1. Start the Vagrant box

    ```bash
    vagrant up
    ```

1. Select desired virtual switch when prompted.

    ```bash
        default: Please choose a switch to attach to your Hyper-V instance.
        default: If none of these are appropriate, please open the Hyper-V manager
        default: to create a new virtual switch.
        default:
        default: 1) External VSwitch
        default: 2) Default Switch
        default: 3) WSL
        default:
        default: What switch would you like to use?
    ```

    Note: Using Git-Bash, the External VSwitch option seemed to be the only one that worked and allowed connectivity from my WSL installation.

1. Get any Network information

    ```bash
    vagrant ssh-config
    ```

1. Connect to Vagrant Box

    ```bash
    vagrant ssh
    ```

## Reference

- `https://www.vagrantup.com/docs/providers/hyperv/limitations`
- `https://docs.microsoft.com/en-us/virtualization/community/team-blog/2017/20170706-vagrant-and-hyper-v-tips-and-tricks`
