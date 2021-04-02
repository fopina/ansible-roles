This role will fetch cloudflare IP ranges and add them to iptables, `DROP`ping everything else.

It uses the `DOCKER-USER` chain as this one overrides the normal `INPUT` one

**blocking IPs in `INPUT` when docker is managing iptables does not block anything at all**

It accepts `iptables_extra_input` and `iptables_extra_udp_input` variables for additional allowed ranges.

TODO:
* make the *docker oriented* setup optional / configurable
* support ipv6?
