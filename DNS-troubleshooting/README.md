# Lab 003: DNS Troubleshooting

## Overview
Simulated and resolved a DNS configuration issue that prevented websites from loading while IP connectivity remained available.

## Environment
- Windows 11 Pro
- VMware Fusion
- Spiceworks Help Desk

## Issue
Microsoft Edge displayed a DNS error when attempting to load its startup page.

## Investigation
1. Ran `ipconfig /all` and identified the configured DNS server as `192.0.2.1`, intentionally set for this simulation.
2. Pinged the default gateway, `172.16.234.2`, successfully.
3. Pinged the external IP address `1.1.1.1` successfully.
4. Both ping tests returned four replies with 0% packet loss.
5. Ran `nslookup example.com.` and observed DNS request timeouts.

These results isolated the issue to DNS resolution while IP connectivity continued working.

## Resolution
1. Restored automatic DNS server configuration on the Ethernet adapter.
2. Ran `ipconfig /flushdns` to clear the local DNS resolver cache.

Correcting the DNS configuration resolved the cause. Flushing the cache cleared previously cached DNS results.

## Verification
- Repeated `nslookup example.com.` successfully using DNS server `172.16.234.2`.
- Confirmed the previously failing page loaded in Microsoft Edge.
- Documented the investigation, resolution, and verification in Spiceworks.

## Skills Practiced
- Network configuration inspection
- Gateway and external IP connectivity testing
- DNS troubleshooting with nslookup
- DNS client configuration and cache management
- Ticket documentation and resolution

## Screenshots
Supporting screenshots are included in this folder.

## Scope
This was a simulated DNS client configuration issue in a home lab.
