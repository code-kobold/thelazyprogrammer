The Lazy Programmer
===================

#Docker

##Default docker0 Bridge
docker0 bridge is a virtual interface created by Docker server to configure the host system’s docker0 interface as an Ethernet bridge inside the Linux kernel. This allows Docker containers to communicate with each other and with the outside world.

Address and subnet from the private range defined by RFC 1918 that are not in use on the host machine are randomly choosen and assigned to docker0. All Docker containers will be connected to the docker0 bridge by default and can use iptables NAT rules created by docker to communicate with the outside world.

`~$ brctl show`
<table>
    <thead>
        <th>bridge name</th>
        <th>bridge id</th>
        <th>STP enabled</th>
        <th>interfaces</th>
    </thead>
    <tbody>
        <tr>
            <td>br-80fa56973d68</td>
            <td>8000.024240c6178d</td>
            <td>no</td>
            <td>veth0c1d80b, veth2f08619, veth563afa5, veth6c9dc85</td>
        </tr>
        <tr>
            <td>docker0</td>
            <td>8000.02420e6d5191</td>
            <td>no</td>
            <td>-</td>
        </tr>
    </tbody>
</table>



https://developer.ibm.com/recipes/tutorials/networking-your-docker-containers-using-docker0-bridge/



