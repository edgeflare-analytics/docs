# Tools Included In The Free Plan




## ICMP Ping (Free Version):
- Grants access to 6 ICMP Probes @ 0.5 second intervals.

### Full Request:
```json
{
    "apiKey": "YOUR_API_KEY",
    "toolType": "pingFree",
    "host": "1.1.1.1"
}
```

### Full Return:
```json
{
    "args": {
        "host": "1.1.1.1"
    },
    "authed": true,
    "error": null,
    "result": {
        "probes": [
            "64 bytes from 1.1.1.1: icmp_seq=1 ttl=60 time=8.15 ms",
            "64 bytes from 1.1.1.1: icmp_seq=2 ttl=60 time=6.64 ms",
            "64 bytes from 1.1.1.1: icmp_seq=3 ttl=60 time=7.49 ms",
            "64 bytes from 1.1.1.1: icmp_seq=4 ttl=60 time=7.57 ms",
            "64 bytes from 1.1.1.1: icmp_seq=5 ttl=60 time=7.62 ms",
            "64 bytes from 1.1.1.1: icmp_seq=6 ttl=60 time=6.86 ms"
        ],
        "stats": [
            "6 packets transmitted, 6 received, 0% packet loss, time 2510ms"
        ]
    },
    "success": true,
    "toolType": "pingFree",
    "userType": "free"
}
```

----

## NMAP LITE (Free Version):
- Grants access to fast NMAP scan (LITE). Scans top 100 ports.

### Full Request:
```json
{
    "apiKey": "YOUR_API_KEY",
    "toolType": "nampFree",
    "host": "1.1.1.1"
}
```

### Full Return:
```json
{
    "args": {
        "host": "1.1.1.1"
    },
    "authed": true,
    "error": null,
    "result": {
        "info": [
            "Starting Nmap 6.40 ( http://nmap.org ) at 2020-10-16 09:29 CEST",
            "Nmap scan report for one.one.one.one (1.1.1.1)",
            "Host is up (1.0s latency).",
            "Not shown: 89 closed ports",
            "Nmap done: 1 IP address (1 host up) scanned in 9.90 seconds"
        ],
        "ports": [
            {
                "port": "21/tcp",
                "service": "ftp",
                "state": "filtered"
            },
            {
                "port": "22/tcp",
                "service": "ssh",
                "state": "filtered"
            },
            {
                "port": "25/tcp",
                "service": "smtp",
                "state": "filtered"
            },
            {
                "port": "53/tcp",
                "service": "domain",
                "state": "open"
            },
            {
                "port": "80/tcp",
                "service": "http",
                "state": "open"
            },
            {
                "port": "110/tcp",
                "service": "pop3",
                "state": "filtered"
            },
            {
                "port": "113/tcp",
                "service": "ident",
                "state": "filtered"
            },
            {
                "port": "443/tcp",
                "service": "https",
                "state": "open"
            },
            {
                "port": "587/tcp",
                "service": "submission",
                "state": "filtered"
            },
            {
                "port": "993/tcp",
                "service": "imaps",
                "state": "filtered"
            },
            {
                "port": "995/tcp",
                "service": "pop3s",
                "state": "filtered"
            }
        ]
    },
    "success": true,
    "toolType": "nmapFree",
    "userType": "free"
}
```
