# VTP-CONFIGURATION
VTP CONFIGURATION
------------------

SW-1
------
int fa0/1
switchport mode trunk 
end

SW-2
------
int range fa0/1-2
switchport mode trunk 
end

SW-1
------
int fa0/1
switchport mode trunk 
end

creating VTP modes
-----------------

SW-1
------
vtp mode server
vtp domain ccna
vtp password cisco123
exit

SW-2
----
vtp mode client
vtp domain ccna
vtp password cisco123
exit

SW-3
----
vtp mode transparent
vtp domain ccna
vtp password cisco123
exit
![VTP CONFIGURATION](https://user-images.githubusercontent.com/106605770/177993446-47d79947-8e55-40e4-9f7d-00074dc611e4.jpg)


creating vlans
----------------
SW-1
-----
vlan 10
name IT 
exit
vlan 20
name HR

SW-2
is client it recieves the vlans of sw-1


SW-3
-----
vlan 100
name Finance
exit
vlan 50
name Admin
