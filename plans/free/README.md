# Tools Included In Free Plan


## ICMP Ping (Free Version):
- Grants access to 6 ICMP Probes @ 0.5 second intervals.

## Full Request:
```json
{
    "apiKey": "YOUR_API_KEY",
    "toolType": "pingFree",
    "host": "1.1.1.1"
}
```

## Full Return:
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



