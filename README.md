# Fluxlab

My homelab managed with NixOS and Flux CD.

## TODO

### MetalLB

The current configuration for metallb relies on the release and pods running before 
applying address pool and L2 Announcements. Thus attempting to bootstrap the cluster
in its current state will not work, as the necessary ressources required for 
IPAddressPool and L2Announcement to be created does not exist. This should be rectified
with dependsOn or similar tools, telling flux to create ressources in a given order.

- [ ] Use dependsOn

### Pihole

- [ ] Figure out sops for flux, to set password and share it with external-dns

### External-dns

This is not active yetm but should be set up later. It was postponed as Bitnami stopped 
support of their external-dns chart with built-in pihole support, and i need to read
about the official chart and how to set it up for this purpoose.
