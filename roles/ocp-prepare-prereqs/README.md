# openshift4-prereqs-prepare

## Pré-requisites

### Prepare workstation
subscription-manager register --username=<rhn_username>
subscription-manager attach --pool=<rhn_pool>
subscription-manager repos --disable='*' \
    --enable=rhel-8-for-x86_64-baseos-rpms \
    --enable=rhel-8-for-x86_64-appstream-rpms
    --enable=ansible-2.8-for-rhel-8-x86_64-rpms  
dnf update -y
reboot
yum install git
yum install ansible

----- 

TODO: 
- VALIDATE PRE-REQS - IN PROGRESS
- VALIDATE LBs
- VALIDATE DHCP (IS IT POSSIBLE?)
- VALIDATE FIREWALL (HOW?)