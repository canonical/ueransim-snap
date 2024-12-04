# UERANSIM snap

This project contains a snap package of UERANSIM.

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

To run the gNodeB, edit the configuration file in
`/var/snap/ueransim/common/gnb.yml` as root and run the command:

```bash
sudo ueransim.nr-gnb -c /var/snap/ueransim/common/gnb.yml
```

To run the UE, edit the configuration file in
`/var/snap/ueransim/common/ue.yml` as root and run the command:

```bash
sudo ueransim.nr-ue -c /var/snap/ueransim/common/ue.yml
```

Because ueransim is a confined snap, it can only read and write to its own
directory: `/var/snap/ueransim/common`.
