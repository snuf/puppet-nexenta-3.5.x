# Puppet installer for Nexenta 3.5.x

After repackaging Chef and deploying it someone asked me if I could have
a look at Puppet, as they were not able to get it running on their Nexenta
kit. Turns out there is a libc compatibility issue, which can be "solved" 
and is "solved" by the install script by first installing Chef and reuse
the ruby that is packaged with Chef for Puppet.

## Installing

**nexenta-puppet-install** uses **chef-11.8.0-1.solaris2.5.10.solaris** and 
**puppet-enterprise-3.1.0-solaris-10-i386.tar.gz**. It has only been tested
with those specific versions!!
The puppet.conf is aimed towards a host named **puppet** by default. Put 
the Chef and Puppet client packages in the directory the script resides
in, run the script and all should be fine. If not check the puppet-install.log.

## Uninstalling

Run **nexenta-puppet-uninstall**

## Testing

The setup was only tested with the above named versions of Chef, Puppet
and Nexenta. The Puppet master was also running Puppet 3.1.0.

## Irony

Puppet on Nexenta 3.5.x requires Chef to run :)
