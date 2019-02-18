[![Docker Stars](https://img.shields.io/docker/stars/malaiwah/bind.svg)](https://hub.docker.com/r/malaiwah/bind/) [![Docker Pulls](https://img.shields.io/docker/pulls/malaiwah/bind.svg)](https://hub.docker.com/r/malaiwah/bind/)
# BIND on Alpine
[![](https://images.microbadger.com/badges/version/malaiwah/bind.svg)](https://microbadger.com/images/malaiwah/bind "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/malaiwah/bind.svg)](https://microbadger.com/images/malaiwah/bind "Get your own image badge on microbadger.com")

### Running

Use this command to start the container. Unbound will listen on port 53/udp.

`docker run --name bind -d -p 53:53/udp -p 53:53 malaiwah/bind`

________________________________________

### Configuration
**Parameters:**

WORK-IN-PROGRESS

* `-e DO_IPV6` Enable or disable ipv6. (Default: "yes", Possible Values: "yes, no")
* `-e DO_IPV4` Enable or disable ipv4. (Default: "yes", Possible Values: "yes, no")
* `-e DO_UDP` Enable or disable udp. (Default: "yes", Possible Values: "yes, no")
* `-e DO_TCP` Enable or disable tcp. (Default: "yes", Possible Values: "yes, no")
* `-e VERBOSITY` Verbosity number, 0 is least verbose. (Default: "0", Possible Values: "<integer>")
* `-e SO_RCVBUFF` Buffer size for UDP port 53 incoming. (Default: "0", Possible Values: "<integer>")
* `-e SO_SNDBUF` Buffer size for UDP port 53 outgoing. (Default: "0", Possible Values: "<integer>")
* `-e SO_REUSEPORT` Use SO_REUSEPORT to distribute queries over threads. (Default: "no", Possible Values: "yes, no")
* `-e EDNS_BUFFER_SIZE` EDNS reassembly buffer to advertise to UDP peers. (Default: "4096", Possible Values: "<integer>")
* `-e MSG_CACHE_SIZE` The amount of memory to use for the message cache. Plain value in bytes or you can append k, m or G. (Default: "4m", Possible Values: "<integer>")
* `-e RRSET_CACHE_SIZE` The amount of memory to use for the RRset cache. Plain value in bytes or you can append k, m or G. (Default: "4m", Possible Values: "<integer>")
* `-e CACHE_MIN_TTL` The time to live (TTL) value lower bound, in seconds. (Default: "0", Possible Values: "<integer>")
* `-e CACHE_MAX_TTL` The time to live (TTL) value cap for RRsets and messages in the cache. Items are not cached for longer. In seconds. (Default: "86400", Possible Values: "<integer>")
* `-e CACHE_MAX_NEGATIVE_TTL` The time to live (TTL) value cap for negative responses in the cache. (Default: "3600", Possible Values: "<integer>")
* `-e HIDE_IDENTITY` Enable to not answer id.server and hostname.bind queries. (Default: "no", Possible Values: "yes, no")
* `-e HIDE_VERSION` Enable to not answer version.server and version.bind queries. (Default: "no", Possible Values: "yes, no")
* `-e DNSSEC_VALIDATOR` Enable DNSSEC validation. (Default: "no", Possible Values: "yes, no")
* `-e DNSSEC_VERBOSITY` Enable Unbound DNSSEC validation verbose logging. (Default: "0", Possible Values: "0, 1, 2")

### Original idea

* https://hub.docker.com/r/safelinkinternet/unbound/
