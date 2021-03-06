# Docker Template: ngircd

This docker template provides the 'ngircd' IRC Daemon on port 6667. This port is used downstream by the IRC Bouncer 'znc'. Since the 'znc' exposes the secure port '6697' (SSL) to external IRC clients, the 'ngircd' container does not expose 6697 (even though it is configured).

## Website
http://ngircd.barton.de

## Dependendy
### Downstream
`znc` 
`kiwiirc`

## (Re)Building the image
`./build.sh <userid>`

## Running the image
`docker run -d --name ngircd -p 6667:6667 <userid>/ngircd`

## Adding user authentication
See https://pragmasec.wordpress.com/2014/07/12/set-up-a-secure-and-easy-irc-server-with-ssl-and-pam-authentication-using-crypt-salted-passwords/ for enabling PAM.
See http://www.debiantutorials.com/installing-vsftpd-using-text-file-for-virtual-users/ for using 'htpassword'.