# Firewall nftables IP4 pour 1, 2, ou 3 interfaces



## Utilisation :

- Sauvegardez ce script sous /etc/nftables.conf

- Activez nftables au démarrage :
```bash
	systemctl enable nftables
	systemctl start nftables
```
- Activez le routage IP (dans /etc/sysctl.conf) :
```
	net.ipv4.ip_forward=1
	# Pour desactiver ipv6 (facultatif mais recommandé)
	net.ipv6.conf.all.disable_ipv6 = 1
	net.ipv6.conf.default.disable_ipv6 = 1
	net.ipv6.conf.lo.disable_ipv6 = 1
```
- Puis rechargez :
```bash
	sysctl -p
```
