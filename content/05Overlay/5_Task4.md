---
title: "Remote IPsec"
menuTitle: "Task 4 - Remote IPsec"
chapter: false
weight: 4
---

### Configure IPsec VPN on remote site

* Open a CLI console in the FortiGate by clicking on the cursor **>_** icon or using SSH to the public management IP.  Copy the below configurations into your favorite text editor and "set remote-gw" to the lb-ip. Once completed, copy and paste thes configurations into the cli console.

```sh
config vpn ipsec phase1-interface
    edit HUB1
        set interface port1
        set ike-version 2
        set peertype any
        set net-device disable
        set mode-cfg enable
        set proposal aes256-sha256
        set add-route disable
        set dpd on-idle
        set remote-gw <lb-ip>
        set psksecret Fortinet1!
    next
end


config vpn ipsec phase2-interface
    edit HUB1
        set phase1name HUB1
        set proposal aes256-sha256
        set auto-negotiate enable

    next
end

config firewall policy
    edit 0
        set name ipsec-out
        set srcintf port2
        set dstintf HUB1
        set action accept
        set srcaddr all
        set dstaddr all
        set schedule always
        set service ALL
        set nat disable
    next
    edit 0
        set name ipsec-in
        set srcintf HUB1
        set dstintf port2
        set action accept
        set srcaddr all
        set dstaddr all
        set schedule always
        set service ALL
        set nat enable
    next
end
```

* Run the below commands to ensure that the tunnels are up and functioning proplerly.

```sh
get vpn ipsec tunnel summary
diagnose vpn ike gateway list name HUB1
```

{{% notice note %}}Useful Link - https://community.fortinet.com/t5/FortiGate/Troubleshooting-Tip-IPsec-VPNs-tunnels/ta-p/195955 {{% /notice %}}

