# iptables

<code>
iptables -L

iptables -P INPUT DROP
iptables -P FORWARD DROP
iptables -P OUTPUT ACCEPT


iptables -A INPUT -p tcp --dport 22 -j ACCEPT
iptables -A INPUT -p tcp --dport 80 -j ACCEPT
iptables -A INPUT -p tcp --dport 8006 -j ACCEPT
iptables -A INPUT -p tcp --dport 5900:5999 -j ACCEPT




iptables -A INPUT -i lo -j ACCEPT
iptables -A OUTPUT -o lo -j ACCEPT


iptables -A INPUT -m conntrack --ctstate RELATED,ESTABLISHED -j ACCEPT
iptables -A OUTPUT -m conntrack --ctstate RELATED,ESTABLISHED -j ACCEPT


iptables -A INPUT -p icmp --icmp-type echo-request -j ACCEPT


mkdir /etc/iptables
touch /etc/iptables/rules.v4
chmod 600 /etc/iptables/rules.v4
iptables-save > /etc/iptables/rules.v4



iptables-save > /etc/iptables/rules.v4

apt install iptables-persistent

iptables -L
</code>
