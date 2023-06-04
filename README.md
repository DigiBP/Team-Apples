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
</ul>


  
# Introduction
This document describes the contribution to the process from the company Ximiq AG as part of the course "Digitalization of Business Processes" at the University of Applied Sciences and Arts North-western Switzerland. 


# Description of the Use Case 

Ximiq was founded in 2013 as a Consulting Firm with the objective of working with customer as partners. The aim of Ximiq is to align Business and IT. This is done through Enterprise Architecture Management. While supporting one of our customers in EAM, we realized the need to automatically generate reports from the Enterprise Architecture Modelling Tools. At this point, Ximiq developed the ADOIT Report Generator for Microsoft Word. Thanks to the ADOIT Report Generator for Word customers are able to flexibly and quickly create architecture documentation in Microsoft Word by data sourced live from ADOIT. Customers can create their own template structure for their individual use cases or existing project management templates (e.g. Hermes) and create deliverables automatically. Instead of compiling their lists and data manually, customers can have it automatically inserted and updated from one single reliable source. 

<img src="https://github.com/DigiBP/Team-Apples/blob/a7366a9b4432520cdf6009083acb7db741415361/AS-IS-PROCESS/ICON.svg"  width="50%" height="50%">

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

![AS-IS-PROCESS/01_AS-IS_Sales Process ADOIT RGfW.png](https://github.com/DigiBP/Team-Apples/blob/4d466a928f8c591dfe7c846aaeca9fe214f92d3c/AS-IS-PROCESS/01_AS-IS_Sales%20Process%20ADOIT%20RGfW.png)




Description of AS-IS Process Elements
========

| Row | Picture | Description          | Problems & Possible Improvements          |
| --- | ------- | ---------------- | ---------------- |
| 1   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS01.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS01.png) | Potential customers can download the application in the Microsoft AppSource Marketplace. It can be installed and added to Microsoft Word but has to be activated by a license key before its usable. https://smp-prod-pb-cac.azurewebsites.net/en-us/product/office/WA200004614?tab=Overview&exp=ubp8   |  | 
| 2   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS02.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS02.png) | Potential customers can request the application via the BOC-Marketplace. BOC is the company that develops ADOIT. This will generate an email sent to Ximiq. The following is the content of the email: Form of address, First Name, Last Name, Email, Organization, Country, Telephone, Messsage.  https://knowledge.boc-group.com/de/module/adoit-word-report-generator/ | This doesn’t automatically trigger the creation of a Lead in CRM | 
| 3   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS03.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS03.png) | Ximiq has several partners (other consultants and resellers of ADOIT) who recommend the Report Generator to their customers. Requests from them arrive via various channels (email, phone, teams chat or verbal). | This doesn’t automatically trigger the creation of a Lead in CRM and is difficult to automate since the data input is unstructured.  | 
| 4   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS04.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS04.png) | If a potential customer downloads the application in the Microsoft AppSource Marketplace, a new lead is automatically generated in Ximiqs CRM-System (Microsoft Dynamics) via API.  | No message for the consultant. Quality of entry is not sufficient yet but can be fixed.    | 
| 5   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS05.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS05.png) | Since there is no message arriving when leads are generated, the consultants have to check whether new leads arrived and if the entries are of good quality.   | This process step is a waste that can be eliminated by automatically informing the consultant when a new lead is created. | 
| 6   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS06.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS06.png) | In the cases when the leads aren’t generated automatically a consultant creates a new lead in CRM.  | This process step can be eliminated by automizing the Lead creatin with structured data input.| 
| 7   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS07.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS07.png) | In all cases an initial email with the following content is sent to the customer : Download-link, Pricing information, Trial information, Technical questions, Link to book a live demo appointment   | Since it’s a standard email for any customer this process step can be automized. | 
| 8   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS08.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS08.png) | When clicking the link in the initial email a customer gets access to a booking tool connected to the customers outlook calendar. The following content appears in the booking tool:  dropdown to choose a consultant, free slots for live demo, Name, Email, Address, Phone number, Notes, ADOIT Version (OnPremis/Cloud) |    | 
| 9   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS09.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS09.png) | If the customer sends the form an appointment and a Teams call link is automatically generated in Outlook. https://outlook.office365.com/owa/calendar/Sales1@ximiq.ch/bookings/  (do not book a live demo!)  |    | 
| 10  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS10.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS10.png) | The potential customer has the chance to book an appointment via booking-link from the initial email. |  |
| 11  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS11.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS11.png) | The live demo is held via Teams. In this call the consultant demonstrates the generator and answers the customers questions. |   | 
| 12  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS12.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS12.png) | The potential customer has the chance to request a 30days trial license to try out the ADOIT Report Generator for Word.  | Since it’s free license it could be sent automatically to the customer. | 
| 13  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS13.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS13.png) | After sending the initial email Ximiq waits two weeks for an answer. |   | 
| 14  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS14.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS14.png) | If the customer doesn’t answer within two weeks a reminder/follow-up email is sent. | This process step could be eliminated by automatization.   | 
| 15  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS15.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS15.png) | After sending the reminder email Ximiq waits two weeks for an answer.  |   | 
| 16  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS16.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS16.png) | The customer either orders the license, the trial license or doesn’t reply. |  | 
| 17  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS17.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS17.png) | The Trial license key is generated via https://guidgenerator.com/ and registered in Postman. The license key is a 32 digit number.  | This process step could be eliminated by automatization.  | 
| 18  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS18.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS18.png) | The license key and an users handbook is sent to the customer vis email.   | This process step could be eliminated by automatization.   | 
| 19  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS19.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS19.png) | The customer can try the report generator for 30 days. The consultant then sends a follow up email. | No automatic reminder for the consultant. |
| 20  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS20.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS20.png) | A follow up email is sent to the customer with the following content: Asking how they liked the Report Generator, Pricing information |  This process step could be eliminated by automatization.   |
| 21  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS21.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS21.png) | The customer either orders the license or not.  | No automatic reminder for the consultant. |
| 22  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS22.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS22.png) | If the customer isn’t interested in buying the license the opportunity is closed as lost in CRM. | This process step could be eliminated by automatization. | 
| 23  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS23.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS23.png) | If the customer wants to order the Report Generator the order is registered in CRM.  |  | 
| 24  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS24.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS24.png) | The Price is calculated based on the following pricing model: Single User: USD 360.00 p.a; Team 10: USD 2520.00 p.a; Team 10: USD 5400.00 p.a; Unlimited: upon request;   | The calculation could be done automatically based on the order entry in the CRM | 
| 25  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS25.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS25.png) | The consultant informs the accountant about the new order via email. | This process step could be eliminated by automatization. | 
| 26  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS26.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS26.png) | The accountant creates the invoice in the ERP-System.| This process step could be eliminated by automatization. | 
| 27  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS27.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS27.png) | The accountant forwards the invoice to the consultant via email. | The accountant could send the invoice directly to the customer. Or it could even be automated. | 
| 28  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS28.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS28.png) | The consultant sends the invoice to the customer.  | The accountant could send the invoice directly to the customer. Or it could even be automated. | 
| 29  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS29.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS29.png) | waiting up to 30 days for payment | No automatic reminder for the consultant | 
| 30  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS30.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS30.png) | The customer then either pays or not. |  | 
| 31  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS31.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS31.png) | If the customer doesn’t pay a reminder is sent. | This process step could be eliminated by automatization | 
| 32  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS32.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS32.png) | After the reminder is sent Ximiq waits another 14 days for the payment.| No automatic reminder for the consultant | 
| 33  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS33.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS33.png) | The customer pays. |  |
| 34  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS34.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS34.png) |  If the client pays and if the accounting team receives a notification that a payment has been made the accountant informs the consultant.  |  | 
| 35  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS35.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS35.png) | The license key is generated via https://guidgenerator.com/ and is then registered in Postman together with the validity date and the number of users. Via Postman API the validity of the license will be checked when it is activated the first time as well as whenever the application is used.| The current solution is not scalable.  |
| 36  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS36.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS36.png) | The consultant sends the license key, a user handbook as well as a installation handbook to the customer. | This process step could be eliminated by automatization |
| 37  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS37.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS37.png) | In the CRM the status of the opportunity is set to “won”. |  |








