# dnsproxy-winsw
Configuration file for using DNSProxy with WinSW

This is a configuration file for using DNSProxy (https://github.com/AdguardTeam/dnsproxy) together with WinSW (https://github.com/winsw/winsw). Thus, DNSProxy gets installed as a service and starts on boot. That way, you can change DNS settings to point to localhost and get to use secure DNS on all of Windows, because (as of June 2024) it still doesn't support DoH or DoT.

The file is set-up with Cloudflare but can be changed to suit your needs. 

This is also useful if you want to use WinSW for other purposes and need a real-life sample to get things working, as it can be convoluted to get started with it.

## Installation instructions

1. Grab a copy of WinSW.

2. Rename its binary to dnsproxyservice.exe and put it into the same directory as dnsproxy.exe

3. Put dnsproxyservice.xml from this repository into the directory too.

4. Run command `dnsproxyservice install` from a prompt inside the directory.

5. Run `dnsproxyservice start` to start the service.

6. On your network settings, set DNS servers to 127.0.0.1 for IPv4 and ::1 for IPv6.
