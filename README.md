## Heartbeat on Centos
<pre>
rpm -Uvh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
yum -y install heartbeat

# modify /etc/hosts file on both nodes
176.155.1.1 node1_hostname
176.155.1.2 node2_hostname
</pre>

## Heartbeat Configuration
176.155.1.1 --> node1 real ip address  
176.155.1.2 --> node2 real ip address  
123.45.67.89 --> virtual ip address  

Upload ha.cf, haresources, authkeys to /etc/ha.d directory. authkeys should have permission 0600. See [http://www.linux-ha.org/doc/users-guide/users-guide.html](http://www.linux-ha.org/doc/users-guide/users-guide.html) for more info.
