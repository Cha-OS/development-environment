google.com 74.125.205.113
wikipedia.org 91.198.174.192
github.com 192.30.253.112
colabo.space 78.46.175.184
facebook.com 185.60.216.35
youtube.com 64.233.162.190
ebay.com 66.211.181.123
paypal.com 64.4.250.33
vpn.umu.se 130.239.0.246
vpn.uio.no 129.240.0.86
vpn2.uio.no 129.240.0.83

https://en.wikipedia.org/wiki/Google_Public_DNS

https://developers.google.com/speed/public-dns/docs/using
https://developers.google.com/speed/public-dns/docs/using#testing
 http://216.218.228.119/
If you want to use Google’s DNS servers, you can add the following two items to the list:

8.8.8.8
8.8.4.4
If you’d rather use OpenDNS instead, which has lots of extra features, you can use the following two entries:

208.67.222.222
208.67.220.220

List DNSes
https://superuser.com/questions/258151/how-do-i-check-what-dns-server-im-using-on-mac-os-x
scutil --dns | grep 'nameserver\[[0-9]*\]'
networksetup -getdnsservers Wi-Fi
networksetup -getdnsservers Ethernet