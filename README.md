UNDERSTANDING DNS.

DNS converts computer names such as "www.google.com" to an IP address such as "216.58.199.228" which can be used by the computer to locate resources.

<h2>Video Demonstration</h2>


- ### Building Intuition For DNS [
](https://drive.google.com/file/d/1bORupvdv9gHS6ZOBumU0cessbq0L8BOk/view?usp=share_link)


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)

  Virtual machine-1 named DC-1 which is the Domain server and Virtual machine-2 named Client-1. 
- Microsoft Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- Windows server 2022

Tasks done include;-
- Inspect DNS A-records on the server.
- create some of our own A-records on the server and observe them from the client-1 computer.
- Change IP Address "mainframe" in A-records from server and observe if it changes on Client-1.
- Inspect the A-records again on client-1 ( "ping mainframe" )
- Touch on "CNAME" records (mapping one name to another).

INSPECT DNS A-RECORDS ON THE SERVER

Login to Client-1 as an Admin.

<img width="289" alt="Screenshot 2024-04-26 at 4 58 17 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/316ed3f7-e1b4-4d1d-9d86-aa853fdfb6d0">

Login to DC-1 as an Admin.

<img width="289" alt="Screenshot 2024-04-26 at 5 01 46 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/274c5fc4-bcf3-4de9-8e34-f53f8a3783f8">

Open Command prompt on Client-1 and ping "mainframe"

<img width="443" alt="Screenshot 2024-04-26 at 5 05 13 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/face52ad-042d-4242-8ab2-803dc1f0c470">

CREATE OUR OWN A-RRECORD "mainframe" ON SERVER AND OBSERVE THE CHANGES ON CLIENT-1

Open Server Manager dashboard on DC-1 and Click DNS

<img width="825" alt="Screenshot 2024-04-26 at 5 10 11 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/2fda6a9d-efa9-45e6-85bf-906a411ca39e">

Create A-record "mainframe" and use IP Address of DC-1

<img width="356" alt="Screenshot 2024-04-26 at 5 12 15 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/e973c65c-6f52-44e0-9dd8-e5b17dafc805">

Observe changes on Client-1 ( "ping mainframe" ) and notice that it resolves.

<img width="429" alt="Screenshot 2024-04-26 at 5 17 13 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/fc0f0f1b-ade4-4c14-9c50-46bcbec3732a">

CHANGE IP ADDRESS OF "MAINFRAME" IN THE A-RECORDS, OBSERVE CHANGES ON CLIENT-1, CLEAR THE CLIENT-1 CACHE AND PING MAINFRAME AGAIN.

Ip Address changed to 8.8.8.8

<img width="373" alt="Screenshot 2024-04-26 at 5 25 02 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/86405b27-ac38-4e01-822b-775998a0dbaf">

ping mainframe on client-1, the Ip Address remains as 10.0.0.4.

<img width="352" alt="Screenshot 2024-04-26 at 5 28 27 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/266b4c5e-c467-4c36-bdc8-fa6dc0dc8b4e">

Clear the DNS Cache ( run as Administrator and enter command "ipconfig /flushdns" )

<img width="244" alt="Screenshot 2024-04-26 at 5 30 11 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/4f33e239-f3e6-4376-80d9-c4b3654c1a6a">

<img width="276" alt="Screenshot 2024-04-26 at 5 31 36 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/3e49c086-f37b-41cb-81c2-48f43bc419a7">

INSPECT THE A-RECORDS AGAIN ON CLIENT-1 ( "ping mainframe" )

The IP Address changes from 10.0.0.4 to 8.8.8.8

<img width="343" alt="Screenshot 2024-04-26 at 5 38 47 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/d9407df8-2e73-44f8-beac-4edbf10d9a51">

TOUCH ON "CNAME" RECORDS ( MAPPING ONE NAME TO ANOTHER ).

<img width="267" alt="Screenshot 2024-04-26 at 5 46 59 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/e87172d1-464c-46bd-ba1c-f0bc770e4c74">

<img width="329" alt="Screenshot 2024-04-26 at 5 48 49 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/52448bcf-08e2-4f2a-9532-566bdd4f6ecc">

Notice how it resolves showing that its "pinging www.google.com"

<img width="349" alt="Screenshot 2024-04-26 at 5 50 28 PM" src="https://github.com/BAHIIZI/azure-AD-DNS/assets/164538571/0653c08f-e7b4-4d6f-aaa8-31dc2a9f9fef">










