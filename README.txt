Droidlib makes better , optimized and fast network operations such as http requests, ICMP and DNS requests.
You can see examples below:
--------------------------------------------------------------------------------
$ python3

>> from droidlib import http
>> mySimpleHTTP = http.get("https://example.com") # http.get(url) , sends http get request
>> print(mySimpleHTTP.status) # response -> (array), [status_code,title]
[200,'Example Domain']
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
>> from droidlib import icmp
>> mySimpleICMP = icmp.echo("google.com",1,1,10) # icmp.echo(domain,count,bytes,timeout) , icmp echo request
>> print(mySimpleICMP.response) # response -> (array), [loss,ip]
[0,216.239.38.120]
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
>> from droidlib import dns
>> mySimpleDNS = dns.a("google.com") # dns.a(domain) , dns request replies A response
>> print(mySimpleDNS.response)
[216.239.38.120]
