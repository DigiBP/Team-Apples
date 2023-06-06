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

Ximiq was founded in 2013 as a Consulting Firm with the objective of working with customer as partners. The aim of Ximiq is to align Business and IT. This is done through Enterprise Architecture Management. While supporting one of their customers in EAM, Ximiq realized the need to automatically generate reports from the Enterprise Architecture Modelling Tools. At this point, Ximiq developed the ADOIT Report Generator for Microsoft Word. Thanks to the ADOIT Report Generator for Word customers are able to flexibly and quickly create architecture documentation in Microsoft Word by data sourced live from ADOIT. Customers can create their own template structure for their individual use cases or existing project management templates (e.g. Hermes) and create deliverables automatically. Instead of compiling their lists and data manually, customers can have it automatically inserted and updated from one single reliable source. 

<img src="https://github.com/DigiBP/Team-Apples/blob/a7366a9b4432520cdf6009083acb7db741415361/AS-IS-PROCESS/ICON.svg"  width="50%" height="50%">

The sales process for the Generator Software is currently at an Ad-hoc stage, meaning that roles and responsibilities are yet to be defined in order to increase pipeline and ultimately business. Throughout this process, we realized that Ximiq doesn’t have the resources for a dedicated Sales Team and the sales engagement is fully managed by consultants. That is the reason why Ximiq needs to implement a lean and streamlined process to better allocate resources.  

 
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

When the Apples Group met with Ximiq, they discovered that their business process did not have any process model  or workflow integration behind. Therefore, the Group created a best effort AS-IS BPMN process with the information they received from Ximiq. BPMN stands for Business Process Model and Notation. It is a standardized graphical notation used for modeling business processes in a visual format. BPMN provides a set of symbols and rules to represent various elements of a business process, such as activities, events, gateways, and flows. Overall, BPMN helps organizations improve process efficiency, identify bottlenecks, and streamline operations by providing a clear and standardized representation of business processes. 

