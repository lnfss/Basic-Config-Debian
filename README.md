# Basic-Config-Debian
## Konfigurasi Jaringan Debian Server 12.9.0

1. Command to Change Hostname

    ```
    hostnamectl set-hostname yourhostname
    ```

2. Command to Set Time, Date, and Timezone

    ```
    timedatectl set-timezone Region/Location
    ```

3. Command to Change Password

    ```
    passwd youruser
    ```

4. Command to Add User

    ```
    adduser newuser
    ```

5. Command to Add Group

    ```
    addgroup newgroup
    ```

6. Command to Add User to Group

    ```
    usermod youruser -G yourgroup
    ```

7. Command to Create Directory

    ```
    mkdir yourdirectoryname
    ```

8. Command to Remove Directory

    ```
    rmdir yourdirectory
    ```

9. Command to Create New File

    ```
    touch yourfilename
    ```

10. Command to Remove File

    ```
    rm yourfile
    ```

11. Command to Get List of Directory Contents

    ```
    ls yourdirectory
    ```

12. Command to Call Directory / Change the Shell Working Directory

    ```
    cd yourdirectory
    ```

13. Command to Get Current Shell Working Directory

    ```
    pwd
    ```

14. Command to Search Text File

    ```
    yourfile |grep textfile
    ```
    notes: 1. to use this grep command, you must type
           2. example: cat /etc/network/interfaces |grep dhcp
           3. 

15. Command to Change IP DHCP or IP Static

    ```
    nano /etc/network/interfaces
    ```
    ```
    # This file describes the network interfaces available on your system
    # and how to activate them. For more information, see interfaces(5).

    source /etc/network/interfaces.d/*

    # The loopback network interface
    auto lo
    iface lo inet loopback

    # The primary network interface
    allow-hotplug ens33
    # Set iface to dhcp if you want to set ip dhcp
    # iface ens33 inet dhcp
    # Set iface to static and set address if you want to set ip static. Then, you can set gateway(optional) if you have other vm as router.
    # iface ens33 inet static
    #    address IPAddress/Prefix
    #    gateway IPAddress
    ```

16. Command to Check The Ports Used by The Linux Server

    To check the ports used by the linux server, you can use the follwing command: netstat or ss
    For example: 

    ```
    ss -lnptu
    ```

17. Command to Use to View Larger Files, It's Paging Program, Provide Scroll Back, Provide Search & Navigate

    ```
    ss -lnptu |less
    ```
    notes: you must type a command with larger files, and then type this '|less' like the example
    
18. Command to Place a Text in Another File

    ```
    echo "<h1>Hello World</h1>" >> /var/www/html
    ```
