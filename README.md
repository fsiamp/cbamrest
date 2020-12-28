# Nokia CBAM (CloudBand Application Manager) REST Client

This tool is a GUI made for Windows and Openstack<br>
In Windows you will just need to execute the setup.exe file and launch installation.<br>

For Openstack, you can just transfer the qcow2 on the controller and upload image in glance. Then from dashboard, launch an instance in network with externally routable IP addresses (e.g management network) and use m1.small flavor. Once the VM is deployed, then go to http://<CBAM_REST_Client_IP> <br>
Moreover, you will need to login web console of the VM as cbam/tigris or root/tigris and edit /etc/network/interfaces<br><br>

Add the correct eth0 configuration based on the network/mask you have deployed:<br>

auto eth0<br>
iface eth0 inet static<br>
address 10.0.0.6<br>
netmask 255.255.255.0<br>
network 10.0.0.0<br><br>
gateway 10.0.0.1<br>

Concerning usage of this tool:<br>
1. Get CBAM token by completing the CBAM IP, client id and client secret fields.<br>

2. Now in case you want to scale VNF then you will need to click on 'Scale VNF'. Access token and CBAM IP will be automatically populated after executing step 1. You will need here to define aspect id, VNF Id, number of steps, scale direction and additional parameters.
