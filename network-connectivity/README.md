# Network Connectivity Troubleshooting Lab

## Environment
- Windows virtual machine
- VMware Fusion
- Spiceworks Help Desk

## Issue
Simulated a user being unable to access the internet because of an unplugged Ethernet cable.

## Simulation
Disconnected the virtual network adapter in VMware Fusion to simulate an unplugged cable.

## Findings
Ran ipconfig. The Ethernet adapter showed “Media disconnected,” indicating no network link.

## Action Taken
Reconnected the virtual network adapter to simulate plugging the Ethernet cable back in.

## Verification
Ran ipconfig and confirmed an IPv4 address and default gateway were displayed. Confirmed successful ping replies and loaded a webpage to verify internet access.

## Outcome
Connectivity was restored. Documented the findings, corrective action, and verification in Spiceworks, attached screenshots, and closed the ticket.

## Skills Practiced
- Network connectivity troubleshooting
- Windows command-line tools
- Virtual machine network configuration
- Help desk ticket documentation and closure
