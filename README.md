# AnsibleRole_LetsEncrypt
creates a LetsEncrypt cert using the Ansible local host. 

Role designed to create or renew a LetEncrypt cert using the Ansible local host. Cert can then be copied to the desired endpoints.

Supply the following VARS for the role..

  vars:
    path: ansible_dir
    acme_directory: https://acme-v02.api.letsencrypt.org/directory # prod
    #acme_directory: https://acme-staging-v02.api.letsencrypt.org/directory # USE FOR TESTING ONLY
    certificate_binding:
        hostname: "*.hostname.co.uk"
        cloudflare_zone: hostname.co.uk
        friendly_name: "star.hostname.co.uk"
    organization_name: "Org name"
    email: "email address"
