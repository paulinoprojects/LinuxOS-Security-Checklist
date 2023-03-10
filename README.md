# LinuxOS-Security-Checklist

1. <b>Keep the OS updated with the latest patches and security updates.</b>
    - Open the termimal interface and follow the these steps below in sequential order.
    - Update the package manager: <b><i>sudo apt-get update</i></b>
    - Upgrade the system packages: <b><i>sudo apt-get upgrade</i></b>
    - Install security updates: <b><i>sudo apt-get dist-upgrade</i></b>
    - Enable automatic updates (You can enable automatic updates by installing the unattended-upgrades package):<b><i>sudo apt-get install unattended-upgrades</i></b>
    - Once the package is installed, you can configure it by editing the configuration file: <b><i>sudo nano /etc/apt/apt.conf.d/50unattended-upgrades</i></b>
      - In the configuration file, you can set the following options:
          - "//Unattended-Upgrade::Automatic-Reboot": <b><i>Set to "true" to enable automatic reboots after updates.</i></b>
          - "//Unattended-Upgrade::Automatic-Reboot-Time": <b><i>Set the time of day to perform automatic reboots.</i></b>
    - Use a package audit tool (You can use a package audit tool like <b><i>lynis</i></b> to scan the system for security issues and vulnerabilities):
    <b><i>sudo apt-get install lynis</i></b>
    - Once the tool is installed, you can run it with the following command: <b><i>sudo lynis audit system</i></b>
    - Monitor the system logs: Regularly check system logs like <b><i>/var/log/syslog and /var/log/auth.log</i></b> for any suspicious activity or errors.

By following these steps, you can ensure that your Linux OS stays updated with the latest security patches and updates.



2. <b>Remove or disable any unnecessary services, ports, and protocols.</b>
    - Identify the services, ports, and protocols that are not needed: Review the list of installed services and running processes, and identify any that are not needed for the system's intended purpose. For example, if the system is not used as a web server, it may not need to run a web server daemon like Apache or Nginx.
        - ps command: This command displays information about the currently running processes. To display all processes, run the command "ps -ef". To display only the processes for a specific user, run the command "ps -u username".
        - top command: This command provides a real-time view of the system processes, including their CPU and memory usage. To run the command, simply type "top" in the terminal.
        - netstat command: This command displays the current network connections and open ports. To display all open ports, run the command "netstat -tulnp".
        - systemctl command: This command is used to manage services on a Linux system. To list all services, run the command "systemctl list-units --type=service".
        - chkconfig command: This command is used to list and manage services on a Linux system. To list all services, run the command "chkconfig --list".
        - nmap command: This command is used to scan for open ports on a system or network. To scan a specific IP address or range of addresses, run the command "nmap IP_address_or_range". 
    - Disable the services: Use the systemctl command to disable any services that are not needed. For example, to disable the Apache web server, run the following command: <b><i>sudo systemctl disable apache2</b></i>.
    - Close unnecessary ports: Use the firewall to close any unnecessary open ports. You can use the <b><i>iptables or ufw (Uncomplicated Firewall)</b></i> command to configure the firewall. For example, to close port 80 (HTTP), run the following command: <b><i>sudo ufw deny 80</b></i>.
    - Disable unnecessary protocols: Review the network configuration and disable any unnecessary protocols. For example, if the system is not used for file sharing, you may want to disable the SMB or NFS protocols.
    - Test the configuration: After making changes to the services, ports, and protocols, test the configuration to ensure that the system is still functioning as intended.

4. Use strong passwords for all user accounts and disable password authentication for SSH access in favor of public key authentication.
5. Configure a firewall to restrict incoming and outgoing traffic.
6. Disable root login and create a separate non-root user with sudo privileges.
7. Encrypt sensitive data using tools like dm-crypt or LUKS.
8. Configure SELinux or AppArmor to enforce mandatory access controls and protect against privilege escalation attacks.
9. Enable auditing and logging to monitor system activity and detect potential security incidents.
10. Disable unnecessary kernel modules and system calls.
Limit user privileges using tools like chroot or containers.
Use intrusion detection and prevention systems like Snort or Suricata to monitor network traffic and detect potential attacks.
Disable unnecessary network services like Telnet, FTP, and NFS.
Enable two-factor authentication for privileged accounts.
Regularly backup important data and test the backups to ensure they are functional and reliable.
Implement password policies to enforce password complexity, length, and expiration.
Implement network segmentation and isolate critical systems from public-facing networks.
Use encryption for remote access and data transmission using tools like OpenVPN or IPsec.
Configure the system to use secure protocols like SSH and TLS/SSL.
Disable unnecessary logging and debugging features.
Regularly review system logs for any potential security incidents or issues.
This is not an exhaustive list, but it covers many of the important security measures that should be taken to harden a Linux operating system.