# Potential automisations and extensions
When analysing the AS-IS process several open points are there. First of all why does the firm have 
.
.
.
.
.
.
.
.


# TO-BE Process Description


![TO-BE-PROCESS/01_TO-BE_Sales Process ADOIT RGfW.png](https://github.com/DigiBP/Team-Apples/blob/6bca72e9c4b8127b2efd3ab2ec582e0f63ea8a77/TO-BE-PROCESS/01_TO-BE_Sales%20Process%20ADOIT%20RGfW.png)




Description of TO-BE Process Elements
========

| Row | Picture | Description          | Solution          | 
| --- | ------- | ---------------- | ---------------- | 
| 1   |   ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE01.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE01.png) | During any partners download process the customer filled the contact form.   |  1. Start Event - Software request received https://github.com/DigiBP/Team-Apples#1-start-event---software-request-received| 
| 2   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE02.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE02.png) |  Customers information is stored in CRM. | 1. Start Event - Software request received https://github.com/DigiBP/Team-Apples#1-start-event---software-request-received  | 
| 3   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE03.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE03.png) | An initial email is sent to the customer. The email includes a link to order a 30 days free trial license as well as scheduling a Live-Demo.  | 2. Sent e-mail with URL links https://github.com/DigiBP/Team-Apples#2-sent-e-mail-with-url-links  | 
| 4   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE04.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE04.png) | The customer then either orders the  30 days free trial license or not. | Row 4, Column 4  | 
| 5   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE05.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE05.png) | Ximiq waits for 14 days for an answer from the customer.   | Row 5, Column 4   | 
| 6   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE06.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE06.png) | If the customer doesn’t reply the opportunity is closed in CRM.   | Row 6, Column 4   | 
| 7   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE07.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE07.png) | The customer orders the 30 days free trial license.   | Row 7, Column 4   | 
| 8   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE08.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE08.png) | A 30 days free trial license key is generated automatically.   | 4. Generate free trial license https://github.com/DigiBP/Team-Apples#4-generate-free-trial-license | 
| 9   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE09.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE09.png) | The 30 days free trial license key is generated and stored in CRM  | 4. Generate free trial license https://github.com/DigiBP/Team-Apples#4-generate-free-trial-license   | 
| 10  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE10.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE10.png) | The 30 days free trial license key is automatically sent to the customer.  | Row 10, Column 4  |  5. Sent free trial license https://github.com/DigiBP/Team-Apples#5-sent-free-trial-license |
| 11  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE11.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE11.png) | Row 11, Column 3  | Row 11, Column 4  | 
| 12  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE12.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE12.png) | The customer then either requests the Live Demo or not.  | Row 12, Column 4  | 
| 13  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE13.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE13.png) |  Time passes until the scheduled Live-Demo.  | Row 13, Column 4  | 
| 14  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE14.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE14.png) | A Ximiq consultant executes the Live-Demo in a video call.   | Row 14, Column 4  | 
| 15  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE15.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE15.png) | Time passes until the 30 days free trial license expires.  | Row 15, Column 4  | 
| 16  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE16.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE16.png) | A form to order the full license is sent automatically to the customer.  | 6. Sent License key order form URL https://github.com/DigiBP/Team-Apples#6-sent-license-key-order-form-url| 
| 17  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE17.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE17.png) | The customer then either orders the full license or not.  | Row 17, Column 4  | 
| 18  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE18.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE18.png) | Ximiq waits for 14 days for an answer from the customer.  | Row 18, Column 4  | 
| 19  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE19.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE19.png) | If the customer doesn’t reply the opportunity is closed in CRM. | Row 19, Column 4 | 
| 20  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE20.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE20.png) | The customers order is received via form.  | Row 20, Column 4 | 
| 21  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE21.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE21.png) | The order is automatically registered in CRM. | Row 21, Column 4 | 
| 22  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE22.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE22.png) |  The price for the full license is calculated and an invoice is created and sent automatically.    | 8. Create Invoice and send https://github.com/DigiBP/Team-Apples#8-create-invoice-and-send| 
| 23  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE23.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE23.png) | The consultant is checking the account manually. | Row 23, Column 4 | 
| 24  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE24.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE24.png) | The customer either paid or not. | Row 24, Column 4 | 
| 25  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE25.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE25.png) | Ximiq waits for 30 days for the payment.  | Row 25, Column 4 | 
| 26  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE26.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE26.png) | If the customer doesn’t pay the opportunity is closed.  | Row 26, Column 4 |
| 27  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE27.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE27.png) | If the customer pays, the full license is generated. | 9. Generate license key https://github.com/DigiBP/Team-Apples#9-generate-license-key | 
| 28  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE28.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE28.png) | The license is registered in CRM. | Row 28, Column 4 | 
| 29  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE29.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE29.png) | The license is automatically sent to the customer. | 10. Sent license key https://github.com/DigiBP/Team-Apples#10-sent-license-key| 
| 30  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE30.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE30.png) | The process is on hold for 330 days.  | Row 30, Column 4 | 
| 31  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE31.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE31.png) | After 330 days a form to renew the license is automatically sent to the customer.  | 11. Sent license renewal form URL https://github.com/DigiBP/Team-Apples#11-sent-license-renewal-form-url | 
| 32  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE32.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE32.png) | The customer then either requests the renewal or not. 3 | Row 31, Column 4 | 
| 33  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE33.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE33.png) | Ximiq waits for 30 days for the order. | Row 31, Column 4 | 
| 34  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE34.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE34.png) | If the customer didn’t order the software request process is finish.  | Row 31, Column 4 | 
| 35  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE35.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE35.png) | The customer orders the renewal. | Row 31, Column 4 | 
| 36  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE36.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE36.png) | Order is registered in CRM | Row 31, Column 4 | 
| 37  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE37.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE37.png) | A Consultant then manually checks the account and updates the date in CRM (task form). | Row 31, Column 4 | 
| 38  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE38.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE38.png) | The customer the either pays or not | Row 31, Column 4 | 
| 39  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE39.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE39.png) | Ximiq waits for 30 days for the payment. | Row 31, Column 4 | 
| 40  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE40.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE40.png) | If the customer doesn’t pay the software request process is finish.  | Row 31, Column 4 | 
| 41  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE41.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE41.png) |  The renewal is the automatically confirmed to the customer.   |  13. Confirm renewal https://github.com/DigiBP/Team-Apples#13-confirm-renewal   | 
| 42  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE42.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE42.png) | The renewal is the automatically registered in CRM. | Row 31, Column 4 | 



