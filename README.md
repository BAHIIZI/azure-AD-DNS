UNDERSTANDING DNS
DNS converts computer names such as "www.google.com" to an IP address such as "216.58.199.228" which can be used by the computer to locate resources.

HOW TO CREATE DNS CACHE
Creating a local DNS cache can help improve the speed and efficiency of DNS resolution by storing previously accessed domain names and their corresponding IP addresses locally. Here's a general guide to creating a local DNS cache on a Windows system:

1. **Open Command Prompt**: Press `Win + R`, type `cmd`, and hit Enter to open Command Prompt.

2. **Install DNS Server**: If you haven't already, you need to install the DNS Server feature on your Windows machine. Run the following command in Command Prompt with administrative privileges:
   ```
   dism /online /enable-feature /featurename:DNS-Server-Full-Role /all
   ```

3. **Open DNS Manager**: After the DNS Server feature is installed, open the DNS Manager by typing `dnsmgmt.msc` in Command Prompt and hitting Enter.

4. **Create a Forward Lookup Zone**: In DNS Manager, right-click on "Forward Lookup Zones" and select "New Zone". Follow the wizard to create a new primary zone for the domain you want to cache.

5. **Configure Zone Settings**: Follow the prompts to configure zone settings. You can choose to create a new zone for your entire domain or for specific domains you want to cache.

6. **Configure DNS Server Properties**: Right-click on your DNS server name in DNS Manager and select "Properties". In the properties window, go to the "Forwarders" tab and specify the IP addresses of your ISP's DNS servers or other public DNS servers (e.g., Google DNS - 8.8.8.8, 8.8.4.4).

7. **Start DNS Server Service**: Make sure the DNS Server service is running. You can start it by typing `services.msc` in Command Prompt, finding the "DNS Server" service, and starting it if it's not already running.

8. **Flush DNS Cache**: To clear the DNS cache, run the following command in Command Prompt:
   ```
   ipconfig /flushdns
   ```

9. **Test DNS Resolution**: You can now test DNS resolution by accessing various websites and checking if the DNS cache is working by querying the local DNS server.

This process sets up a local DNS cache using the DNS Server feature on a Windows machine. Keep in mind that configuring DNS settings can affect network connectivity, so ensure that you understand the changes you are making and their implications. Additionally, you may need administrative privileges to perform some of these steps.
