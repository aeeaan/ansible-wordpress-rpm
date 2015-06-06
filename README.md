correcthorse.wordpress
=========

An ansible role for installing wordpress. This role is currently incomplete and very experimental. I may start from scratch using wp-cli to manage the installation.

Role Variables
--------------

| Variable				| Default							| Notes		 |
| :---					| :---								| :---		 |
| wordpress_version			| 4.1.1								|		 |
| wordpress_home			| /var/www/wordpress						|		 |
| wordpress_user			| wordpress							|		 |
| wordpress_create_user			| true								|		 |
| wordpress_download_base		| https://wordpress.org/					|		 |
| wordpress_base_name			| "wordpress-{{ wordpress_version }}"				|		 |
| wordpress_extracted_name		| wordpress			  				|		 |
| wordpress_archive			| "{{ wordpress_base_name }}.tar.gz"			 	|		 |
| wordpress_download_url		| "{{ wordpress_download_base }}{{ wordpress_archive }}" 	|		 |
| wordpress_db_name			| wordpress		      	   		     		|		 |
| wordpress_db_user			| wordpress							|		 |
| wordpress_db_password			| wordpress							|		 |
| wordpress_db_host			| localhost							|		 |
| wordpress_db_charset			| utf8								|		 |
| wordpress_db_collate			| ''								|		 |
| wordpress_auth_key			| ''								|		 |
| wordpress_secure_auth_key		| ''								|		 |
| wordpress_logged_in_key		| ''								|		 |
| wordpress_nonce_key			| ''								|		 |
| wordpress_auth_salt			| ''								|		 |
| wordpress_secure_auth_salt		| ''								|		 |
| wordpress_logged_in_salt		| ''								|		 |
| wordpress_nonce_salt			| ''								|		 |
| wordpress_cache			| true								|		 |
| wordpress_permalinks			| true								|		 |


List of files to keep outside the application that shouldn't change with upgrades. Symlinks are created to these files inside the application.

    wordpress_shared_links:
      - .htaccess
      - wp-config.php
      - wp-content/uploads
      - wp-content/cache
      - wp-content/w3tc-config



Dependencies
------------

correcthorse.php
correcthorse.app

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: correcthorse.wordpress }

License
-------

MIT

Author Information
------------------

* [Joshua Rusch](https://correct.horse/)
