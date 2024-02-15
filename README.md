# Ansible for switching PiVPN and 3X-UI configurations
Fast multiple configurations switching (enable/disable) for PiVPN and 3X-UI.

## Prerequisites
You should have at least one server with allowed SSH connection with installed pivpn or 3x-ui panels.

## Usage
1. Install Ansible according to the [official instructions](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#pip-install).
2. Install git according to the [official instructions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
3. Download the repository to your computer: `git clone https://github.com/exmanka/ksiVPN-ansible-pivpn-3xui.git`
4. Move to project directory: `cd ksiVPN-ansible-pivpn-3xui`
5. Add your servers to file `hosts` according to template in file.
6. Run playbook for pivpn on servers (3x-ui will be added later): `ansible-playbook pivpn-switch.yml -e "client=<client> state=<state>"`
7. Replace:  
   `<client>` — unique set of characters for desired group of configurations.  
   For example, you want to turn on/off only `pc_KSIVA` and `sp_KSIVA` configurations of many avaiable: `pc_Masheb4ka`, `sp_Egor`, `test`, `pc_KSIVA`, `sp_KSIVA`. You can pass `KSIVA` or `ksi`.
   
   `<state>` — `-on` to enable desired group of configurations, `-off` to disable desired group of configurations.

## About ksiVPN project
🔥 __ksiVPN__ — an open source student project that has become something more not only for its creator, but also for most customers .Thanks to hard work, the use of basic modern protocols and competent server rental, the project is able to provide the highest quality VPN connection for the minimum cost.  
### ksiVPN uses the following open-source solutions:
- [pivpn](https://github.com/pivpn/pivpn)
- [3x-ui](https://github.com/MHSanaei/3x-ui)
- [nekoray](https://github.com/MatsuriDayo/nekoray)
- [v2rayNG](https://github.com/2dust/v2rayNG)
