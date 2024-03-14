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
<img width="1512" alt="Screenshot 2024-03-14 at 3 33 19 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/fbb54042-fa2b-483d-931a-938ca8fcfb0a">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 33 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/a18e41eb-a1d6-4caa-93c4-793e7f296b93">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 44 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/62aa9416-cbd3-4429-b463-271df6f2b788">
<img width="1512" alt="Screenshot 2024-03-14 at 3 35 06 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/93a07b6f-304a-4abe-b348-36e94d1fa100">
</p>

<br />

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

1.  Part 1 (Create Virtual Machine in Azure).  Create a Resource Group.  Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs.  When creating the VM, allow it to create a new Virtual Network (Vnet).
</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 3 33 19 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/fbb54042-fa2b-483d-931a-938ca8fcfb0a">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 33 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/a18e41eb-a1d6-4caa-93c4-793e7f296b93">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 44 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/62aa9416-cbd3-4429-b463-271df6f2b788">
<img width="1512" alt="Screenshot 2024-03-14 at 3 35 06 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/93a07b6f-304a-4abe-b348-36e94d1fa100">
</p>

<br />

1.  Part 1 (Create Virtual Machine in Azure).  Create a Resource Group.  Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs.  When creating the VM, allow it to create a new Virtual Network (Vnet).
</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 3 33 19 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/fbb54042-fa2b-483d-931a-938ca8fcfb0a">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 33 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/a18e41eb-a1d6-4caa-93c4-793e7f296b93">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 44 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/62aa9416-cbd3-4429-b463-271df6f2b788">
<img width="1512" alt="Screenshot 2024-03-14 at 3 35 06 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/93a07b6f-304a-4abe-b348-36e94d1fa100">
</p>

<br />

1.  Part 1 (Create Virtual Machine in Azure).  Create a Resource Group.  Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs.  When creating the VM, allow it to create a new Virtual Network (Vnet).
</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 3 33 19 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/fbb54042-fa2b-483d-931a-938ca8fcfb0a">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 33 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/a18e41eb-a1d6-4caa-93c4-793e7f296b93">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 44 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/62aa9416-cbd3-4429-b463-271df6f2b788">
<img width="1512" alt="Screenshot 2024-03-14 at 3 35 06 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/93a07b6f-304a-4abe-b348-36e94d1fa100">
</p>

<br />

1.  Part 1 (Create Virtual Machine in Azure).  Create a Resource Group.  Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs.  When creating the VM, allow it to create a new Virtual Network (Vnet).
</p>

</p>
<img width="1512" alt="Screenshot 2024-03-14 at 3 33 19 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/fbb54042-fa2b-483d-931a-938ca8fcfb0a">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 33 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/a18e41eb-a1d6-4caa-93c4-793e7f296b93">
<img width="1512" alt="Screenshot 2024-03-14 at 3 34 44 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/62aa9416-cbd3-4429-b463-271df6f2b788">
<img width="1512" alt="Screenshot 2024-03-14 at 3 35 06 PM" src="https://github.com/richardwines32/osticket_prerequisites_and_installation/assets/162821778/93a07b6f-304a-4abe-b348-36e94d1fa100">
</p>

<br />
