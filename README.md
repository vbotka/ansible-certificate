# certificate

[![quality](https://img.shields.io/ansible/quality/27910)](https://galaxy.ansible.com/vbotka/certificate)[![Build Status](https://travis-ci.org/vbotka/ansible-certificate.svg?branch=master)](https://travis-ci.org/vbotka/ansible-certificate)

[Ansible role](https://galaxy.ansible.com/vbotka/certificate/). Manage SSL certificates.

Feel free to [share your feedback and report issues](https://github.com/vbotka/ansible-certificate/issues).

[Contributions are welcome](https://github.com/firstcontributions/first-contributions).


## Tested providers

Tested providers: selfsigned
Not tested yet: acme, entrust, ownca


## Requirements and dependencies

### Roles

- [ansible_lib](https://galaxy.ansible.com/vbotka/ansible_lib) library of Ansible tasks.

### Collections

- [community.crypto](https://galaxy.ansible.com/community/crypto)

### Packages

- [cryptography](https://cryptography.io/en/latest/)
- [openssl](https://www.openssl.org/)
- [acme-tiny](https://pypi.org/project/acme-tiny/)


## Role Variables

- review default variables in *defaults/main.yml*
- review OS specific variables in *vars/defaults/*
- review examples in *vars/main.yml*


## Workflow

- Install the role and required dependencies

- Create playbook

```
shell> cat playbook.yml
- hosts: srv.example.com
  roles:
    - vbotka.certificate
```

- Display help

```
shell> ansible-playbook playbook.yml
```

- Run setup tasks

```
shell> ansible-playbook playbook.yml -t certificate_debug
shell> ansible-playbook playbook.yml -t certificate_packages
shell> ansible-playbook playbook.yml -t certificate_sanity
shell> ansible-playbook playbook.yml -t certificate_dirs
```

- Optionaly generate a self signed OpenSSL certificates by openssl command

```
shell> ansible-playbook playbook.yml -t certificate_command
```

- Optionaly generate private keys, CSRs, and certificates step-by-step

```
shell> ansible-playbook playbook.yml -t certificate_openssl_privatekey
shell> ansible-playbook playbook.yml -t certificate_openssl_csr
shell> ansible-playbook playbook.yml -t certificate_openssl_certificate
```

- Optionaly generate private keys, CSRs, and certificates in one step

```
shell> ansible-playbook playbook.yml -t certificate_openssl
```

- Optionaly display information on OpenSSL private keys, CSRs, and dectificates

```
shell> ansible-playbook playbook.yml -t certificate_openssl_privatekey_info
shell> ansible-playbook playbook.yml -t certificate_openssl_csr_info
shell> ansible-playbook playbook.yml -t certificate_openssl_certificate_info
```

- Optionaly display status of files OpenSSL private keys, CSRs, and certificates

```
shell> ansible-playbook playbook.yml -t certificate_openssl_stat
```


## References

- [PKCS#10 certificate request and certificate generating utility](https://www.openssl.org/docs/man1.0.2/apps/openssl-req.html)
- [SSL and TLS Deployment Best Practices](https://github.com/ssllabs/research/wiki/SSL-and-TLS-Deployment-Best-Practices)
- [SSL Best Practices: a Quick and Dirty](https://www.ssl.com/guide/ssl-best-practices-a-quick-and-dirty-guide/)
- [ACME Protocol Updates](https://letsencrypt.org/docs/acme-protocol-updates/)
- [ACME RFC8555 8.Identifier Validation Challenges](https://tools.ietf.org/html/rfc8555#section-8)
- [ACME-TLS-ALPN Draft 3.TLS with Application Level Protocol Negotiation (TLS ALPN) Challenge](https://tools.ietf.org/html/draft-ietf-acme-tls-alpn-05#section-3)


## License

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)


## Author Information

[Vladimir Botka](https://botka.link)
