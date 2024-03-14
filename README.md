<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

<p>
1.  Part 1 (Create Virtual Machine in Azure).  Create a Resource Group.  Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs.  When creating the VM, allow it to create a new Virtual Network (Vnet).
</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 3 33 19 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/fbb54042-fa2b-483d-931a-938ca8fcfb0a">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 33 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/a18e41eb-a1d6-4caa-93c4-793e7f296b93">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 44 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/62aa9416-cbd3-4429-b463-271df6f2b788">
<img width="1512" alt="Screenshot 2024-03-14 at 3 35 06 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/93a07b6f-304a-4abe-b348-36e94d1fa100">
</p>

<br />

 <p>
2.  Part 2.  Install / Enable IIS in Windows WITH CGI and Common HTTP Features.  World Wide Web Services -> Application Development Features -> [X] CGI [X] Common HTTP Features AND IIS Management Console Internet Information Services -> Web Management Tools -> IIS Management Console [X] IIS Management Console

</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 4 03 25 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/939f8e7d-d6b8-48e6-96b9-2bab6bc057bf">
<img width="1512" alt="Screenshot 2024-03-14 at 4 04 03 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/5d39af2f-4d6d-4d8e-8952-ff3f662da422">
<img width="1512" alt="Screenshot 2024-03-14 at 4 06 53 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/bd7b6324-d991-4b93-b38d-402eaf5a2446">
</p>

<br />

<p>
3.  From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi).  From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi).
</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 4 13 07 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/72a74953-1273-4614-92a0-793904097dd5">
<img width="1512" alt="Screenshot 2024-03-14 at 4 14 08 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/f4d30109-4220-4685-a162-8753cbe49131">
<img width="1512" alt="Screenshot 2024-03-14 at 4 16 28 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/b8de08bf-59f0-4eb5-b100-e37eab02112a">
</p>

<br />

<p>
4.  Create the directory C:\PHP.  From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP.
</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 4 22 29 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/87d35422-71ab-40fb-af10-b9c539e3678d">
<img width="1512" alt="Screenshot 2024-03-14 at 4 26 39 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/3b198802-0cf7-440d-80c1-5808d8b05f6b">
<img width="1512" alt="Screenshot 2024-03-14 at 4 26 44 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/2a2c07d2-fefe-48a6-8be4-580cf57eb7f7">
</p>

<br />

5. From the Installation Files, download and install VC_redist.x86.exe.  From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi).  Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration -> Create Password,
</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 4 31 38 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/d9da5bd8-c07d-478e-9f83-58c9390e8ff2">
<img width="1512" alt="Screenshot 2024-03-14 at 4 32 30 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/dff10020-5ec0-44a4-953e-9d8f1f417955">
<img width="1512" alt="Screenshot 2024-03-14 at 4 33 12 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/6468b1c8-c342-4dee-ac7b-86bdfa8170b5">
<img width="1512" alt="Screenshot 2024-03-14 at 4 34 08 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/e8107daa-7902-45ab-8155-add56cd86061">
</p>

<br />

6.  Open IIS as an Admin.  Register PHP from within IIS.  Reload IIS (Open IIS, Stop and Start the server)
</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 4 37 28 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/ac1af1e7-fe36-4df9-9cb9-1a3fb1217106">
<img width="1512" alt="Screenshot 2024-03-14 at 4 39 01 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/e70b60c1-bf4c-4a27-b7c7-e0b307d61d9a">
<img width="1512" alt="Screenshot 2024-03-14 at 4 39 39 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/003db350-3edb-4429-aa6a-a74fec67265f">
<img width="1512" alt="Screenshot 2024-03-14 at 4 40 26 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/0e8c6157-8e1c-449f-8554-4fba0200afb5">
</p>

<br />

7.  Install osTicket v1.15.8.  Download osTicket from the Installation Files Folder.  Extract and copy “upload” folder to c:\inetpub\wwwroot.  Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”.

</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 4 47 01 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/07c32a34-5efe-4e97-969f-35ad1a4ede5b">
<img width="1512" alt="Screenshot 2024-03-14 at 4 49 28 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/eff94334-1794-4adc-a3bf-eecf84f93348">
<img width="1512" alt="Screenshot 2024-03-14 at 4 50 30 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/d6f29042-1d44-4c91-982b-6b7eef005ab6">
<img width="1512" alt="Screenshot 2024-03-14 at 4 51 09 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/71a20363-2e2f-4444-a1bb-f08586ca6f71">
</p>

<br />

8.  Reload IIS (Open IIS, Stop and Start the server).  Go to sites -> Default -> osTicket.  On the right, click “Browse *:80”

