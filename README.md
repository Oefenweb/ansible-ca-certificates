## ca-certificates

[![CI](https://github.com/Oefenweb/ansible-ca-certificates/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-ca-certificates/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-ca--certificates-blue.svg)](https://galaxy.ansible.com/Oefenweb/ca_certificates)

Manage ca-certificates in Debian-like systems.

#### Requirements

None

#### Variables

* `ca_certificates_certificate_map`: [default: `[]`]: Certificate declarations
* `ca_certificates_certificate_map.{n}.src`: [required]: The local path of the certificate
* `ca_certificates_certificate_map.{n}.dest`: [required]: The remote path of the certificate (relative to `/usr/share/ca-certificates`)

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - ca-certificates
  vars:
    ca_certificates_certificate_map:
      - src: ca-oefenweb-nl.crt
        dest: oefenweb/Oefenweb_nl-B_V.crt
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-ca-certificates/issues)!
