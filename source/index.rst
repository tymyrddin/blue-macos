Hardening macOS
================================================

Version 0.1: These mitigations are all based on Catalina. Supposedly, `Big Sur has better security <https://www.endpointprotector.com/blog/macos-11-0-big-sur-security-and-privacy-changes-you-need-to-know/>`_. Some of the below is still applicable and useful. When we have a Big Sur set up we will test it, and split and update these mitigations.

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Authentication

   docs/authentication/README.md
   docs/authentication/login.md
   docs/authentication/resuming.md
   docs/authentication/passwords.md
   docs/authentication/password-manager.md
   docs/authentication/mfa.md
   docs/authentication//ssh-mfa.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Services and applications

   docs/services/README.md
   docs/services/restrict-apps.md
   docs/services/sip.md
   docs/services/browsers.md
   docs/services/messaging.md
   docs/services/email-services.md
   docs/services/ssh.md
   docs/services/vpn.md
   docs/services/vpn-fail-open.md
   docs/services/dns-servers.md
   docs/services/tor-proxy.md
   docs/services/change-mac.md
   docs/services/renew-lease.md
   docs/services/edit-hosts-file.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Data

   docs/data/README.md
   docs/data/time-machine.md
   docs/data/disk-encryption.md
   docs/data/pwprotect.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Privacy

   docs/privacy/README.md
   docs/privacy/settings.md
   docs/privacy/metadata.md
   docs/privacy/metadata-images.md
   docs/privacy/hexeditors.md
   docs/privacy/bleachbit.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Malware

   docs/malware/README.md
   docs/malware/myths.md
   docs/malware/clean-machine.md
   docs/malware/daemons-and-agents.md
   docs/malware/analysing-trojans.md

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Operations security

   docs/opsec/README.md
   docs/opsec/email-use.md
   docs/opsec/check-mail.md
   docs/opsec/browsing.md
   docs/opsec/integrity-downloads.md
   docs/opsec/*

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: Guards! Guards!

   docs/guards/README.md
   docs/guards/soup.md
   docs/guards/ids.md
   docs/guards/*

.. toctree::
   :caption: Links

   Blue Team <https://blue.tymyrddin.dev/>
