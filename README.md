# Active Directory - Setting up & Implementing Group Policy Objects (GPOs) 
## Description

An Active Directory homelab exercise demonstrating how to configure, deploy, and enforce essential Group Policy Objects (GPOs) across a domain environment. This lab covers key administrative security controls, system hardening, user experience standardization, and drive mapping to establish a secure and standardized Active Directory domain structure.

## Environment Used

- Windows Server 2022
- VMware Workstation
- Windows 10 Pro / Enterprise

## 

## Active Directory - Password Policy
### Description

An Active Directory homelab exercise demonstrating how to configure and enforce Domain Password Policies using Group Policy Objects (GPOs). This lab covers creating a new custom GPO, 
configuring account policy rules—including minimum password length, complexity requirements, minimum password age, and maximum password age—and verifying the updated policy settings in the Group Policy Management Editor.

## Lab walk-through


<p align="center">
Launch the Group Policy Management console to view the forest and domain structure.
  <img src="./assets/images/GPO_Ui.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
Create a new Group Policy Object named "Password Policy" in the domain.
  <img src="./assets/images/Creating_pass_policy.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center"> Navigate to Computer Configuration > Policies > Windows Settings > Security Settings > <br> Account Policies > Password Policy in the Group Policy Management Editor.
  <img src="./assets/images/changing_pass_policy.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
  Configure the Minimum password length policy setting to require at least 12 characters.
  <img src="./assets/images/min_length_pass.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center"> 
  Enable the Password must meet complexity requirements policy setting.
  <img src="./assets/images/com_pass.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center"> Configure the Minimum password age setting so passwords must be kept for at least 30 days before changing.
  <img src="./assets/images/min_pass_age.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center"> 
  Configure the Maximum password age setting to require a password expiration every 90 days.
  <img src="./assets/images/max_pass_age.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center">
  Verify the final Password Policy settings summary in the Group Policy Management Editor.
  <img src="./assets/images/changes_pass_policy.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

# Testing & Implementing


<p align="center"> Executed gpupdate /force on client workstations via Command Prompt / PowerShell to pull updated GPOs immediately.
  <img src="./assets/images/forcing-gpo-update.png" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>

<p align="center"> Configures domain-wide account security rules, including minimum password length, complexity requirements, minimum/maximum password age, and account lockout thresholds.
  <img src="./assets/images/pass-policy-testing.PNG" alt="Create new user"
       style="width:80%;height:80%;display:block;margin:0 auto;" />
</p>




