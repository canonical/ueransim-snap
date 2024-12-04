# UERANSIM snap

This project is contains a snap package of UERANSIM.

UERANSIM (pronounced "ju-i ræn sɪm"), is the open source state-of-the-art
5G UE and RAN (gNodeB) simulator. UE and RAN can be considered as a 5G
mobile phone and a base station in basic terms. The project can be used
for testing 5G Core Network and studying 5G System.

## Usage

Install and connect the snap:

```bash
sudo snap install ueransim
sudo snap connect ueransim:network-control
```

To run the gNodeB, create a configuration file in
`/var/snap/ueransim/common/gnb.yml` and run the command:

```bash
sudo ueransim.nr-gnb -c /var/snap/ueransim/common/gnb.yml
```

Because ueransim is a confined snap, it can only read and write to its own
directory: `/var/snap/ueransim/common`.

## Build

To build this snap, you will need a machine with the following requirements:
- Processor: x86-64 dual-core processor
- OS: Ubuntu >= 20.04
- Memory: 8GB RAM

Run
```bash
snapcraft
```
