# Basic documentation regarding our free API

## Base Endpoint:
`https://api.edgeflare.io/`

## Allowed Request Methods:
`POST`

### For Enterprise/moderate scanning, refer to our enterprise API documentation. (*Coming Soon*)


## Basic Request: 
- Example: ICMP Ping (free):

### JSON Request
```json
{
    "apiKey": "YOUR_API_KEY",
    "toolType": "pingFree",
    "host": "1.1.1.1"
}
```

### JSON Response:
```json
{
    "args": {
        "host": "google.com"
    },
    "authed": true,
    "error": "",
    "planInfo": [
        "Add dictionary argument: '{..., \"planInfo\": \"1\"}' to get stats about plan when making requests!"       
    ],
    "result": {
        "probes": [
            "64 bytes from lga15s48-in-f206.1e100.net (172.217.4.206): icmp_seq=1 ttl=118 time=21.2 ms",
            "64 bytes from lga15s48-in-f206.1e100.net (172.217.4.206): icmp_seq=2 ttl=118 time=20.8 ms",
            "64 bytes from lga15s48-in-f206.1e100.net (172.217.4.206): icmp_seq=3 ttl=118 time=21.1 ms",
            "64 bytes from lga15s48-in-f206.1e100.net (172.217.4.206): icmp_seq=4 ttl=118 time=20.7 ms",
            "64 bytes from lga15s48-in-f206.1e100.net (172.217.4.206): icmp_seq=5 ttl=118 time=20.8 ms",
            "64 bytes from lga15s48-in-f206.1e100.net (172.217.4.206): icmp_seq=6 ttl=118 time=21.2 ms"
        ],
        "stats": [
            "6 packets transmitted, 6 received, 0% packet loss, time 2505ms"
        ]
    },
    "success": true,
    "toolType": "pingFree",
    "userType": "free"
}
```

----

## Advanced Request: 
-example: ICMP Ping (free + plan info):

### JSON Request
```json
{
    "apiKey": "YOUR_API_KEY",
    "toolType": "pingFree",
    "host": "google.com",
    "planInfo": "1"
}
```

### JSON Response:
```json
{
    "args": {
        "host": "google.com"
    },
    "authed": true,
    "error": "",
    "planInfo": {
        "planAllowances": {
            "enterprise": {
                "enterpriseModuleRequestAllowance": 0,
                "enterpriseRequestsLeftThisMonth": 0,
                "enterpriseRequestsThisMonth": 0
            },
            "free": {
                "freeModuleRequestAllowance": 150,
                "freeRequestsLeftThisMonth": 110,
                "freeRequestsThisMonth": 40
            },
            "moderate": {
                "moderateModuleRequestAllowance": 0,
                "moderateRequestsLeftThisMonth": 0,
                "moderateRequestsThisMonth": 0
            },
            "regular": {
                "regularModuleRequestAllowance": 0,
                "regularRequestsLeftThisMonth": 0,
                "regularRequestsThisMonth": 0
            }
        },
        "userLevel": 1,
        "userType": "free"
    },
    "result": {
        "probes": [
            "64 bytes from ord37s07-in-f46.1e100.net (172.217.1.46): icmp_seq=1 ttl=119 time=25.1 ms",
            "64 bytes from ord37s07-in-f46.1e100.net (172.217.1.46): icmp_seq=2 ttl=119 time=24.8 ms",
            "64 bytes from ord37s07-in-f46.1e100.net (172.217.1.46): icmp_seq=3 ttl=119 time=24.7 ms",
            "64 bytes from ord37s07-in-f46.1e100.net (172.217.1.46): icmp_seq=4 ttl=119 time=24.8 ms",
            "64 bytes from ord37s07-in-f46.1e100.net (172.217.1.46): icmp_seq=5 ttl=119 time=24.8 ms",
            "64 bytes from ord37s07-in-f46.1e100.net (172.217.1.46): icmp_seq=6 ttl=119 time=24.8 ms"
        ],
        "stats": [
            "6 packets transmitted, 6 received, 0% packet loss, time 2504ms"
        ]
    },
    "success": true,
    "toolType": "pingFree",
    "userType": "free"
}

```

