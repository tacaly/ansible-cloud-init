# ansible-cloud-init

An [Ansible](https://www.ansible.com) - [cloud-init](http://cloud-init.org/)

## Requirements

Install cloud init "yum -y install cloud-init"

Note:
CentOS 6x on GCE: We have observed intermittent issues with the CentOS 6.x native version of cloud-init (cloud-init-0.7.5-10.el6.centos.2.src.rpm) hanging prior to our userdata script being executed. The suggested workaround for this is to use the RHEL version of cloud-init cloud-init-0.7.5-2.el6.src.rpm. To rebuild where epel can not update:

"rpm -Uvh cloud-init-0.7.5-2.el6.src.rpm
  sed -i.orig -e 's/2%{?dist}/20%{?dist}/g' ~/rpmbuild/SPECS/cloud-init.spec
  rpmbuild -ba ~/rpmbuild/SPECS/cloud-init.spec
  rpm -Uvh ~/rpmbuild/RPMS/x86_64/cloud-init-0.7.5-20.el6.x86_64.rpm
  rm -fr ~/rpmbuild"

## Role Variables

[defaults/main.yml](defaults/main.yml)

## Dependencies

## Example Playbook

## License

MIT

## Author Information
 -Daniils Avdejevs