# Make (formerly Integromat) -Scenarios
In order to automate the above TOBE BPMN process Integromat has been used to visually create, build and automate the workflow. The scenarios are created by process engine and added to the "external task list" and external worker queries the topic, locks the task, works on it and completes the service task. 

## 1. Start Event - Software request received
- The starting scenario involves watching for new rows in a Google Sheet, which serves as the CRM (Customer Relationship Management) system for XIMIQ.
- When a new row is detected in the Google Sheet, a process instantiation is triggered via a REST call. This means that an instance of a process model in Camunda is created to handle the workflow for the new data.
- As part of the process instantiation, a new business key is generated. The business key is a unique identifier associated with the process instance and can be used for tracking or referencing purposes.
- The information related to the new business key is then sent via an external worker to Camunda. The external worker acts as an interface between the external systems (such as the Google Sheet) and Camunda, allowing for the execution of specific tasks within the workflow.
- Once Camunda receives the information about the new business key from the external worker, it can start managing the workflow according to the defined process model. The process instance can proceed with its predefined steps, such as executing user tasks, making decisions, or invoking external services.

![TO-BE-PROCESS/MAKE-Screenshots/1. Start Event - Software request received.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/1.%20Start%20Event%20-%20Software%20request%20received.png)

<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/1.%20Generate%20Client%20ID.png" width="50%" height="50%">

