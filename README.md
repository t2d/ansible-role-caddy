galaxy-caddy
============

Install and update Caddy webserver on Debian

Requirements
------------

None

Role Variables
--------------

- caddy_home: home of caddy user
- caddy_logs: logs directory
- caddy_conf: conf directory
- caddy_confd: confd directory
- caddy_www: directory used to store websites sources
- caddy_email: email used to register ACME/Let's Encrypt stuff
- caddy_update: yes/no - activate caddy updates

- test_url: url used for the test page
- test_https: should the test page use https
- test_name: name of the test
- test_code: test page source code directory
- test_www: yes/no - enable redirection from www. to .

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: galaxy-caddy, test_url: test.io }

Run tests
---------

Ensure galaxy-vagrant is up

    ansible-playbook -i tests/inventory tests/test.yml