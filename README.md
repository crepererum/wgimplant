# wgimplant

Re-routes all traffic of network local host over a [WireGuard](https://www.wireguard.com/) VPN.

**IPv6: This script currently is IPv4-only. You may want to disable IPv6 in your router-settings so that the victim
cannot bypass the tunnel.**

## Use Cases
For devices where WireGuard does not run on (e.g. TVs):

- Security Protections
- Traffic Shaping
- Watch other countries content

## Usage
Place a `wg-quick`-compatible config in `wg.conf`.

You are going to need the IP address of the victim. You can use your router interface or some scanning tools to find
that out. It can be helpful to change the router settings to always assign the same IP address to the victim.

```
./wgimplant <VICIM_IP>
```

`wgimplant` will now auto-detect certain parameters and print them. Press any key to confirm. The tunnel should be
established after a few seconds.

Now, the victim should be routed through the WireGuard VPN. You can check this using
[whatismyipaddress.com](https://whatismyipaddress.com/).

Hit `CTRL-C` to stop the implant.
