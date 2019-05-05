# Ansible Role: Secure SSH

[![Build Status](https://travis-ci.org/dsgnr/ansible-role-secure-ssh.svg?branch=master)](https://travis-ci.org/dsgnr/ansible-role-secure-ssh)
[![Build Status](https://jenkins.handsoff.cloud/buildStatus/icon?job=ansible-role-secure-ssh%2Fmaster)](https://jenkins.handsoff.cloud/job/ansible-role-secure-ssh/job/master/)

This role makes some basic changes to SSH to make it more secure

## Requirements

None.

## Role Variables

None.

## Dependencies

None.

## Example Playbook

    - hosts: all
      become: true

      roles:
        - secure-ssh

## License

GNUv3

## Author Information

This role was created by [Dan Hand](https://danielhand.io).

