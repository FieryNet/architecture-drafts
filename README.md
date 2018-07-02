# architecture-drafts

#### Multiple Regions

Cloud Vendor & Geographic Regions table, showing current & announced regions:

| Cloud Vendor | Geographic Regions | Reference |
| :---: | :---: | :---: |
| Microsoft Azure | 54  | https://azure.microsoft.com/en-us/global-infrastructure/regions/ |
| Google Cloud Platform | 20  | https://cloud.google.com/about/locations/ |
| Amazon Web Services  | 22  | https://aws.amazon.com/about-aws/global-infrastructure/ |

#### Messaging Support

Types:

- Broadcast
- Multicast
- Unicast (aka 'whispers')

#### Message Network Propagation

Factors to consider:

- Message type
- Bandwidth consumption (message size & frequency)
- Amount of receiving servers
- Amount of receiving clients

#### Load Balancer & VM's of Node & Redis

```
| - - - - - - - - - - - - |
|  LOAD BALANCER          |
| - - - - - - - - - - - - |

    ^
  | |
  v

| - - - - - - - - - - - - |
|  NODE VM                |
|  (multiple instances)   |
| - - - - - - - - - - - - |

    ^
  | |
  v

| - - - - - - - - - - - - |
|  REDIS VM               |
|  (single / cluster)     |
| - - - - - - - - - - - - |
```

#### Libraries
- `pbf` (for Protocol Buffers)
- `uws` (for server-side WebSockets)
- `simple-peer` (for client-side WebRTC)
