General

* https://developers.google.com/speed/public-dns/docs/performance discusses the topic from the web browser perspective and includes practical suggestions for improving performance
* http://opentodo.net/2012/09/monitoring-dns-queries-with-bindgraph/ shows one way to monitor BIND performance 
* http://packetnexus.com/2010/12/how-to-install-djbs-dnscache-on-ubuntu-10-10/ is how we setup dnscache.  Making the `/service` directory and symlinking into it is not needed.  `/etc/service` seems to be the directory used by Ubuntu's djb packages.

Tools

* https://code.google.com/p/namebench/

Similar test results

* http://www.dnssec-deployment.org/index.php/tag/dnssec/ shows a home WAP doing 700 queries per second
* http://nms.lcs.mit.edu/papers/dns-ton2002.pdf
