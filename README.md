# ApacheDS test

Run:

	vagrant plugin install vagrant-vbguest
	vagrant up

and enjoy ApacheDS on ports 10389 and 10636.

To connect use DN `uid=admin,ou=system` with password `secret`, as stated by the [manual](https://directory.apache.org/apacheds/basic-ug/1.4.2-changing-admin-password.html).
