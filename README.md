# <a href="#-team-apples"><g-emoji class="g-emoji" alias="apple" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f34c.png">🍎</g-emoji> Team Apples</a>
## <a href="#-team-members">
  <g-emoji class="g-emoji" alias="busts_in_silhouette" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f465.png">👥</g-emoji>
  Team Members
</a>
<ul>
  <li>Juan Coutink</li>
  <li>Cédric Hügli</li>
  <li>Özlem Kösker</li>
  <li>Revathi Ravada</li>
  <li>Hossein Zamanlou</li>
</ul>

# Table of Content

  
# Introduction
This document describes the contribution to the process from the company Ximiq AG as part of the course "Digitalization of Business Processes" at the University of Applied Sciences and Arts North-western Switzerland. 


# Description of the Use Case 

Ximiq was founded in 2013 as a Consulting Firm with the objective of working with customer as partners. The aim of Ximiq is to align Business and IT. This is done through Enterprise Architecture Management. While supporting one of our customers in EAM, we realized the need to automatically generate reports from the Enterprise Architecture Modelling Tools. At this point, Ximiq developed the ADOIT Report Generator for Microsoft Word. Thanks to the ADOIT Report Generator for Word customers are able to flexibly and quickly create architecture documentation in Microsoft Word by data sourced live from ADOIT. Customers can create their own template structure for their individual use cases or existing project management templates (e.g. Hermes) and create deliverables automatically. Instead of compiling their lists and data manually, customers can have it automatically inserted and updated from one single reliable source. 

The sales process for the Generator is currently at an Ad-hoc stage, meaning that roles and responsibilities are yet to be defined in order to increase pipeline and ultimately business. Throughout this process, we realized that Ximiq doesn’t have the resources for a dedicated Sales Team and the sales engagement is fully managed by consultants. That’s the reason why we need to implement a lean and streamlined process to better allocate resources.  

 
# AS-IS Process Description 

The Sales Process is triggered by three Events:

1. A potential customer downloads the Report Generator in the AppSource Marketplace from Microsoft.
2. A potential customer sends a request for the Report Generator through the BOC-Marketplace which results in an E-Mail sent to Ximiq AG.
3. A Reseller/Partner or one of the Ximiq-Consultants refers the Report Generator to a customer. This is done by sending an email, a chat message or a call.

The first event automatically creates a new Lead in Ximiqs CRM-System. Since there’s no notification, the new leads must be checked. After the other two events, a new lead must be created. Then an initial email with the following content is sent: 

- A link to book a live demo
- Mention of the possibility to request a trial-License
- The pricing model

If the customer requests a live demo, an appointment will be automatically generated. The live demo takes place. If the customer requests a trial license, the license will be sent to them. After 30 days, another reminder email including the price information is sent to the customer. If there is still no feedback, after 14 days, the lead is closed as lost.

However, if the customer orders the full license, the deal is registered in the CRM and the pricing is calculated based on the type of license chosen and the size of the customer in terms of number users. The accountant is then informed in order to create a new invoice based on the information registered in the CRM. The accountant forwards the invoice to the consultant who will then send it to the customer. If the customer doesn’t pay the invoice, an email reminder is sent by the consultant. Should there not be feedback from the customer, the lead is closed as lost.

However, if the customer does pay the invoice, the full license key is generated and then sent to the customer. In this case, the opportunity is closed as won.

At any point of this process, the customer can always purchase the license, the process resumes on the step “Register order in CRM”.

Description of AS-IS Process Elements
========

