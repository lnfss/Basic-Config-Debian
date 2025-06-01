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

3. Command to change password

    ```
    passwd youruser
    ```

4. Command to add user

    ```
    adduser newuser
    ```

5. Command to add group

    ```
    addgroup newgroup
    ```

6. Command to add user to group

    ```
    usermod youruser -G yourgroup
    ```

7. Command to create directory

    ```
    mkdir yourdirectoryname
    ```

8. Command to remove directory

    ```
    rmdir yourdirectory
    ```

9. Command to create new file

    ```
    touch yourfilename
    ```

10. Command to remove file

    ```
    rm yourfile
    ```

11. Command to get list of directory contents

    ```
    ls yourdirectory
    ```

12. Command to Call Directory / Change the shell working directory

    ```
    cd yourdirectory
    ```

13. Command to get current shell working directory

    ```
    pwd
    ```

14. Command to search text file

    ```
    yourfile |grep textfile
    ```
    notes: 1. to use this grep command, you must type
           2. example: cat /etc/network/interfaces |grep dhcp
           3. 

15. Command to change IP DHCP or IP Static

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

16. Command to check the ports used by the linux server
To check the ports used by the linux server, you can use the follwing command: netstat or ss
For example: 

    ```
    ss -lnptu
    ```
