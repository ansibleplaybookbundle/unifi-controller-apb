unifi-controller-apb
=========

Deploy the Ubiquity UniFi Controller with either ephemeral or persistent
storage.

Intended to be consumed as an [Ansible Playbook
Bundle](http://automationbroker.io).

unifi-controller-apb variables
--------------

    app_name: "unifi-ctrl-apb-{{ _apb_service_instance_id.split('-')[0] }}"

Default application name when provisioning objects. Make sure this name does
not exceed 63 chars (less 18 characters if using GlusterFS due to persistent
volume dynamic name creation).

    app_image: docker.io/jacobalberty/unifi:5.8.30

Container image and version to deploy. Image provided by Jacob Alberty.

    namespace: "{{ lookup('env','NAMESPACE') | default('unifi', true) }}"

Namespace the application will be deployed to.

License
-------

Apache v2.0

Author Information
------------------

Leif Madsen (leif at leifmadsen dot com)
