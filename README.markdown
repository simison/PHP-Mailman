 php_mailman
===========

This is just a basic skeleton to send some most used commands to Mailman.
You shouldn't echo functions out, because cURL returns an admin view.
Though you can use something like [Simple HTML DOM](http://simplehtmldom.sourceforge.net/) 
to get some feedback from this class. Use at your own risk, though.


## You can

* Subscribe
* Unsubscribe
* Set digest
* List a member
* List lists
 

## Howto

* Construct

`require_once('php_mailman.php');'
'$mailman = new php_mailman('domain.com', 'password', 'listname_domain.com');`


* Subscribe

`$mailman->subscribe('email@address.com');`


* Unsubscribe

`$mailman->unsubscribe('email@address.com');`


* Subscribe

`$mailman->digest('email@address.com');`


* Subscribe

`$mailman->list_member('email@address.com');`


* Subscribe

`$mailman->list_lists();`


* Re-set settings

`$mailman->set_domain('domain.com');'
'$mailman->set_adminpasswd('password');'
'$mailman->set_listname('listname_domain.com');'
'$mailman->set_protocol('https');'
'$mailman->set_listlanguage('fi'); // shortcode (en, de, etc...)'
'$mailman->set_notifyowner('1'); // 1 = yes | 0 = no'
'$mailman->set_notifyuser('1'); // 1 = yes | 0 = no'
'$mailman->set_digest('1'); // 1 = yes | 0 = no`'

Or you can set all these on start:

`$mailman = new php_mailman($domain, $adminpasswd, $listname, $protocol, $listlanguage, $notifyowner, $notifyuser, $digest);`


## Read more

Mailman Wiki: [Additional web administration tools?](http://wiki.list.org/pages/viewpage.action?pageId=4030567)