<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/1.%20Start%20Process.png"  width="50%" height="50%">



## 2. Sent e-mail with URL links
- When a new registry is added to the CRM (Customer Relationship Management) system, a trigger is initiated.
- An email is automatically generated using the "Send an Email" module. The email includes details retrieved from the CRM, such as customer information, order details, or any other relevant data.
- The email is sent to the client without any human interaction. This step is automated, meaning that the system handles it automatically without requiring manual intervention.
- After sending the email, the workflow proceeds to the next step, which involves making an HTTP request to fetch and lock information from Camunda. This could be a service task that retrieves additional data or performs a specific action using an API provided by Camunda.
- The fetched information is then used to complete the service task or execute a specific action. This could involve processing the data, performing calculations, or integrating with other systems.
- Once the service task is completed, the resulting information or outcome is sent back to Camunda. This allows Camunda to update the process instance's state and continue with the workflow based on the completed task.

![TO-BE-PROCESS/MAKE-Screenshots/2. Sent e-mail with URL links.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/2.%20Sent%20e-mail%20with%20URL%20links.png)

## 3. Order free trial license key message
- The client is given the option to request a free trial license.
- If the client decides to proceed with the free trial, they fill out a form indicating their intention.
- The "Watch New Row" module detects the new row or entry in the form.
- The "Watch New Row" module triggers an intermediate catching message event in Camunda.
- The intermediate catching message event in Camunda serves as a waiting state for a specific message to arrive. In this case, it is waiting for the message indicating the client's request for a free trial license.
- Once the intermediate catching message event is triggered, Camunda captures the event and continues with the workflow. 

