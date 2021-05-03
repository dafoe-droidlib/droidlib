Droidlib makes better , optimized and fast network operations such as http requests, ICMP and DNS requests.
You can see examples below:
--------------------------------------------------------------------------------
$ python3

>> from droidlib import *
>> mySimpleHTTP = http_get("https://example.com") # http_get(url) , sends http get request
>> print(mySimpleHTTP.status_code)
200
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
>> mySimpleICMP = icmp_echo("google.com",1,1,10) # icmp_echo(domain,count,bytes,timeout) , icmp echo request
>> print(mySimpleICMP.response) # response -> (array), [loss,ip]
[0,216.239.38.120]
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
>> mySimpleDNS = dns_a("google.com") # dns_a(domain) , dns request replies A response
>> print(mySimpleDNS.response)
[216.239.38.120]
