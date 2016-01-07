# /etc/shadow

[Ref](http://www.cyberciti.biz/faq/where-are-the-passwords-of-the-users-located-in-linux/)

where encrypted password is saved.

## Fields:

Login name
Encrypted password
Days since Jan 1, 1970 that password was last changed
Days before password may be changed
Days after which password must be changed
Days before password is to expire that user is warned
Days after password expires that account is disabled
Days since Jan 1, 1970 that account is disabled

## Encrypted password

[Ref](http://stackoverflow.com/questions/12660851/which-is-the-encryption-method-used-on-etc-shadow)

Crypted using 'crypt(3)' function. On glibc, the method used depends on the salt, if it starts with:

$1$: it uses MD5.
$5$: it uses SHA-256.
$6$: it uses SHA-512.
$2a$: it uses blowfish, not supported everywhere.
Otherwise it uses DES.

## Generate a password

[Ref](http://serverfault.com/questions/259722/how-to-generate-a-etc-shadow-compatible-password-for-ubuntu-10-04)

```
apt-get install whois
mkpasswd -m sha-512
```
