# Fluxlab

My homelab managed with NixOS and Flux CD.

## TODO

### MetalLB

The current configuration for metallb relies on the release and pods running before 
applying address pool and L2 Announcements. Thus attempting to bootstrap the cluster
in its current state will not work, as the necessary ressources required for 
IPAddressPool and L2Announcement to be created does not exist. This should be rectified
with dependsOn or similar tools, telling flux to create ressources in a given order.