</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 4 54 42 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/13c71825-27a2-4379-a85a-7e0f92a26cf0">
<img width="1512" alt="Screenshot 2024-03-14 at 4 56 30 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/391bef72-038f-4af3-997a-e141a27a3043">
<img width="1512" alt="Screenshot 2024-03-14 at 4 57 01 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/751dc935-e411-433c-85ac-a9b614cf51a8">
</p>

<br />

9.  Note that some extensions are not enabled.  Go back to IIS, sites -> Default -> osTicket.  Double-click PHP Manager.  Click “Enable or disable an extension”.  Enable: php_imap.dll.  Enable: php_intl.dll  Enable: php_opcache.dll  Refresh the osTicket site in your browse, observe the changes.

</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 5 29 16 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/d24357cf-3101-466b-b753-aa32b73dd518">
<img width="1512" alt="Screenshot 2024-03-14 at 5 30 21 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/ec05d1c5-9e73-4bda-ab1a-5916382f3292">
<img width="1512" alt="Screenshot 2024-03-14 at 5 30 44 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/e928b29f-a9a1-4c88-8233-a921b0afa44c">
</p>

<br />

10.  Rename: ost-config.php From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost-config.php  Assign Permissions: ost-config.php  Disable inheritance -> Remove All  New Permissions -> Everyone -> All  Continue Setting up osTicket in the browser (click Continue)  Name Helpdesk  Default email (receives email from customers)

</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 5 37 26 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/50630469-241c-4d00-9e58-f1f91e812e7d">
<img width="1512" alt="Screenshot 2024-03-14 at 5 37 44 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/d84bedd8-4d48-41be-b49c-4b1c48db3b46">
<img width="1512" alt="Screenshot 2024-03-14 at 5 42 56 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/759d676c-f0f6-43ae-9e61-2d9ebab7f6a3">
<img width="1512" alt="Screenshot 2024-03-14 at 5 41 37 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/a6c3557e-26dc-472b-ab48-c4c2185a6c23">
<img width="1512" alt="Screenshot 2024-03-14 at 5 41 44 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/83c51880-07e5-43a6-a6c8-aae7080bfc3b">

</p>

<br />

11.  Continue Setting up osTicket in the browser (click Continue).  Name Helpdesk Default email (receives email from customers).  From the Installation Files, download and install HeidiSQL.  Open Heidi SQL.  Create a new session, root/Password1  Connect to the session.  Create a database called “osTicket”.

</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 6 54 07 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/6b065efd-c52a-41e4-b344-4d19b0f78b70">
<img width="1512" alt="Screenshot 2024-03-14 at 6 55 27 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/7fbfbdb5-e7ad-4883-bbe9-d414804669a7">
<img width="1512" alt="Screenshot 2024-03-14 at 6 58 22 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/7a177a0e-8896-43af-8e8f-975909ab60c7">
<img width="1512" alt="Screenshot 2024-03-14 at 6 59 34 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/4be11b2a-d248-4571-a98c-e4837cb2adc8">
<img width="1512" alt="Screenshot 2024-03-14 at 7 01 36 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/dd092ce3-8d5c-4fea-9be8-439fcb9a4437">
<img width="1512" alt="Screenshot 2024-03-14 at 7 04 20 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/8bc731c0-0ea8-41b5-98ca-736fb8878f66">
</p>

<br />

12.  Continue Setting up osticket in the browser  MySQL Database: osTicket  MySQL Username: root  MySQL Password: Password1  Click “Install Now!”  Congratulations, hopefully it is installed with no errors!  Browse to your help desk login page: http://localhost/osTicket/scp/login.php  End Users osTicket URL:  http://localhost/osTicket/  Clean up  Delete: C:\inetpub\wwwroot\osTicket\setup  Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php Browse to your help desk login page: http://localhost/osTicket/scp/login.php   End Users osTicket URL: http://localhost/osTicket/ 

</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 7 04 29 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/1e84959c-9d47-4f47-8a74-daa3d353c562">
<img width="1512" alt="Screenshot 2024-03-14 at 7 04 52 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/941ff31d-8d20-482b-b430-04b420cf1da4">
<img width="1512" alt="Screenshot 2024-03-14 at 7 10 36 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/5134d38f-5c3d-4323-a462-f9850e1feaa1">
<img width="1512" alt="Screenshot 2024-03-14 at 7 11 15 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/6d263960-d95a-437c-8158-83fdc976ee58">
<img width="1512" alt="Screenshot 2024-03-14 at 7 14 33 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/68218914-e7d8-48cf-b0e4-c34568f1faa8">
<img width="1512" alt="Screenshot 2024-03-14 at 7 16 11 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/37134919-a951-4b94-b651-0100feb358ef">
<img width="1512" alt="Screenshot 2024-03-14 at 7 17 45 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/ff5b6375-469d-489e-8804-f685f8ac7d9a">

</p>

<br />