![AS-IS-PROCESS/01_AS-IS_Sales Process ADOIT RGfW.png](https://github.com/DigiBP/Team-Apples/blob/4d466a928f8c591dfe7c846aaeca9fe214f92d3c/AS-IS-PROCESS/01_AS-IS_Sales%20Process%20ADOIT%20RGfW.png)


Description of AS-IS Process Elements, Problems and Possible Improvements
========

| Row | Picture | Description          | Problems & Possible Improvements          |
| --- | ------- | ---------------- | ---------------- |
| 1   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS01.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS01.png) | Potential customers can download the application in the Microsoft AppSource Marketplace. It can be installed and added to Microsoft Word but has to be activated by a license key before its usable. https://smp-prod-pb-cac.azurewebsites.net/en-us/product/office/WA200004614?tab=Overview&exp=ubp8   |  | 
| 2   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS02.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS02.png) | Potential customers can request the application via the BOC-Marketplace. BOC is the company that develops ADOIT. This will generate an email sent to Ximiq. The following is the content of the email: Form of address, First Name, Last Name, Email, Organization, Country, Telephone, Messsage.  https://knowledge.boc-group.com/de/module/adoit-word-report-generator/ | This doesn’t automatically trigger the creation of a Lead in CRM | 
| 3   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS03.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS03.png) | Ximiq has several partners (other consultants and resellers of ADOIT) who recommend the Report Generator to their customers. Requests from them arrive via various channels (email, phone, teams chat or verbal). | This doesn’t automatically trigger the creation of a Lead in CRM and is difficult to automate since the data input is unstructured.  | 
| 4   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS04.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS04.png) | If a potential customer downloads the application in the Microsoft AppSource Marketplace, a new lead is automatically generated in Ximiqs CRM-System (Microsoft Dynamics) via API.  | No message for the consultant. Quality of entry is not sufficient yet but can be fixed.    | 
| 5   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS05.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS05.png) | Since there is no message arriving when leads are generated, the consultants have to check whether new leads arrived and if the entries are of good quality.   | This process step is a waste that can be eliminated by automatically informing the consultant when a new lead is created. | 
| 6   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS06.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS06.png) | In the cases when the leads aren’t generated automatically a consultant creates a new lead in CRM.  | This can be automated with no human involvement.| 
| 7   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS07.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS07.png) | In all cases an initial email with the following content is sent to the customer : Download-link, Pricing information, Trial information, Technical questions, Link to book a live demo appointment   | Since it’s a standard email for any customer this process step can be automized. | 
| 8   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS08.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS08.png) | When clicking the link in the initial email a customer gets access to a booking tool connected to the customers outlook calendar. The following content appears in the booking tool:  dropdown to choose a consultant, free slots for live demo, Name, Email, Address, Phone number, Notes, ADOIT Version (OnPremis/Cloud) | This is an automated form which could be integrated into the Groups solution. Since there are some limitations, this form will not be used in this solution.   | 
| 9   | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS09.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS09.png) | If the customer sends the form an appointment and a Teams call link is automatically generated in Outlook. https://outlook.office365.com/owa/calendar/Sales1@ximiq.ch/bookings/  (do not book a live demo!)  |  This is an automated form which could be integrated into the Groups solution.  | 
| 10  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS10.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS10.png) | The potential customer has the chance to book an appointment via booking-link from the initial email. |  |
| 11  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS11.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS11.png) | The live demo is held via Teams. In this call the consultant demonstrates the generator and answers the customers questions. |   | 
| 12  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS12.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS12.png) | The potential customer has the chance to request a 30days trial license to try out the ADOIT Report Generator for Word.  |  | 
| 13  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS13.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS13.png) | After sending the initial email Ximiq waits two weeks for an answer. |   | 
| 14  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS14.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS14.png) | If the customer doesn’t answer within two weeks a reminder/follow-up email is sent. | This process step could be eliminated as it is over-processing. If client is interested they would come back.   | 
| 15  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS15.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS15.png) | After sending the reminder email Ximiq waits two weeks for an answer.  |   | 
| 16  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS16.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS16.png) | The customer either orders the license, the trial license or doesn’t reply. |  | 
| 17  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS17.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS17.png) | The Trial license key is generated via https://guidgenerator.com/ and registered in Postman. The license key is a 32 digit number.  | This process step could be automated.  | 
| 18  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS18.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS18.png) | The license key and a users handbook is sent to the customer by email.   | This process step could be automated.   | 
| 19  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS19.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS19.png) | The customer can try the report generator for 30 days. The consultant then sends a follow up email. | Does not automatically remind the Consultant. |
| 20  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS20.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS20.png) | A follow up email is sent to the customer with the following content: Asking how they liked the Report Generator, Pricing information |   This can be integrated already in previous emails. No need for additional emails.  |
| 21  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS21.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS21.png) | The customer either orders the license or not.  | Does not automatically remind the Consultant. |
| 22  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS22.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS22.png) | If the customer isn’t interested in buying the license the opportunity is closed as lost in CRM. | This process could be automated. | 
| 23  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS23.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS23.png) | If the customer wants to order the Report Generator the order is registered in CRM.  | This can be automated with no human involvement. | 
| 24  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS24.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS24.png) | The Price is calculated based on the following pricing model: Single User: USD 360.00 p.a; Team 10: USD 2520.00 p.a; Team 10: USD 5400.00 p.a; Unlimited: upon request;   | The calculation could be done automatically based on employee size within the order entry in CRM. | 
| 25  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS25.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS25.png) | The consultant informs the accountant about the new order via email. | This process step could be automated. | 
| 26  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS26.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS26.png) | The accountant creates the invoice in the ERP-System.| This could be fully automated. | 
| 27  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS27.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS27.png) | The accountant forwards the invoice to the consultant via email. | The accountant could send the invoice directly to the customer. Or it could even be automated fully with no human involvement. | 
| 28  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS28.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS28.png) | The consultant sends the invoice to the customer.  | The accountant could send the invoice directly to the customer. Or it could even be automated fully with no human involvement. | 
| 29  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS29.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS29.png) | waiting up to 30 days for payment | Does not automatically remind the Consultant. | 
| 30  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS30.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS30.png) | The customer then either pays or not. | Does not automatically remind the Consultant to check the account. | 
| 31  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS31.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS31.png) | If the customer doesn’t pay a reminder is sent. | This process step could be eliminated as it is over-processing. If client is interested they would come back. | 
| 32  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS32.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS32.png) | After the reminder is sent Ximiq waits another 14 days for the payment.| Does not automatically remind the Consultant. | 
| 33  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS33.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS33.png) | The customer pays. |  |
| 34  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS34.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS34.png) |  If the client pays and if the accounting team receives a notification that a payment has been made the accountant informs the consultant.  | The notification could also be sent directly to the Consultant.  | 
| 35  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS35.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS35.png) | The license key is generated via https://guidgenerator.com/ and is then registered in Postman together with the validity date and the number of users. Via Postman API the validity of the license will be checked when it is activated the first time as well as whenever the application is used.| This can be improved by automating and saving time for the Consultants' business as usual. |
| 36  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS36.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS36.png) | The consultant sends the license key, a user handbook as well as a installation handbook to the customer. | This process step could be fully automated. |
| 37  | ![AS-IS-PROCESS/SCREENSHOTS-PROCESS-ELEMENTS/ASIS37.png](https://github.com/DigiBP/Team-Apples/blob/c359fb74a7a2e72c2f18677aa13f3012f2183d54/AS-IS-PROCESS/Screenshots-Process-Elements/ASIS37.png) | In the CRM the status of the opportunity is set to “won”. |  |


# AS-IS Business Process Problems 
When analysing the AS-IS process to do a lean process improvement several questions came up. 
- First of all Ximiq has a lot of wastes in its sales process. 
- Besides some automated tasks in the process most of the tasks are manually and the clients have no added value for themselves. 
- The only value adding tasks in the process are the Demo done by the Consultant for the client, the license keys the client receives and the price information. 
- There is a lot of transportation wast, wasted potentials of Consultants and Accountants, waiting time for the client and over-processing such as sending reminders to clients. 
- The 3 trigger points seem not to be synchronized and needs to be merged at some point manually. 
- Accounting seems to do everything manually and there is again a transportation between Accounting and Consulting department. 
- Several tasks are not automated and the Consultants do not receive any reminders to make sure to contact the client after e.g. 30 days of trial phase. 

![AS-IS-PROCESS/02_Wastes in AS-IS Process.png](https://github.com/DigiBP/Team-Apples/blob/3dc488e1addcc066fbbe203cab2336ef6cbf9227/AS-IS-PROCESS/02_Wastes%20in%20AS-IS%20Process.png)


# TO-BE Process Description


![TO-BE-PROCESS/01_TO-BE_Sales Process ADOIT Report Generator for Word.png](https://github.com/DigiBP/Team-Apples/blob/420ef52f89b387d3727006403113fcd08eb692cd/TO-BE-PROCESS/01_TO-BE_Sales%20Process%20ADOIT%20Report%20Generator%20for%20Word.png)




Description of TO-BE Process Elements and Final Solutions
========

| Row | Picture | Description          | Solution / Comment          | 
| --- | ------- | ---------------- | ---------------- | 
| 1   |   ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE01.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE01.png) | During any partners download process the customer filled the contact form.   |  1. Start Event - Software request received https://github.com/DigiBP/Team-Apples#1-start-event---software-request-received| 
| 2   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE02.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE02.png) |  Customers information is stored in CRM. | 1. Start Event - Software request received https://github.com/DigiBP/Team-Apples#1-start-event---software-request-received  | 
| 3   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE03.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE03.png) | An initial email is sent to the customer. The email includes a link to order a 30 days free trial license as well as scheduling a Live-Demo.  | 2. Sent e-mail with URL links https://github.com/DigiBP/Team-Apples#2-sent-e-mail-with-url-links  | 
| 4   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE04.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE04.png) | The customer then either orders the  30 days free trial license or not. | Event based gateway waits until one of the messages get triggered. Without any message triggering the tocken will remain at the gateway. | 
| 5   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE05.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE05.png) | Ximiq waits for 14 days for an answer from the customer.   | Going back to the client could be an option but that would stop the consultant from doing more important things such as executing Demos for existing clients.   | 
| 6   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE06.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE06.png) | If the customer doesn’t reply the opportunity is closed in CRM.   | It is up to the consultant to decide when to contact clients personally but it does not make sense to run after every client to win the opportunity.  | 
| 7   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE07.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE07.png) | The customer orders the 30 days free trial license.   | This is done via Google form and triggers the message intermediate catch event.  | 
| 8   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE08.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE08.png) | A 30 days free trial license key is generated automatically.   | 4. Generate free trial license https://github.com/DigiBP/Team-Apples#4-generate-free-trial-license | 
| 9   | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE09.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE09.png) | The 30 days free trial license key is generated and stored in CRM  | 4. Generate free trial license https://github.com/DigiBP/Team-Apples#4-generate-free-trial-license   | 
| 10  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE10.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE10.png) | The 30 days free trial license key is automatically sent to the customer.  | 5. Sent free trial license https://github.com/DigiBP/Team-Apples#5-sent-free-trial-license |
| 11  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE11.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE11.png) | Call client for Demo request is a User task.   | This User task includes all the details and needs to be completed before the tocken can move on. | 
| 12  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE12.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE12.png) | The customer then either requests the Live Demo or not.  | This needs to be indicated in the User task in the Task list.  | 
| 13  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE13.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE13.png) | Time passes until the scheduled Live-Demo.  | Until then the User task Live demo Executed remains in the task list of the consultant.  | 
| 14  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE14.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE14.png) | A Ximiq consultant executes the Live-Demo in a video call.   | User task needs to be completed in the Task List.  | 
| 15  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE15.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE15.png) | Time passes until the 30 days free trial license expires.  | Automatically calculated by the scenario 6.  | 
| 16  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE16.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE16.png) | A form to order the full license is sent automatically to the customer.  | 6. Sent License key order form URL https://github.com/DigiBP/Team-Apples#6-sent-license-key-order-form-url| 
| 17  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE17.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE17.png) | The customer then either orders the full license or not.  | Event based gateway waits until one of the messages get triggered. Without any message triggering the tocken will remain at the gateway.  | 
| 18  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE18.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE18.png) | Ximiq waits for 14 days for an answer from the customer.  | Going back to the client could be an option but that would stop the consultant from doing more important things such as executing Demos for existing clients.  | 
| 19  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE19.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE19.png) | If the customer doesn’t reply the opportunity is closed in CRM. | It is up to the consultant to decide when to contact clients personally but it does not make sense to run after every client to win the opportunity. | 
| 20  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE20.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE20.png) | The customers order is received via form.  | Row 20, Column 4 | 
| 21  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE21.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE21.png) | The order is automatically registered in CRM. | Row 21, Column 4 | 
| 22  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE22.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE22.png) |  The price for the full license is calculated and an invoice is created and sent automatically.    | 8. Create Invoice and send https://github.com/DigiBP/Team-Apples#8-create-invoice-and-send| 
| 23  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE23.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE23.png) | The consultant is checking the account manually. | This is a good control point to manage the revenues of each Consultant. The User Task needs to be completed. | 
| 24  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE24.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE24.png) | The customer either paid or not. |  To be indicated in the User Task in the Task list. | 
| 25  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE25.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE25.png) | Ximiq waits for 30 days for the payment.  |  It is up to the Consultant to call the client or not. | 
| 26  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE26.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE26.png) | If the customer doesn’t pay the opportunity is closed.  | It is up to the Consultant to call the client or not, it always depends on the client portofolio situation of the Consultant. |
| 27  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE27.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE27.png) | If the customer pays, the full license is generated. | 9. Generate license key https://github.com/DigiBP/Team-Apples#9-generate-license-key | 
| 28  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE28.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE28.png) | The license is registered in CRM. | 9. Generate license key https://github.com/DigiBP/Team-Apples#9-generate-license-key | 
| 29  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE29.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE29.png) | The license is automatically sent to the customer. | 10. Sent license key https://github.com/DigiBP/Team-Apples#10-sent-license-key| 
| 30  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE30.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE30.png) | The process is on hold for 330 days.  | Client can anytime get in touch with the Chatbot for questions or problems. | 
| 31  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE31.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE31.png) | After 330 days a form to renew the license is automatically sent to the customer.  | 11. Sent license renewal form URL https://github.com/DigiBP/Team-Apples#11-sent-license-renewal-form-url | 
| 32  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE32.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE32.png) | The customer then either requests the renewal or not. | Event based gateway waits until one of the messages get triggered. Without any message triggering the tocken will remain at the gateway. | 
| 33  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE33.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE33.png) | Ximiq waits for 30 days for the order. | Going back to the client could be an option but that would stop the consultant from doing more important things such as executing Demos for existing clients. | 
| 34  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE34.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE34.png) | If the customer didn’t order the software request process is finish.  | It is up to the Consultant to call the client or not, it always depends on the client portofolio situation of the Consultant. | 
| 35  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE35.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE35.png) | The customer orders the renewal. | Message Intermediate catching event should be triggered. | 
| 36  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE36.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE36.png) | Order is registered in CRM | Row 31, Column 4 | 
| 37  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE37.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE37.png) | A Consultant then manually checks the account and updates the date in the Task list. | Task list will notify automatically via Custom webhook the last scenario which will then trigger the service task "Confirm renewal" and write back the new expiry date into CRM | 
| 38  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE38.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE38.png) | The customer the either pays or not | It is up to the Consultant to call the client or not, it always depends on the client portofolio situation of the Consultant. | 
| 39  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE39.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE39.png) | Ximiq waits for 30 days for the payment. | It is up to the Consultant to call the client or not, it always depends on the client portofolio situation of the Consultant. | 
| 40  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE40.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE40.png) | If the customer doesn’t pay the software request process is finish.  | It is up to the Consultant to call the client or not, it always depends on the client portofolio situation of the Consultant. | 
| 41  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE41.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE41.png) |  The renewal is the automatically confirmed to the customer.   |  13. Confirm renewal https://github.com/DigiBP/Team-Apples#13-confirm-renewal   | 
| 42  | ![TO-BE-PROCESS/BPMN-SCREENSHOTS/TOBE42.png](https://github.com/DigiBP/Team-Apples/blob/fd3b11aaf18135496621c8368adca24553044478/TO-BE-PROCESS/BPMN-Screenshots/TOBE42.png) | The renewal is the automatically registered in CRM. | 13. Confirm renewal https://github.com/DigiBP/Team-Apples#13-confirm-renewal  | 

# Make (formerly Integromat) - Scenarios
In order to automate the above TO-BE BPMN process's service tasks and message events, Integromat was utilized to visually create, build, and automate the workflow. The workflow entails coordinating humans, resources, and information to achieve a specific objective. Each task or activity within the workflow relies on the successful completion of preceding tasks or the occurrence of specific events, such as receiving a lead from a potential client.

In Integromat, scenarios are created using the process engine and added to the "external task list". An external worker then queries the topic, locks the task, performs the necessary work, and completes the service task within Camunda BPMN. On the other hand, user tasks are directly handled by the BPMN engine.


## 1. Start Event - Software request received
- When client decides to request the software, they will fill in a Google Form as a starting point.
- The starting scenario involves watching for new rows in a Google Sheet, which serves as the CRM (Customer Relationship Management) system for Ximiq.
- When a new row is detected in the Google Sheet, a process instantiation is triggered via a REST call. This means that an instance of a process model in Camunda is created to handle the workflow for the new data.
- As part of the process instantiation, a new business key is generated. The business key is a unique identifier associated with the process instance and can be used for tracking or referencing purposes.
- The information related to the new business key is then sent via an external worker to Camunda. The external worker acts as an interface between the external systems (such as the Google Sheet) and Camunda, allowing for the execution of specific tasks within the workflow.
- Once Camunda receives the information about the new business key from the external worker, it can start managing the workflow according to the defined process model. The process instance can proceed with invoking the first external services task "Sent free license key URL".

### Google Form
<img src="https://github.com/DigiBP/Team-Apples/blob/097a99c54c4f1473a525fd9840ff0b9ba86b0463/TO-BE-PROCESS/Google-Forms-Screenshots/00_Starting_Form.png"  width="50%" height="50%">

### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/1. Start Event - Software request received.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/1.%20Start%20Event%20-%20Software%20request%20received.png)

### CRM - Google Sheet Starting Data
![TO-BE-PROCESS/Google-Sheets-Screenshots/00_CRM.png](https://github.com/DigiBP/Team-Apples/blob/097a99c54c4f1473a525fd9840ff0b9ba86b0463/TO-BE-PROCESS/Google-Sheets-Screenshots/00_CRM.png)

The Google Form only updates the field in Google Sheet that are filled in by the client the other fields such as Price and Client ID and also License Key and Renewal Date are updated with the Module Google Sheet - Update a Row.

#### Scenario Module Tools - Generation Business Key 
<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/1.%20Generate%20Client%20ID.png" width="50%" height="50%">

### Scenario Module Google Sheet - Update Client ID and calculate Price


Picture to be added!!!!!!!!@cédric 

#### Scenario Module HTTP - Make a request to Camunda
<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/1.%20Start%20Process.png"  width="50%" height="50%">


## 2. Sent e-mail with URL links
- When a new registry is added to the CRM system, a trigger is initiated.
- An email is automatically generated using the "Send an Email" module. The email includes details retrieved from the CRM, such as customer information, order details, or any other relevant data.
- The email is sent to the client without any human interaction. This step is automated, meaning that the system handles it automatically without requiring manual intervention.
- After sending the email, the workflow proceeds to the next step, which involves making an HTTP request to fetch and lock information from Camunda BPMN engine.
- The fetched information is then used to complete the service task.
- Once the service task is completed, the resulting information or outcome is sent back to Camunda. This allows Camunda to update the process instance's state and continue with the workflow, in this case the next event is the message intermediate catch event "Free trial License order received" which waits for a message to be received. 

### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/2. Sent e-mail with URL links.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/2.%20Sent%20e-mail%20with%20URL%20links.png)

### First E-mail to client with Google Form URL
- The e-mail always refers to the Chatbot in case the client has issues or questions they can get in touch with the Chatbot.

<img src="https://github.com/DigiBP/Team-Apples/blob/e0b465c7025875559349c3bf35189fb21940c24e/TO-BE-PROCESS/E-Mail-Schreenshots/02_Software%20Request.png" width="50%" height="50%">

## 3. Order free trial license key message
- The client is given the option to request a free trial license via Google Form.
- The "Watch New Row" module detects the new entry in Google Sheet.
- The intermediate catching message event in Camunda serves as a waiting state for a specific message to arrive. In this case, it is waiting for the message indicating the client's request for a free trial license via a message post.
- Once the intermediate catching message event is triggered, Camunda captures the event and continues with the workflow. 

### Google Form
<img src="https://github.com/DigiBP/Team-Apples/blob/b46ba03d6847fcf93072fb754b7cca9defc1a79e/TO-BE-PROCESS/Google-Forms-Screenshots/02_Free_Trial_License.png" width="50%" height="50%">

### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/3. Order free trial license key message.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/3.%20Order%20free%20trial%20license%20key%20message.png)


## 4. Generate free trial license
- The free trial license is being generated using a UUID (Universally Unique Identifier). A UUID is a unique identifier that ensures each generated license has a distinct value.
- After generating the free trial license with the UUID, the generated license information is written back into the CRM (Customer Relationship Management) system.
- Writing the license information back into the CRM allows for proper tracking and management of the free trial licenses. It ensures that the generated licenses are associated with the respective clients or organizations.
- The CRM system can store the generated license information, including the UUID, client details, and any other relevant information tied to the free trial license.

### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/4. Generate free trial license.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/4.%20Generate%20free%20trial%20license.png)

### CRM - Google Sheet Free Trial License
![TO-BE-PROCESS/Google-Sheets-Screenshots/02_CRM.png](https://github.com/DigiBP/Team-Apples/blob/097a99c54c4f1473a525fd9840ff0b9ba86b0463/TO-BE-PROCESS/Google-Sheets-Screenshots/02_CRM.png)


## 5. Sent free trial license
- The process starts with an HTTP make a request step, where Integromate makes a request to fetch and lock relevant information, including the license key, from a Google Sheet or CRM system.
- The HTTP request fetches the necessary details from the Google Sheet or CRM system, such as the client's information and the generated license key.
- Once the information is retrieved, Camunda proceeds with the workflow and uses the obtained data.
- As part of the workflow, an email is automatically sent to the client immediately as soon as the preceding scenario is finished. 
- The Custom Webhook assures a smooth and faster sending of the License Key E-mail.
- The email content is composed using the retrieved details from the Google Sheet or CRM, and it includes the generated free license key.


### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/5. Send free trial license.png](https://github.com/DigiBP/Team-Apples/blob/52999f1baade0f6eb8c914de3e85cf57910ea5c7/TO-BE-PROCESS/MAKE-Screenshots/5.%20Send%20free%20trial%20license.png)

### E-mail Free Trial License Key
- The e-mail always refers to the Chatbot in case the client has issues or questions they can get in touch with the Chatbot.

<img src="https://github.com/DigiBP/Team-Apples/blob/e0b465c7025875559349c3bf35189fb21940c24e/TO-BE-PROCESS/E-Mail-Schreenshots/05_Fee%20Trial%20License%20Key.png"  width="50%" height="50%">


## 6. Sent License key order form URL
- The client has a 30-day free trial license and once that is expired this scenario calculates with "Tool" modules the number of remaining days. 
- It calculates today minus the license start date and defines if it is expired or not.
- Once the remaining days are zero, an email is automatically sent to the client.
- The email contains a URL that directs the client to a Google form where they can order the one-year license key.
- To accomplish this, the scenario utilizes two HTTP make a request steps: fetch and lock, and complete in order to communicate with Camunda and make sure the correct business key is processed. 
- After composing the email, the scenario completes the HTTP request by sending the email to the client.
- The client receives the email, which includes the URL to the Google form, allowing them to order the one-year license key.


### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/6. Sending e-mail with form ordering final license.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/6.%20Sending%20e-mail%20with%20form%20ordering%20final%20license.png)

#### Scenario Module Tools - Calculation Free Trial License duration 
<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/6.%20Difference.png"  width="50%" height="50%">

### E-mail Expiration Free Trial License
- The e-mail always refers to the Chatbot in case the client has issues or questions they can get in touch with the Chatbot.

<img src="https://github.com/DigiBP/Team-Apples/blob/e0b465c7025875559349c3bf35189fb21940c24e/TO-BE-PROCESS/E-Mail-Schreenshots/06_Free%20License%20expired%20Link%20to%20order%20yearly%20License.png"  width="50%" height="50%">


## 7. Order received message
- The client is given the option to request a one yearly license, which is no longer free.
- If the client decides to proceed with the yearly license, they fill out a form indicating their intention.
- The "Watch New Row" module detects the new row or entry in CRM.
- The "Watch New Row" module triggers an intermediate catching message event in Camunda.
- The intermediate catching message event in Camunda serves as a waiting state for a specific message to arrive. In this case, it is waiting for the message indicating the client's request for a yearly license key.
- Once the intermediate catching message event is triggered, Camunda captures the event and continues with the workflow in this case the service task "Create and sent Invoice". 

### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/7. Order received message.png](https://github.com/DigiBP/Team-Apples/blob/53080c6a715c2e99104000f13f0dffe02d081155/TO-BE-PROCESS/MAKE-Screenshots/7.%20Order%20received%20message.png)

### Google Form
<img src="https://github.com/DigiBP/Team-Apples/blob/097a99c54c4f1473a525fd9840ff0b9ba86b0463/TO-BE-PROCESS/Google-Forms-Screenshots/06_Ordering%20final%20License.png" width="50%" height="50%">

### CRM - Google Sheet License Ordering
![TO-BE-PROCESS/Google-Sheets-Screenshots/06_CRM.png](https://github.com/DigiBP/Team-Apples/blob/097a99c54c4f1473a525fd9840ff0b9ba86b0463/TO-BE-PROCESS/Google-Sheets-Screenshots/06_CRM.png)


## 8. Create Invoice and send
- The scenario initiates an HTTP make a request step to fetch and lock the business key and topic name from Camunda. This step allows the workflow to access the necessary information for further processing.
- With the fetched information, the scenario proceeds to create an Invoice Number. This could involve generating a unique identifier or following a specific numbering scheme.
- Additionally, the scenario generates a Barcode associated with the invoice. This Barcode serves as a reference for scanning purposes.
- The Barcode is saved in Google Drive. This step ensures that the Barcode is securely stored and can be easily accessed or referenced later in the payment information.
- The scenario continues by creating an invoice using the generated Invoice Number and Barcode. The invoice contains relevant details such as client ID, product name, pricing, and Invoice Number. 
- The created invoice is saved as a PDF file. This allows for easy sharing, printing, and archiving of the invoice document.
- The scenario writes back the Invoice Number and the document ID of the saved invoice in Google Sheet. This step updates the Google Sheet with the relevant invoice information for tracking and reference purposes.
- An email is then sent to the recipient, attaching the generated invoice as a PDF file. The e-mail includes the details of the payment. 
- Finally, the scenario completes the process with another HTTP make a request, indicating the successful completion of the workflow.


### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/8. Create Invoice and send.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/8.%20Create%20Invoice%20and%20send.png)

#### Scenario Module Barcodes - Generate Barcode and save in Google Drive
<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/8.%20Barcode.png"  width="50%" height="50%">

#### Scenario Module Google Documents - Create a Document with Barcode (Thumbnail Link)
<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/8.%20Create%20Invoice%20with%20Barcode.png"  width="50%" height="50%">

#### Scenario Module Gmail - Sent an e-mail including Invoice attachement
<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/8.%20Gmail.png"  width="50%" height="50%">

### E-mail sent with Invoice
- The e-mail always refers to the Chatbot in case the client has issues or questions they can get in touch with the Chatbot.

<img src="https://github.com/DigiBP/Team-Apples/blob/e0b465c7025875559349c3bf35189fb21940c24e/TO-BE-PROCESS/E-Mail-Schreenshots/08_Invoice%20Number.png"  width="50%" height="50%">

### Invoice created with Price and Quantity information
<img src="https://github.com/DigiBP/Team-Apples/blob/e0b465c7025875559349c3bf35189fb21940c24e/TO-BE-PROCESS/E-Mail-Schreenshots/08_Invoice%20(Attachment).png"  width="50%" height="50%">


## 9. Generate license key
- The client decides to purchase a license key after paying for it.
- Once the payment is completed, a new license key is generated.
- The generated license key is then written back into the CRM system.
- The license key is associated with the client's credentials in the CRM system, ensuring it is properly linked to the client's profile.

### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/9. Generate license key.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/9.%20Generate%20license%20key.png)


## 10. Sent License Key
- With this scenario the license key is retrieved from the CRM and sent via E-mail to the client immediately as soon as the preceding scenario is finished. 
- The Custom Webhook assures a smooth and faster sending of the License Key E-mail. 
- The email content is composed using the retrieved details from the Google Sheet or CRM, and it includes the generated license key.


### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/10. Sent license key.png](https://github.com/DigiBP/Team-Apples/blob/52999f1baade0f6eb8c914de3e85cf57910ea5c7/TO-BE-PROCESS/MAKE-Screenshots/10.%20Sent%20license%20key.png)

### E-mail License Key 
- The e-mail always refers to the Chatbot in case the client has issues or questions they can get in touch with the Chatbot.

<img src="https://github.com/DigiBP/Team-Apples/blob/e0b465c7025875559349c3bf35189fb21940c24e/TO-BE-PROCESS/E-Mail-Schreenshots/10_License%20Key.png"  width="50%" height="50%">


## 11. Sent license renewal form URL

- After 330 days just 30 days before the expiration of the yearly license key this scenario automatically sents a renewal licens URL Link to the client via E-mail. 
- The email content is composed using the retrieved details from the CRM, and it includes the price information to be paid, if renewal is requested. 

### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/11. Sent license renewal form URL.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/11.%20Sent%20license%20renewal%20form%20URL.png)

### E-mail Expiration License Key and Renewal URL
- The e-mail always refers to the Chatbot in case the client has issues or questions they can get in touch with the Chatbot.

<img src="https://github.com/DigiBP/Team-Apples/blob/e0b465c7025875559349c3bf35189fb21940c24e/TO-BE-PROCESS/E-Mail-Schreenshots/11_License%20Key%20expiration%20in%2030%20days.png"  width="50%" height="50%">

## 12. Renewing request received
- The client is given the option to renew the existing yearly license key. 
- If the client decides to renew the license key, they fill out a form indicating their intention.
- The "Watch New Row" module detects the new row or entry in CRM.
- The "Watch New Row" module triggers an intermediate catching message event in Camunda.
- The intermediate catching message event in Camunda serves as a waiting state for a specific message to arrive. In this case, it is waiting for the message indicating the client's request for a yearly license key.
- Once the intermediate catching message event is triggered, Camunda captures the event and continues with the workflow in this case the user task "Confirm payment and renew license" will appear in the task list of the Consultant. 


### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/12. Renewing request received.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/12.%20Renewing%20request%20received.png)

### Google Form
<img src="https://github.com/DigiBP/Team-Apples/blob/b46ba03d6847fcf93072fb754b7cca9defc1a79e/TO-BE-PROCESS/Google-Forms-Screenshots/11_License_renewal.png" width="50%" height="50%">

### CRM - Google Sheet Renew License Key
![TO-BE-PROCESS/Google-Sheets-Screenshots/11_CRM.png](https://github.com/DigiBP/Team-Apples/blob/097a99c54c4f1473a525fd9840ff0b9ba86b0463/TO-BE-PROCESS/Google-Sheets-Screenshots/11_CRM.png)


## 13. Confirm renewal
- Within this scenario the immediate trigger is once data arrives from the previous event fetched and locked from Camuda engine. In this case it is a user task in which a new date is confirmed or not.
- If the Consultant confirms the renewal of the license then this scenario is formating the date and writting it back to CRM.
- Once the previous modules are done the client receives within this scenario an automatic confirmation e-mail with the new expiration date. 
- The email content is composed using the retrieved details from CRM, and it includes the newly formated expiration date. 

### Scenario
![TO-BE-PROCESS/MAKE-Screenshots/13. Confirm renewal.png](https://github.com/DigiBP/Team-Apples/blob/1546a24de3f3222c595b6a0c8fbc52b69e984a95/TO-BE-PROCESS/MAKE-Screenshots/13.%20Confirm%20renewal.png)

#### Scenario Module Tools - Set variable Date to String
<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/13.%20Date%20to%20String.png"  width="50%" height="50%">

#### Scenario Module Tools - Set variable Fromat Date
<img src="https://github.com/DigiBP/Team-Apples/blob/c19ac9acfcf5427fa8143a7f42124891f7619a22/TO-BE-PROCESS/MAKE-Screenshots/Details/13.%20Format%20Date.png"  width="50%" height="50%">

### E-mail Confirmation renewal of License Key
- The e-mail always refers to the Chatbot in case the client has issues or questions they can get in touch with the Chatbot.

<img src="https://github.com/DigiBP/Team-Apples/blob/e0b465c7025875559349c3bf35189fb21940c24e/TO-BE-PROCESS/E-Mail-Schreenshots/13_Confirmation%20renewal%20License%20Key.png"  width="50%" height="50%">

# Chatbot
The Chatbot helps to solve any potential problem the customers may face throughout the sales cycle using an interactive frontend website. These are issues such as:
- Accessing ordering forms for our software license: trial, purchase and renewal
- Difficulties to use the software
- Licenses were not sent to the customer/ didn’t receive/lost them
- The customer needs to talk chat/video call with us
- The customer doesn’t receive/understand our invoices

Solutions were mapped all along sales cycle to ensure the customer always gets an answer. More than 17 different type of problems were identified with at least 4 different inputs from the customer.

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/2.%20What%20it%20solves.png"  width="90%" height="90%">

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/3.%20What%20it%20solves.png"  width="90%" height="90%">

Here are some chat hisory examples: 

<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/4.%20Examples.png"  width="30%" height="30%"> <img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/5.%20Examples.png"  width="30%" height="30%"> <img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/6.%20Examples.png"  width="30%" height="30%">

The following tools were used:
- Frontend using WIX.com website and HTML code to add Kommunicate.io as a widget
- Chatbot Interface using Kommunicate.io
- Webhooks using Make.com to Fill Google sheets, search rows and use Reponse fulfillment
- Chatbot natural language understanding platform using Google Dialogflow

The following automations were done:
- Provides user Manual to Customer - integrated link
- Records Company ID and email in Google Sheets for Customer Service get in contact with client
- In case the customer urgently needs assistance, it automatically handsover the conversation to a live agent using Kommunicate.io.
- Provides customer's trial license in case they didnt get it, using search rows and response fulfillment
- Provides an appointment scheduler using Google Calendar in case customer needs to reschedule or missed the live demo - integrated link

### WIX.com
<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/7.%20wix.com.png"  width="90%" height="90%">

### Kommunicate.io
<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/8.%20Kommunikate.io.png"  width="90%" height="90%">

### Dialogflow
<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Chatbot%20-%20Make%20Screenshot.png"  width="90%" height="90%">

### make.com
<img src="https://github.com/DigiBP/Team-Apples/blob/811e7d6c4fe3021648fd8a5305d04f5f5ad0b963/CHATBOT-Files/Screenshots/9.%20Dialogflow.png"  width="90%" height="90%">

### Google Calendar, Google Forms, Google Sheets
<img src="https://github.com/DigiBP/Team-Apples/blob/73a2b174b6e706d5762de81f862105f0b9e240ee/CHATBOT-Files/Screenshots/10.%20Google%20Calendar%2C%20Forms%2C%20Sheet.png"  width="90%" height="90%">

# Conclusion 
The process has been improved massively and if Ximiq would give the Group Apples the time used for each user task the Group could have calculated the 
Flow Efficiency (%) = Value added Time   / Process Lead Time (total time needed to fulfill a customer order) 
Looking at all the manual tasks that probably costed a lot of time the flow efficiency with the TOBE process is massivelly better than the AS-IS process. 





# List of Artifacts and Presentation
Artifacts:

1. [BPMN-Files (AS-IS & TO-BE)](https://github.com/DigiBP/Team-Apples/tree/8f019e16a5874df54c8768ca8b76a117889c4a79/BPMN-Files)
2. [MAKE-Scenario Blueprints (.json)](https://github.com/DigiBP/Team-Apples/tree/8f019e16a5874df54c8768ca8b76a117889c4a79/MAKE-Blueprint%20Exports)
3. [Workflow-Documentation Video (download)](https://github.com/DigiBP/Team-Apples/blob/8f019e16a5874df54c8768ca8b76a117889c4a79/TO-BE-PROCESS/02_TO-BE_Sales%20Process%20Video%20Documentation.mp4)
5. [Chatbot-Documantation PPT (download)](https://github.com/DigiBP/Team-Apples/blob/8f019e16a5874df54c8768ca8b76a117889c4a79/CHATBOT-Files/ADOIT%20RGfW%20Chatbot%20documentation.pptx)
6. [Chatbot-Documantation Video (download)](https://github.com/DigiBP/Team-Apples/blob/8f019e16a5874df54c8768ca8b76a117889c4a79/CHATBOT-Files/ADOIT%20RGfW%20Chatbot%20demonstration%20video.mp4)
7. Final Presentation PPT: will be uploaded in Moodle and contains log-in details the google account used for the external services.
