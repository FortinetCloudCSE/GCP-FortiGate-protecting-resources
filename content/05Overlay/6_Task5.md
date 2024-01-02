---
title: "On-Ramp BGP"
menuTitle: "On-Ramp BGP"
chapter: false
weight: 5
---

### Configure BGP on cloud on-ramp FortiGate

* Copy the below BGP configurations and paste them into the active FortiGate's CLI console.

```sh
config router bgp
    set as 65400
    set ibgp-multipath enable
    set additional-path enable 
    set additional-path-select 4
    config neighbor-group
        edit HUB1
            set remote-as 65400
            set additional-path both
            set adv-additional-path 4
            set route-reflector-client enable
        next
    end
    config neighbor-range
        edit 1
            set prefix 10.10.1.0 255.255.255.0
            set max-neighbor-num 20
            set neighbor-group HUB1
        next
end

    config network
        edit 1
            set prefix 172.20.1.0 255.255.255.0
        next
    end
end
```

{{% notice note %}} Note the prefix setting under "config neighbor-range".  The dynamic IP addresses assigned to the remote site IPsec VPN interfaces fall within that range, meaning that this router will accept any bgp peer request from those remote sites. {{% /notice %}}