![TO-BE-PROCESS/MAKE-Screenshots/3. Order free trial license key message.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/3.%20Order%20free%20trial%20license%20key%20message.png)

## 4. Generate free trial license
![TO-BE-PROCESS/MAKE-Screenshots/4. Generate free trial license.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/4.%20Generate%20free%20trial%20license.png)

## 5. Sent free trial license
![TO-BE-PROCESS/MAKE-Screenshots/5. Send free trial license.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/5.%20Send%20free%20trial%20license.png)

## 6. Sent License key order form URL
![TO-BE-PROCESS/MAKE-Screenshots/6. Sending e-mail with form ordering final license.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/6.%20Sending%20e-mail%20with%20form%20ordering%20final%20license.png)

<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/6.%20Difference.png"  width="50%" height="50%">

## 7. Order received message
![TO-BE-PROCESS/MAKE-Screenshots/7. Order received message.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/7.%20Order%20received%20message.png)

## 8. Create Invoice and send
![TO-BE-PROCESS/MAKE-Screenshots/8. Create Invoice and send.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/8.%20Create%20Invoice%20and%20send.png)

<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/8.%20Gmail.png"  width="50%" height="50%">

<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/8.%20Create%20Invoice%20with%20Barcode.png"  width="50%" height="50%">

<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/8.%20Barcode.png"  width="50%" height="50%">


## 9. Generate license key
![TO-BE-PROCESS/MAKE-Screenshots/9. Generate license key.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/9.%20Generate%20license%20key.png)

## 10. Sent license key
![TO-BE-PROCESS/MAKE-Screenshots/10. Sent license key.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/10.%20Sent%20license%20key.png)

## 11. Sent license renewal form URL
![TO-BE-PROCESS/MAKE-Screenshots/11. Sent license renewal form URL.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/11.%20Sent%20license%20renewal%20form%20URL.png)

## 12. Renewing request received
![TO-BE-PROCESS/MAKE-Screenshots/12. Renewing request received.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/12.%20Renewing%20request%20received.png)

## 13. Confirm renewal
![TO-BE-PROCESS/MAKE-Screenshots/13. Confirm renewal.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/13.%20Confirm%20renewal.png)

<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/13.%20Date%20to%20String.png"  width="50%" height="50%">

<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/13.%20Format%20Date.png"  width="50%" height="50%">



# Chatbot

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/1.%20Customer%20Service%20Chatbot.png"  width="75%" height="75%">

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/2.%20What%20it%20solves.png"  width="90%" height="90%">

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/3.%20What%20it%20solves.png"  width="90%" height="90%">

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/4.%20Examples.png"  width="30%" height="30%"> <img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/5.%20Examples.png"  width="30%" height="30%"> <img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/6.%20Examples.png"  width="30%" height="30%">

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/7.%20wix.com.png"  width="90%" height="90%">

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/8.%20Kommunikate.io.png"  width="90%" height="90%">

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Chatbot%20-%20Make%20Screenshot.png"  width="90%" height="90%">

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/9.%20Dialogflow.png"  width="90%" height="90%">




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
