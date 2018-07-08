# DNS

## Missing DNS servers first-aid

+ IP resolutions lists
  + google.com 74.125.205.113
  + wikipedia.org 91.198.174.192
  + github.com 192.30.253.112
  + colabo.space 78.46.175.184
  + facebook.com 185.60.216.35
  + youtube.com 64.233.162.190
  + ebay.com 66.211.181.123
  + paypal.com 64.4.250.33
  + vpn.umu.se 130.239.0.246
  + vpn.uio.no 129.240.0.86
  + vpn2.uio.no 129.240.0.83

### Public DNS

+ Google 
  + https://en.wikipedia.org/wiki/Google_Public_DNS
  + https://developers.google.com/speed/public-dns/docs/using
  + https://developers.google.com/speed/public-dns/docs/using#testing
  + http://216.218.228.119/

If you want to use **Google’s DNS servers**, you can add the following two items to the list:

8.8.8.8
8.8.4.4

If you’d rather use **OpenDNS** instead, which has lots of extra features, you can use the following two entries:

208.67.222.222
208.67.220.220

### List DNSes

https://superuser.com/questions/258151/how-do-i-check-what-dns-server-im-using-on-mac-os-x

```sh
scutil --dns | grep 'nameserver[[0-9]*]'
networksetup -getdnsservers Wi-Fi
networksetup -getdnsservers Ethernet
```

+ https://support.apple.com/kb/PH25354?locale=en_US&viewlocale=en_US
+ http://kb.mit.edu/confluence/display/istcontrib/How+to+check+DNS+settings+on+Mac+OS+X+10.7
+ http://osxdaily.com/2011/06/03/get-dns-server-ip-command-line-mac-os-x/

# Sharing local server

+ [DNSdynamic](https://www.dnsdynamic.org/?host=colabo&domain=1)
+ noip.com
  + [Free Dynamic DNS : Getting Started Guide](https://www.noip.com/support/knowledgebase/getting-started-with-no-ip-com/)
  + https://www.noip.com/sign-up
  + https://www.noip.com/download?page=mac

# cURL command

### SPARQL (POST) example

+ ***`—data-urlencode`*** - uses HTTP **POST** verb, but it also **encodes** the data following the parameter. data should be **CGI-compliant** (name=value), in our example it is: `query='…'`
+ ***`-G`*** - this command **compensates** the switching to the POST verb effect of the command the `—data-urlencode`, and therefore the GET verb will be used instead and the `name=value` data will be appended to the URL with ***`?`*** separator (or ***`&`*** separator of not the first and only data)
  + NOTE: using the `-G` option is option-al :) = we will get proper response from the SPARQL endpoint
+ ***`—header`*** - provides additional HTTP headers
  + NOTE: you can ask either for XML
    + `Accept: application/sparql-results+xml`
  + or JSON
    + `Accept: application/sparql-results+json`
  + Extra info:
    + https://www.w3.org/TR/rdf-sparql-XMLres/
    + https://www.w3.org/2001/03mr/rdf_mt
      + `application/rdf+xml`


```sh
# SPARQL classes
curl --header "Accept: application/sparql-results+json"  -G  'http://fdbsun1.cs.umu.se:3030/demo3models/query' --data-urlencode query='prefix owl: <http://www.w3.org/2002/07/owl#> prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> SELECT DISTINCT ?class ?label ?description WHERE {  ?class a owl:Class.  OPTIONAL { ?class rdfs:label ?label}  OPTIONAL { ?class rdfs:comment ?description}}'

# SPARQL data
curl --header "Accept: application/sparql-results+json"  -G  'http://fdbsun1.cs.umu.se:3030/demo3models/query' --data-urlencode query='prefix owl: <http://www.w3.org/2002/07/owl#> prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> SELECT DISTINCT ?subject ?predicate ?object WHERE {?subject ?predicate ?object} LIMIT 100'
```