![AS-IS_Process_Description_1](https://user-images.githubusercontent.com/127504427/232119513-b4df5ba0-b13e-48c6-8511-db435e3c85a0.png)
![AS-IS_Process_Description_2](https://user-images.githubusercontent.com/127504427/232119516-8ae475e3-bd41-4cef-8e8d-a57cf7498430.png)
![AS-IS_Process_Description_3](https://user-images.githubusercontent.com/127504427/232119517-1816298c-d361-4250-a1bc-5973c4aa87d0.png)
![AS-IS_Process_Description_4](https://user-images.githubusercontent.com/127504427/232119519-079ffcc8-473e-434d-8b84-3684c501b218.png)
![AS-IS_Process_Description_5](https://user-images.githubusercontent.com/127504427/232119524-034f1ae4-6395-4f8b-ba5b-ee7e0331622c.png)
![AS-IS_Process_Description_6](https://user-images.githubusercontent.com/127504427/232119525-6f1a9fd1-0895-46b3-8ce3-7b695a73d26c.png)
![AS-IS_Process_Description_7](https://user-images.githubusercontent.com/127504427/232119526-f4229d96-7c2d-4571-8190-81957db2e7a8.png)


# Potential automisations and extensions
When analysing the AS-IS process several open points are there. First of all why does the firm have 

# TO-BE Process Description

Description of TO-BE Process Elements
========

| Row | Picture | Column 3          | Column 4          | Column 5          |
| --- | ------- | ---------------- | ---------------- | ---------------- |
| 1   |   ![TO-BE-PROCESS/TOBE01.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE01.png) | Row 2, Column 3   | Row 2, Column 4   | Row 2, Column 5   |
| 2   | ![TO-BE-PROCESS/TOBE02.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE02.png) | Row 2, Column 3   | Row 2, Column 4   | Row 2, Column 5   |
| 3   | ![TO-BE-PROCESS/TOBE03.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE03.png) | Row 3, Column 3   | Row 3, Column 4   | Row 3, Column 5   |
| 4   | ![TO-BE-PROCESS/TOBE04.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE04.png) | Row 4, Column 3   | Row 4, Column 4   | Row 4, Column 5   |
| 5   | ![TO-BE-PROCESS/TOBE05.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE05.png) | Row 5, Column 3   | Row 5, Column 4   | Row 5, Column 5   |
| 6   | ![TO-BE-PROCESS/TOBE06.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE06.png) | Row 6, Column 3   | Row 6, Column 4   | Row 6, Column 5   |
| 7   | ![TO-BE-PROCESS/TOBE07.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE07.png) | Row 7, Column 3   | Row 7, Column 4   | Row 7, Column 5   |
| 8   | ![TO-BE-PROCESS/TOBE08.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE08.png) | Row 8, Column 3   | Row 8, Column 4   | Row 8, Column 5   |
| 9   | ![TO-BE-PROCESS/TOBE09.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE09.png) | Row 9, Column 3   | Row 9, Column 4   | Row 9, Column 5   |
| 10  | ![TO-BE-PROCESS/TOBE10.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE10.png) | Row 10, Column 3  | Row 10, Column 4  | Row 10, Column 5  |
| 11  | ![TO-BE-PROCESS/TOBE11.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE11.png) | Row 11, Column 3  | Row 11, Column 4  | Row 11, Column 5  |
| 12  | ![TO-BE-PROCESS/TOBE12.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE12.png) | Row 12, Column 3  | Row 12, Column 4  | Row 12, Column 5  |
| 13  | ![TO-BE-PROCESS/TOBE13.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE13.png) | Row 13, Column 3  | Row 13, Column 4  | Row 13, Column 5  |
| 14  | ![TO-BE-PROCESS/TOBE14.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE14.png) | Row 14, Column 3  | Row 14, Column 4  | Row 14, Column 5  |
| 15  | ![TO-BE-PROCESS/TOBE15.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE15.png) | Row 15, Column 3  | Row 15, Column 4  | Row 15, Column 5  |
| 16  | ![TO-BE-PROCESS/TOBE16.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE16.png) | Row 16, Column 3  | Row 16, Column 4  | Row 16, Column 5  |
| 17  | ![TO-BE-PROCESS/TOBE17.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE17.png) | Row 17, Column 3  | Row 17, Column 4  | Row 17, Column 5  |
| 18  | ![TO-BE-PROCESS/TOBE18.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE18.png) | Row 18, Column 3  | Row 18, Column 4  | Row 18, Column 5  |
| 19  | ![TO-BE-PROCESS/TOBE19.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE19.png) | Row 19, Column 3 | Row 19, Column 4 | Row 19, Column 5 |
| 20  | ![TO-BE-PROCESS/TOBE20.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE20.png) | Row 20, Column 3 | Row 20, Column 4 | Row 20, Column 5 |
| 21  | ![TO-BE-PROCESS/TOBE21.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE21.png) | Row 21, Column 3 | Row 21, Column 4 | Row 21, Column 5 |
| 22  | ![TO-BE-PROCESS/TOBE22.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE22.png) | Row 22, Column 3 | Row 22, Column 4 | Row 22, Column 5 |
| 23  | ![TO-BE-PROCESS/TOBE23.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE23.png) | Row 23, Column 3 | Row 23, Column 4 | Row 23, Column 5 |
| 24  | ![TO-BE-PROCESS/TOBE24.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE24.png) | Row 24, Column 3 | Row 24, Column 4 | Row 24, Column 5 |
| 25  | ![TO-BE-PROCESS/TOBE25.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE25.png) | Row 25, Column 3 | Row 25, Column 4 | Row 25, Column 5 |
| 26  | ![TO-BE-PROCESS/TOBE26.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE26.png) | Row 26, Column 3 | Row 26, Column 4 | Row 26, Column 5 |
| 27  | ![TO-BE-PROCESS/TOBE27.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE27.png) | Row 27, Column 3 | Row 27, Column 4 | Row 27, Column 5 |
| 28  | ![TO-BE-PROCESS/TOBE28.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE28.png) | Row 28, Column 3 | Row 28, Column 4 | Row 28, Column 5 |
| 29  | ![TO-BE-PROCESS/TOBE29.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE29.png) | Row 29, Column 3 | Row 29, Column 4 | Row 29, Column 5 |
| 30  | ![TO-BE-PROCESS/TOBE30.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE30.png) | Row 30, Column 3 | Row 30, Column 4 | Row 30, Column 5 |
| 31  | ![TO-BE-PROCESS/TOBE31.png](https://github.com/DigiBP/Team-Apples/blob/3d0da9e0d0aa43616acadb324b1f08d5aad8b057/TO-BE-PROCESS/TOBE31.png) | Row 31, Column 3 | Row 31, Column 4 | Row 31, Column 5 |



# Conclusion 

# Next Steps

# List of Artifacts and Presentation
Artifacts:

 <ul>
  <li>1. </li>
  <li>2. </li>
  <li>3. </li>
  <li>4. </li>
  <li>5. </li>
</ul>

Presentation Name:
