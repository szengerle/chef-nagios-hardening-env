#chef-nagios-hardening-env
=====================

vagrant testing environment for chef-nagios-hardening


## environment

- vagrant box with ubuntu trusty x64
- used modules: `ntp`,`os-hardening`, `ssh-hardening`, `nagios`
- `nagios`-module installs nagios
- contactgroup, hosttemplate, service, host, users are needed to start nagios
- these nagios objects are configured in data_bags
