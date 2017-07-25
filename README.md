# using-proxies

Some of programmers cannot even download some free packages because of their country.
they watch a video about a programming course and 
when they want to try the same thing they will give an strange error
so some of them give it up and some of them try to use proxies 
but they should set proxies for every package manager(apt, npm, bower).

This article tries to help this problem.

To use a proxy, you need a http proxy server. 
The IP and port have to be from this proxy server.
using socks proxies, is more complex because you would depend on more tools such as [shadowsocks](https://shadowsocks.org),[proxychains](https://github.com/rofl0r/proxychains-ng).

## set proxy for apt-get
use the following command

`Acquire::http::Proxy "http://yourproxyaddress:proxyport";`

and to use a http-proxy permanently

sudo gedit /etc/apt/apt.conf
and add this line to your /etc/apt/apt.conf file

`Acquire::http::Proxy "http://yourproxyaddress:proxyport";`

or

`Acquire::http::Proxy ""http://username:password@yourproxyaddress:proxyport";";`

## set proxy for npm 
`npm config set proxy "http://domain\username:password@servername:port/"`

`npm config set https-proxy "http://domain\username:password@servername:port/"`