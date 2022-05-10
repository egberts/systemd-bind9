# systemd-bind9

Now reports:

    Overall exposure level for named@test-instance.service: 4.9 OK 🙂

Prototyping the [systemd](https://github.com/systemd/systemd) unit service file
for [ISC Bind9](https://www.isc.org/bind/).

The idea is to maximize the systemd settings for `named` daemon.

# Release schedule

This repo uses [systemd](https://github.com/systemd/systemd)'s 
`tag` naming convention to ensure that these unit service files 
and `systemd` are closely related or exactly matched.

Really, this trial is adopting a push-release schedule.  If this 
repo got pushed, it gets tested and delivered.

My labs have many bind9 scenarios on-hands to try against.

* name-caching (desktop)
* dual-view (home gateway)
* bastion DNS (small-medium business)
* split-horizon DNS (whitelab)
* split-forwarders (laptop)
* private root DNSSEC (whitelab)
* hidden-master

Many of the above scenarios have dependency on interface(s) being 
available before `named` startup and after `named` startup.

And many Linux OS distros like ArchLinux, Devuan, Debian 11, RockyOS, Redhat 8, Fedora, ArchLinux, Gentoo  up and running.  (Smart readers will say Devuan and maybe Gentoo has no `systemd` installed).


# What Test Scenarios We Need

There are a few fringe edge scenarios that I cannot do (or are unable to do)
here that we invite you this repo to expand and be permissive toward:

* GSS/LDAP
* Dynamic Zone
* GeoIP
* `dlopen()` libraries
