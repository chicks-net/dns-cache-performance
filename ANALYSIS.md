DNS cache performance analysis
==============================

Introduction
------------

DNS caching can improve performance for web services.  If you are interested
in minimizing latency you may want a DNS cache on every server in your infrastructure.
I tested the 3 top DNS servers to find the fastest server.


Hypothesis
----------

dnsmasq is simpler than BIND and will perform better since dnsmasq does not have DNSSEC or other advanced
BIND features.


Testing Methodology
-------------------

* do 10 consecutive iterations of namebench with 100 threads and 3000 lookups
* the results are all included in https://github.com/chicks-net/dns-cache-performance/test-results
* the configurations used are all included in https://github.com/chicks-net/dns-cache-performance/configs

dnsmasq
-------

The configuration seems simple.  It works out of the box without any lines of configuration.  For DNS caching
there are only a couple of options.  Looking deeper the configuration options reveal that dnsmasq has a
built-in DHCP and TFTP server.  This certainly contrasts

dnscache
--------

This is another product from the controversial `djb`.  Some love his `supervise` suite of tools.  Others,
such as this author, would rather avoid them forever.  It turns out that BIND performs better so we did not
have to worry about using it.

BIND
----

It just rocks.

Conclusion
----------

BIND is faster.  It has more features too.  Use it with no worries.
