# bash-ping-flood
This is a set of small scripts that allows to perform a ping flood attack.

## Dependencies
`iptables`

## Usage
### alter_target.sh
This script (un)sets the target. It adds (removes) an iptables rule for changing the ICMP source address. Such a trick allows to ping multiple hosts, which in their turn ping the target.

> alter_target.sh \<setup-option\> \<target\>

*\<setup-option\>*: *set-target* or *unset-target*

*\<target\>*: a target host

### ping_flood.sh
This script sends ICMP echo requests to each host listed in the provided text file. Each host in the file must be on a separate line.

> ping_flood.sh \<packet-size\> \<interval\> \<util-hosts-file\>

*\<packet-size\>*: the ICMP packet size (excluding the header 8 bytes)

*\<interval\>*: ping interval

\<util-hosts-file\>: a file with util hosts

## License
[Licensed under the MIT license.](./LICENSE.txt)
