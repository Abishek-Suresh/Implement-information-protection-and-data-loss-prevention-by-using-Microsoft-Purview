# Implement-information-protection-and-data-loss-prevention-by-using-Microsoft-Purview

<img width="1280" height="641" alt="Image" src="https://github.com/user-attachments/assets/16fd7e6c-483f-46ec-ab55-1f4fb0946dea" />

This repository documents a hands-on applied skills exercise based on Microsoft Learn titled "Implement information protection and data loss prevention by using Microsoft Purview". The scenario in this experience helped me to validate my ability to discover, classify, and protect sensitive data in Microsoft 365, effectively implementing data security by using Microsoft Purview. 

# SCENARIO:

You were recently hired by Contoso, Ltd to help the company's IT team implement information protection and data loss prevention by using Microsoft Purview. The company's executives are very concerned that all guidelines are followed and that all requirements are met when you complete the activities in their environment.

## TASK 1 - CREATED A CUSTOM SENSITIVE INFORMATION TYPE (SIT) :

In this first task, I've created a Sensitive Information Type named SIT1 with the following requirements:
- Has a confidence level of medium
- Used a keyword dictionary named Dictionary1 as the primary element that includes the following words: "Contoso", "Litware", and "Adventureworks".
- Used the Func_ssn function as the supporting element.
- 200 characters as proximity

## TASK 2 - CREATED AND PUBLISHED A SENSITIVITY LABEL:

Created a top-level sensitivity label named **Private** for the "internal private" that will apply to emails and files only with highest priority. The solution met the following requirements:
- Parent label **Private** must contain a sublabel named **Internal**. Documents labeled as Internal must have a header of **internal private** on the center of the page.
- Parent label **Private** must contain a sublabel named **External**. Documents labeled as External must meet the following requirements:
    - Be encrypted
    - Be prevented from being changed
    - Expire two weeks after the label is applied.
    - Only be viewed by authenticated users.
    - Only be viewed by users that are signed in.
- Private and its associated sublabels must be published. When a document has either of the sublabels applied, a reason must be provided if a user removes a sublabel or applies a lower priority label.

## TASK 3 - CREATED AND ASSIGNED AN AUTO-LABELING POLICY:

Configured an auto-labeling policy for **Private/Internal** label such that it will be applied to **XLSX** files in Microsoft Sharepoint Online and OneDrive that contain one or more **credit card numbers**.

## TASK 4 - CONFIGURED A DLP POLICY:

Configured a custom DLP policy that will prevent accidental data loss due to sharing of sensitive internal information to people outside of Microsoft 365. The solution met the following requirements:

- Prevent users from sharing **user login credentials with external users** via email, microsoft teams, Sharepoint Online, and OneDrive.
- When a user attempts to share this type of information, generate a high severity alert and notify administrators. The user must receive a policy tip with the message "Sharing user login credentials is not allowed".
- The policy must run in test mode and show policy tips.


## Credential:
https://learn.microsoft.com/api/credentials/share/en-us/ABISHEKS-9295/E350AD514B84108D?sharingId=478DF7F6457271A9
