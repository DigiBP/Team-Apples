# Team-Apples
Team Presentation - Apples 

This document describes the contribution to the process from the company Ximiq AG as part of the course "Digitalization of Business Processes" at the University of Applied Sciences and Arts North-western Switzerland. The team members are: Revathi Ravada, Cédric Hügli, Özlem Kösker, Juan Coutink, Hossein Zamanlou 


Description of the Use Case 

Ximiq was founded in 2013 as a Consulting Firm with the objective of working with customer as partners. The aim of Ximiq is to align Business and IT. This is done through Enterprise Architecture Management. While supporting one of our customers in EAM, we realized the need to automatically generate reports from the Enterprise Architecture Modelling Tools. At this point, Ximiq developed the ADOIT Report Generator for Microsoft Word. Thanks to the ADOIT Report Generator for Word customers are able to flexibly and quickly create architecture documentation in Microsoft Word by data sourced live from ADOIT. Customers can create their own template structure for their individual use cases or existing project management templates (e.g. Hermes) and create deliverables automatically. Instead of compiling their lists and data manually, customers can have it automatically inserted and updated from one single reliable source. 

The sales process for the Generator is currently at an Ad-hoc stage, meaning that roles and responsibilities are yet to be defined in order to increase pipeline and ultimately business. Throughout this process, we realized that Ximiq doesn’t have the resources for a dedicated Sales Team and the sales engagement is fully managed by consultants. That’s the reason why we need to implement a lean and streamlined process to better allocate resources.  

 
AS-IS Process Description 

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


Feel expression Decision task: Calculate Price

<?xml version="1.0" encoding="UTF-8"?>
<bpmn:definitions xmlns:bpmn="http://www.omg.org/spec/BPMN/20100524/MODEL" xmlns:bpmndi="http://www.omg.org/spec/BPMN/20100524/DI" xmlns:dc="http://www.omg.org/spec/DD/20100524/DC" xmlns:di="http://www.omg.org/spec/DD/20100524/DI" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:modeler="http://camunda.org/schema/modeler/1.0" id="Definitions_0yytvvn" targetNamespace="http://bpmn.io/schema/bpmn" exporter="Camunda Modeler" exporterVersion="5.8.0" modeler:executionPlatform="Camunda Platform" modeler:executionPlatformVersion="7.18.0">
  <bpmn:collaboration id="Collaboration_14bafqo">
    <bpmn:participant id="Participant_1o70z0d" name="License Process" processRef="Process_01km5mp" />
    <bpmn:participant id="Participant_1akwafx" name="Microsoft Appsource" processRef="Process_05c2jld" />
    <bpmn:participant id="Participant_14bift5" name="Microsoft Outlook" processRef="Process_0y67tgg" />
    <bpmn:participant id="Participant_0h18pg7" name="Client" processRef="Process_085xu8b" />
    <bpmn:messageFlow id="Flow_0aenrm8" sourceRef="Participant_0h18pg7" targetRef="Event_0t64v6w" />
    <bpmn:messageFlow id="Flow_0kd099w" sourceRef="Participant_0h18pg7" targetRef="Event_08spfzj" />
    <bpmn:messageFlow id="Flow_129eiqu" sourceRef="Activity_19dz912" targetRef="Activity_0aqn0su" />
    <bpmn:messageFlow id="Flow_07mot98" sourceRef="Activity_0pdvvjy" targetRef="Activity_1sqt7m5" />
    <bpmn:messageFlow id="Flow_1ue68w8" sourceRef="Activity_0ycqg0c" targetRef="Activity_0pdvvjy" />
    <bpmn:messageFlow id="Flow_0sgn3sy" sourceRef="Activity_1iju5aw" targetRef="Participant_0h18pg7" />
    <bpmn:messageFlow id="Flow_02yppsp" sourceRef="Activity_0vne28k" targetRef="Participant_0h18pg7" />
    <bpmn:messageFlow id="Flow_1yxkxsw" sourceRef="Activity_1vuq402" targetRef="Activity_12kpnou" />
    <bpmn:messageFlow id="Flow_0qq9pwj" sourceRef="Activity_0g98b7r" targetRef="Participant_0h18pg7" />
    <bpmn:messageFlow id="Flow_0uxov4k" sourceRef="Activity_1h36jq0" targetRef="Activity_0ycqg0c" />
  </bpmn:collaboration>
  <bpmn:process id="Process_01km5mp" isExecutable="true">
    <bpmn:laneSet id="LaneSet_1vp5uxt">
      <bpmn:lane id="Lane_0nedgw3" name="Consulting">
        <bpmn:flowNodeRef>Gateway_0evlgqi</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0dsqx6r</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_0t64v6w</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0aqn0su</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_08spfzj</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_0xoacfb</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1sqt7m5</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_0t2wtov</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1iju5aw</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_1gm1uoq</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_0xy74cy</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1ge1zci</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_1t28f2u</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1cbfv3v</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0zx29vx</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_0915jb8</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1h5tgly</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_1s6v917</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_1i0xo3h</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_0llrc4u</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_09qlzlp</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1h36jq0</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0g98b7r</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_19glvna</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1y7s4ye</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0y8qu7t</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0vwoi4d</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_1u4kxgc</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0vne28k</bpmn:flowNodeRef>
      </bpmn:lane>
      <bpmn:lane id="Lane_1qyd6cw" name="Accounting">
        <bpmn:flowNodeRef>Activity_12kpnou</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0bp5skr</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_04tzi25</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_06d63x6</bpmn:flowNodeRef>
      </bpmn:lane>
    </bpmn:laneSet>
    <bpmn:exclusiveGateway id="Gateway_0evlgqi">
      <bpmn:incoming>Flow_0h5l9t6</bpmn:incoming>
      <bpmn:incoming>Flow_0r5t0l7</bpmn:incoming>
      <bpmn:outgoing>Flow_1mmmxzc</bpmn:outgoing>
      <bpmn:outgoing>Flow_0e91igo</bpmn:outgoing>
      <bpmn:outgoing>Flow_1en2oz0</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:userTask id="Activity_0dsqx6r" name="Create new Lead in CRM">
      <bpmn:incoming>Flow_1uybkaw</bpmn:incoming>
      <bpmn:incoming>Flow_1bo1zve</bpmn:incoming>
      <bpmn:outgoing>Flow_1w2ybps</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:startEvent id="Event_0t64v6w" name="BOC-Marketplace Customer Request E-Mail">
      <bpmn:outgoing>Flow_1bo1zve</bpmn:outgoing>
      <bpmn:messageEventDefinition id="MessageEventDefinition_141dhnu" />
    </bpmn:startEvent>
    <bpmn:userTask id="Activity_0aqn0su" name="Checking New Leads">
      <bpmn:outgoing>Flow_0z3bk6x</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:startEvent id="Event_08spfzj" name="Other Reseller Requests">
      <bpmn:outgoing>Flow_1uybkaw</bpmn:outgoing>
      <bpmn:messageEventDefinition id="MessageEventDefinition_0i1g4ug" />
    </bpmn:startEvent>
    <bpmn:exclusiveGateway id="Gateway_0xoacfb">
      <bpmn:incoming>Flow_0fleqzu</bpmn:incoming>
      <bpmn:outgoing>Flow_0h5l9t6</bpmn:outgoing>
      <bpmn:outgoing>Flow_0vpynia</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:userTask id="Activity_1sqt7m5" name="Execute Live-Demo">
      <bpmn:incoming>Flow_0vpynia</bpmn:incoming>
      <bpmn:outgoing>Flow_0r5t0l7</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:intermediateCatchEvent id="Event_0t2wtov" name="Wait 14 days">
      <bpmn:incoming>Flow_1en2oz0</bpmn:incoming>
      <bpmn:outgoing>Flow_146puru</bpmn:outgoing>
      <bpmn:timerEventDefinition id="TimerEventDefinition_09lfio3" />
    </bpmn:intermediateCatchEvent>
    <bpmn:userTask id="Activity_1iju5aw" name="Send reminder">
      <bpmn:incoming>Flow_146puru</bpmn:incoming>
      <bpmn:outgoing>Flow_1lgjvd6</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:intermediateCatchEvent id="Event_1gm1uoq" name="Wait 14 days">
      <bpmn:incoming>Flow_1lgjvd6</bpmn:incoming>
      <bpmn:outgoing>Flow_1isio8m</bpmn:outgoing>
      <bpmn:timerEventDefinition id="TimerEventDefinition_0kot01m" />
    </bpmn:intermediateCatchEvent>
    <bpmn:exclusiveGateway id="Gateway_0xy74cy">
      <bpmn:incoming>Flow_1isio8m</bpmn:incoming>
      <bpmn:outgoing>Flow_1po20zq</bpmn:outgoing>
      <bpmn:outgoing>Flow_09kv48f</bpmn:outgoing>
      <bpmn:outgoing>Flow_0cwjwtj</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:userTask id="Activity_1ge1zci" name="Register Order in CRM">
      <bpmn:incoming>Flow_1mmmxzc</bpmn:incoming>
      <bpmn:incoming>Flow_0cwjwtj</bpmn:incoming>
      <bpmn:incoming>Flow_1umdjbn</bpmn:incoming>
      <bpmn:outgoing>Flow_0g25pln</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:intermediateThrowEvent id="Event_1t28f2u" name="inform accountant">
      <bpmn:incoming>Flow_1fajj0r</bpmn:incoming>
      <bpmn:outgoing>Flow_0ul13x4</bpmn:outgoing>
      <bpmn:messageEventDefinition id="MessageEventDefinition_1yj22fd" />
    </bpmn:intermediateThrowEvent>
    <bpmn:userTask id="Activity_1cbfv3v" name="Generate Trial-Licence Key">
      <bpmn:incoming>Flow_0e91igo</bpmn:incoming>
      <bpmn:incoming>Flow_09kv48f</bpmn:incoming>
      <bpmn:outgoing>Flow_19zgul2</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:userTask id="Activity_0zx29vx" name="Send Trial licence Key">
      <bpmn:incoming>Flow_19zgul2</bpmn:incoming>
      <bpmn:outgoing>Flow_17364zq</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:intermediateCatchEvent id="Event_0915jb8" name="Wait 30 days">
      <bpmn:incoming>Flow_17364zq</bpmn:incoming>
      <bpmn:outgoing>Flow_0qjtu1t</bpmn:outgoing>
      <bpmn:timerEventDefinition id="TimerEventDefinition_0bgq08c" />
    </bpmn:intermediateCatchEvent>
    <bpmn:userTask id="Activity_1h5tgly" name="Send Price Information">
      <bpmn:incoming>Flow_0qjtu1t</bpmn:incoming>
      <bpmn:outgoing>Flow_0d2097o</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:exclusiveGateway id="Gateway_1s6v917">
      <bpmn:incoming>Flow_0d2097o</bpmn:incoming>
      <bpmn:outgoing>Flow_0li9f6u</bpmn:outgoing>
      <bpmn:outgoing>Flow_1umdjbn</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:endEvent id="Event_1i0xo3h" name="Close Opportunity as lost">
      <bpmn:incoming>Flow_0li9f6u</bpmn:incoming>
      <bpmn:incoming>Flow_1po20zq</bpmn:incoming>
      <bpmn:incoming>Flow_1srag8u</bpmn:incoming>
    </bpmn:endEvent>
    <bpmn:intermediateCatchEvent id="Event_0llrc4u" name="Wait 30 days">
      <bpmn:incoming>Flow_1khvhiz</bpmn:incoming>
      <bpmn:outgoing>Flow_16baqd2</bpmn:outgoing>
      <bpmn:timerEventDefinition id="TimerEventDefinition_1fku8gy" />
    </bpmn:intermediateCatchEvent>
    <bpmn:sequenceFlow id="Flow_0h5l9t6" name="Customer doesn&#39;t request Live Demo" sourceRef="Gateway_0xoacfb" targetRef="Gateway_0evlgqi" />
    <bpmn:sequenceFlow id="Flow_0r5t0l7" sourceRef="Activity_1sqt7m5" targetRef="Gateway_0evlgqi" />
    <bpmn:sequenceFlow id="Flow_1mmmxzc" name="Customer orders Licence" sourceRef="Gateway_0evlgqi" targetRef="Activity_1ge1zci" />
    <bpmn:sequenceFlow id="Flow_0e91igo" name="Customer requests Trial-Licence" sourceRef="Gateway_0evlgqi" targetRef="Activity_1cbfv3v" />
    <bpmn:sequenceFlow id="Flow_1en2oz0" name="Customer doesn&#39;t answer" sourceRef="Gateway_0evlgqi" targetRef="Event_0t2wtov" />
    <bpmn:sequenceFlow id="Flow_1uybkaw" sourceRef="Event_08spfzj" targetRef="Activity_0dsqx6r" />
    <bpmn:sequenceFlow id="Flow_1bo1zve" sourceRef="Event_0t64v6w" targetRef="Activity_0dsqx6r" />
    <bpmn:sequenceFlow id="Flow_04fv9ar" name="forward invoice to consultant" sourceRef="Event_06d63x6" targetRef="Activity_0vne28k" />
    <bpmn:sequenceFlow id="Flow_1khvhiz" sourceRef="Activity_0vne28k" targetRef="Event_0llrc4u" />
    <bpmn:sequenceFlow id="Flow_0vpynia" name="Customer requested Live demo" sourceRef="Gateway_0xoacfb" targetRef="Activity_1sqt7m5" />
    <bpmn:sequenceFlow id="Flow_146puru" sourceRef="Event_0t2wtov" targetRef="Activity_1iju5aw" />
    <bpmn:sequenceFlow id="Flow_1lgjvd6" sourceRef="Activity_1iju5aw" targetRef="Event_1gm1uoq" />
    <bpmn:sequenceFlow id="Flow_1isio8m" sourceRef="Event_1gm1uoq" targetRef="Gateway_0xy74cy" />
    <bpmn:sequenceFlow id="Flow_1po20zq" name="Customer doesn&#39;t reply" sourceRef="Gateway_0xy74cy" targetRef="Event_1i0xo3h" />
    <bpmn:sequenceFlow id="Flow_09kv48f" name="Customer requests Trial-Licence" sourceRef="Gateway_0xy74cy" targetRef="Activity_1cbfv3v" />
    <bpmn:sequenceFlow id="Flow_0cwjwtj" name="Customer orders Licence" sourceRef="Gateway_0xy74cy" targetRef="Activity_1ge1zci" />
    <bpmn:sequenceFlow id="Flow_0g25pln" sourceRef="Activity_1ge1zci" targetRef="Activity_1y7s4ye" />
    <bpmn:sequenceFlow id="Flow_1fajj0r" sourceRef="Activity_1y7s4ye" targetRef="Event_1t28f2u" />
    <bpmn:sequenceFlow id="Flow_1umdjbn" name="Customer orders Licence" sourceRef="Gateway_1s6v917" targetRef="Activity_1ge1zci" />
    <bpmn:sequenceFlow id="Flow_0ul13x4" sourceRef="Event_1t28f2u" targetRef="Activity_04tzi25" />
    <bpmn:sequenceFlow id="Flow_0ddvhia" sourceRef="Activity_04tzi25" targetRef="Event_06d63x6" />
    <bpmn:sequenceFlow id="Flow_19zgul2" sourceRef="Activity_1cbfv3v" targetRef="Activity_0zx29vx" />
    <bpmn:sequenceFlow id="Flow_17364zq" sourceRef="Activity_0zx29vx" targetRef="Event_0915jb8" />
    <bpmn:sequenceFlow id="Flow_0qjtu1t" sourceRef="Event_0915jb8" targetRef="Activity_1h5tgly" />
    <bpmn:sequenceFlow id="Flow_0d2097o" sourceRef="Activity_1h5tgly" targetRef="Gateway_1s6v917" />
    <bpmn:sequenceFlow id="Flow_0li9f6u" name="Customer doesn&#39;t order" sourceRef="Gateway_1s6v917" targetRef="Event_1i0xo3h" />
    <bpmn:sequenceFlow id="Flow_1xbdigh" sourceRef="Activity_12kpnou" targetRef="Activity_0bp5skr" />
    <bpmn:sequenceFlow id="Flow_1uzcs6b" sourceRef="Activity_0bp5skr" targetRef="Activity_0y8qu7t" />
    <bpmn:sequenceFlow id="Flow_1nj9mbb" sourceRef="Activity_0y8qu7t" targetRef="Activity_0vwoi4d" />
    <bpmn:sequenceFlow id="Flow_1i705gw" sourceRef="Activity_0vwoi4d" targetRef="Event_1u4kxgc" />
    <bpmn:sequenceFlow id="Flow_014mwyn" name="No" sourceRef="Gateway_09qlzlp" targetRef="Activity_0g98b7r" />
    <bpmn:sequenceFlow id="Flow_16baqd2" sourceRef="Event_0llrc4u" targetRef="Gateway_09qlzlp" />
    <bpmn:exclusiveGateway id="Gateway_09qlzlp" name="Client payed?">
      <bpmn:incoming>Flow_16baqd2</bpmn:incoming>
      <bpmn:outgoing>Flow_014mwyn</bpmn:outgoing>
      <bpmn:outgoing>Flow_1ljodcx</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:sequenceFlow id="Flow_1ljodcx" name="Yes" sourceRef="Gateway_09qlzlp" targetRef="Activity_12kpnou" />
    <bpmn:sequenceFlow id="Flow_0fleqzu" sourceRef="Activity_1h36jq0" targetRef="Gateway_0xoacfb" />
    <bpmn:sequenceFlow id="Flow_0z3bk6x" sourceRef="Activity_0aqn0su" targetRef="Activity_1h36jq0" />
    <bpmn:sequenceFlow id="Flow_1w2ybps" sourceRef="Activity_0dsqx6r" targetRef="Activity_1h36jq0" />
    <bpmn:userTask id="Activity_1h36jq0" name="Send initial contact E-Mail">
      <bpmn:incoming>Flow_0z3bk6x</bpmn:incoming>
      <bpmn:incoming>Flow_1w2ybps</bpmn:incoming>
      <bpmn:outgoing>Flow_0fleqzu</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:sequenceFlow id="Flow_0qz5ni6" sourceRef="Activity_0g98b7r" targetRef="Event_19glvna" />
    <bpmn:userTask id="Activity_0g98b7r" name="Send Reminder">
      <bpmn:incoming>Flow_014mwyn</bpmn:incoming>
      <bpmn:outgoing>Flow_0qz5ni6</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:intermediateCatchEvent id="Event_19glvna" name="Wait 14 days">
      <bpmn:incoming>Flow_0qz5ni6</bpmn:incoming>
      <bpmn:outgoing>Flow_1srag8u</bpmn:outgoing>
      <bpmn:timerEventDefinition id="TimerEventDefinition_148xkm3" />
    </bpmn:intermediateCatchEvent>
    <bpmn:sequenceFlow id="Flow_1srag8u" sourceRef="Event_19glvna" targetRef="Event_1i0xo3h" />
    <bpmn:receiveTask id="Activity_12kpnou" name="Client payed">
      <bpmn:incoming>Flow_1ljodcx</bpmn:incoming>
      <bpmn:outgoing>Flow_1xbdigh</bpmn:outgoing>
    </bpmn:receiveTask>
    <bpmn:sendTask id="Activity_0bp5skr" name="Inform Consultant once client payed">
      <bpmn:incoming>Flow_1xbdigh</bpmn:incoming>
      <bpmn:outgoing>Flow_1uzcs6b</bpmn:outgoing>
    </bpmn:sendTask>
    <bpmn:manualTask id="Activity_1y7s4ye" name="Calculate Price">
      <bpmn:incoming>Flow_0g25pln</bpmn:incoming>
      <bpmn:outgoing>Flow_1fajj0r</bpmn:outgoing>
    </bpmn:manualTask>
    <bpmn:userTask id="Activity_04tzi25" name="Create Invoice">
      <bpmn:incoming>Flow_0ul13x4</bpmn:incoming>
      <bpmn:outgoing>Flow_0ddvhia</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:intermediateThrowEvent id="Event_06d63x6">
      <bpmn:incoming>Flow_0ddvhia</bpmn:incoming>
      <bpmn:outgoing>Flow_04fv9ar</bpmn:outgoing>
      <bpmn:messageEventDefinition id="MessageEventDefinition_077sg4v" />
    </bpmn:intermediateThrowEvent>
    <bpmn:userTask id="Activity_0y8qu7t" name="Generate Licence Key">
      <bpmn:incoming>Flow_1uzcs6b</bpmn:incoming>
      <bpmn:outgoing>Flow_1nj9mbb</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:userTask id="Activity_0vwoi4d" name="Send Licence Key">
      <bpmn:incoming>Flow_1nj9mbb</bpmn:incoming>
      <bpmn:outgoing>Flow_1i705gw</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:endEvent id="Event_1u4kxgc" name="Close Opportunity as won">
      <bpmn:incoming>Flow_1i705gw</bpmn:incoming>
    </bpmn:endEvent>
    <bpmn:userTask id="Activity_0vne28k" name="Send Invoice">
      <bpmn:incoming>Flow_04fv9ar</bpmn:incoming>
      <bpmn:outgoing>Flow_1khvhiz</bpmn:outgoing>
    </bpmn:userTask>
  </bpmn:process>
  <bpmn:process id="Process_05c2jld" isExecutable="false">
    <bpmn:serviceTask id="Activity_19dz912" name="Create new Lead in CRM (automated)">
      <bpmn:incoming>Flow_18bhntj</bpmn:incoming>
    </bpmn:serviceTask>
    <bpmn:sequenceFlow id="Flow_18bhntj" sourceRef="Event_0661j3a" targetRef="Activity_19dz912" />
    <bpmn:startEvent id="Event_0661j3a" name="Customer Downloaded the App">
      <bpmn:outgoing>Flow_18bhntj</bpmn:outgoing>
      <bpmn:conditionalEventDefinition id="ConditionalEventDefinition_1r4jhdl">
        <bpmn:condition xsi:type="bpmn:tFormalExpression" />
      </bpmn:conditionalEventDefinition>
    </bpmn:startEvent>
  </bpmn:process>
  <bpmn:process id="Process_0y67tgg" isExecutable="false">
    <bpmn:serviceTask id="Activity_0pdvvjy" name="Schedule Live-Demo" />
  </bpmn:process>
  <bpmn:process id="Process_085xu8b" isExecutable="false">
    <bpmn:userTask id="Activity_0ycqg0c" name="Fill in the form &#34;Book a live Demo&#34;" />
    <bpmn:sendTask id="Activity_1vuq402" name="Make payment" />
  </bpmn:process>
  <bpmndi:BPMNDiagram id="BPMNDiagram_1">
    <bpmndi:BPMNPlane id="BPMNPlane_1" bpmnElement="Collaboration_14bafqo">
      <bpmndi:BPMNShape id="Participant_1o70z0d_di" bpmnElement="Participant_1o70z0d" isHorizontal="true">
        <dc:Bounds x="160" y="380" width="2420" height="870" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Lane_1qyd6cw_di" bpmnElement="Lane_1qyd6cw" isHorizontal="true">
        <dc:Bounds x="190" y="380" width="2390" height="240" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Lane_0nedgw3_di" bpmnElement="Lane_0nedgw3" isHorizontal="true">
        <dc:Bounds x="190" y="620" width="2390" height="630" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_0evlgqi_di" bpmnElement="Gateway_0evlgqi" isMarkerVisible="true">
        <dc:Bounds x="975" y="1015" width="50" height="50" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_18o9a7g_di" bpmnElement="Activity_0dsqx6r">
        <dc:Bounds x="455" y="890" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_15b3uqk_di" bpmnElement="Event_0t64v6w">
        <dc:Bounds x="397" y="722" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="306" y="720" width="88" height="40" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1dt4n8y_di" bpmnElement="Activity_0aqn0su">
        <dc:Bounds x="455" y="1110" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_0dsqobc_di" bpmnElement="Event_08spfzj">
        <dc:Bounds x="487" y="722" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="533" y="726" width="73" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_0xoacfb_di" bpmnElement="Gateway_0xoacfb" isMarkerVisible="true">
        <dc:Bounds x="715" y="1015" width="50" height="50" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0t1ih8k_di" bpmnElement="Activity_1sqt7m5">
        <dc:Bounds x="880" y="820" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_1o9j0qz_di" bpmnElement="Event_0t2wtov">
        <dc:Bounds x="1042" y="1122" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1029" y="1165" width="63" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0kce4x8_di" bpmnElement="Activity_1iju5aw">
        <dc:Bounds x="1120" y="1100" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_1tsxcjp_di" bpmnElement="Event_1gm1uoq">
        <dc:Bounds x="1272" y="1122" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1259" y="1165" width="63" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_0xy74cy_di" bpmnElement="Gateway_0xy74cy" isMarkerVisible="true">
        <dc:Bounds x="1335" y="1115" width="50" height="50" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1o6b64c_di" bpmnElement="Activity_1ge1zci">
        <dc:Bounds x="1310" y="700" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_0xg0nmm_di" bpmnElement="Event_1t28f2u">
        <dc:Bounds x="1592" y="722" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1565" y="768" width="89" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_00fveq7_di" bpmnElement="Activity_1cbfv3v">
        <dc:Bounds x="1540" y="1000" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_05zcr64_di" bpmnElement="Activity_0zx29vx">
        <dc:Bounds x="1715" y="1000" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_11f43xq_di" bpmnElement="Event_0915jb8">
        <dc:Bounds x="1862" y="1022" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1849" y="1065" width="63" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1dlkalz_di" bpmnElement="Activity_1h5tgly">
        <dc:Bounds x="1985" y="1000" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_1s6v917_di" bpmnElement="Gateway_1s6v917" isMarkerVisible="true">
        <dc:Bounds x="2245" y="1015" width="50" height="50" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_1i0xo3h_di" bpmnElement="Event_1i0xo3h">
        <dc:Bounds x="2382" y="1022" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="2425" y="1028" width="89" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_0x2ycpc_di" bpmnElement="Event_0llrc4u">
        <dc:Bounds x="1872" y="722" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1858" y="768" width="63" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_0j60224_di" bpmnElement="Gateway_09qlzlp" isMarkerVisible="true">
        <dc:Bounds x="1939" y="715" width="50" height="50" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1996" y="733" width="68" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1st7uko_di" bpmnElement="Activity_1h36jq0">
        <dc:Bounds x="580" y="1000" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1332dts_di" bpmnElement="Activity_0g98b7r">
        <dc:Bounds x="2010" y="850" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="BPMNShape_0quakyh" bpmnElement="Event_19glvna">
        <dc:Bounds x="2172" y="872" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="2158" y="848" width="63" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1t8ys37_di" bpmnElement="Activity_12kpnou">
        <dc:Bounds x="1914" y="490" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0l4xdni_di" bpmnElement="Activity_0bp5skr">
        <dc:Bounds x="2130" y="490" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_079e3xi_di" bpmnElement="Activity_1y7s4ye">
        <dc:Bounds x="1450" y="700" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_13uxmgd_di" bpmnElement="Activity_04tzi25">
        <dc:Bounds x="1550" y="490" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_0x18s6x_di" bpmnElement="Event_06d63x6">
        <dc:Bounds x="1722" y="512" width="36" height="36" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1of4ek0_di" bpmnElement="Activity_0y8qu7t">
        <dc:Bounds x="2130" y="700" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1kat26g_di" bpmnElement="Activity_0vwoi4d">
        <dc:Bounds x="2300" y="700" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_1u4kxgc_di" bpmnElement="Event_1u4kxgc">
        <dc:Bounds x="2442" y="722" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="2485" y="726" width="89" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1eahyyn_di" bpmnElement="Activity_0vne28k">
        <dc:Bounds x="1690" y="700" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_0h5l9t6_di" bpmnElement="Flow_0h5l9t6">
        <di:waypoint x="765" y="1040" />
        <di:waypoint x="975" y="1040" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="770" y="1043" width="87" height="40" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0r5t0l7_di" bpmnElement="Flow_0r5t0l7">
        <di:waypoint x="930" y="900" />
        <di:waypoint x="930" y="1040" />
        <di:waypoint x="975" y="1040" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1mmmxzc_di" bpmnElement="Flow_1mmmxzc">
        <di:waypoint x="1000" y="1015" />
        <di:waypoint x="1000" y="740" />
        <di:waypoint x="1310" y="740" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1032" y="706" width="83" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0e91igo_di" bpmnElement="Flow_0e91igo">
        <di:waypoint x="1025" y="1040" />
        <di:waypoint x="1540" y="1040" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1029" y="993" width="71" height="40" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1en2oz0_di" bpmnElement="Flow_1en2oz0">
        <di:waypoint x="1000" y="1065" />
        <di:waypoint x="1000" y="1140" />
        <di:waypoint x="1042" y="1140" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1006" y="1078" width="87" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1uybkaw_di" bpmnElement="Flow_1uybkaw">
        <di:waypoint x="505" y="758" />
        <di:waypoint x="505" y="890" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1bo1zve_di" bpmnElement="Flow_1bo1zve">
        <di:waypoint x="415" y="758" />
        <di:waypoint x="415" y="930" />
        <di:waypoint x="455" y="930" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_04fv9ar_di" bpmnElement="Flow_04fv9ar">
        <di:waypoint x="1740" y="548" />
        <di:waypoint x="1740" y="700" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1647" y="566" width="86" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1khvhiz_di" bpmnElement="Flow_1khvhiz">
        <di:waypoint x="1790" y="740" />
        <di:waypoint x="1872" y="740" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0vpynia_di" bpmnElement="Flow_0vpynia">
        <di:waypoint x="740" y="1015" />
        <di:waypoint x="740" y="860" />
        <di:waypoint x="880" y="860" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="743" y="930" width="73" height="40" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_146puru_di" bpmnElement="Flow_146puru">
        <di:waypoint x="1078" y="1140" />
        <di:waypoint x="1120" y="1140" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1lgjvd6_di" bpmnElement="Flow_1lgjvd6">
        <di:waypoint x="1220" y="1140" />
        <di:waypoint x="1272" y="1140" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1isio8m_di" bpmnElement="Flow_1isio8m">
        <di:waypoint x="1308" y="1140" />
        <di:waypoint x="1335" y="1140" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1po20zq_di" bpmnElement="Flow_1po20zq">
        <di:waypoint x="1360" y="1165" />
        <di:waypoint x="1360" y="1230" />
        <di:waypoint x="2400" y="1230" />
        <di:waypoint x="2400" y="1058" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1376" y="1197" width="87" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_09kv48f_di" bpmnElement="Flow_09kv48f">
        <di:waypoint x="1385" y="1140" />
        <di:waypoint x="1590" y="1140" />
        <di:waypoint x="1590" y="1080" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1384" y="1140" width="71" height="40" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0cwjwtj_di" bpmnElement="Flow_0cwjwtj">
        <di:waypoint x="1360" y="1115" />
        <di:waypoint x="1360" y="780" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1368" y="1078" width="83" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0g25pln_di" bpmnElement="Flow_0g25pln">
        <di:waypoint x="1410" y="740" />
        <di:waypoint x="1450" y="740" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1fajj0r_di" bpmnElement="Flow_1fajj0r">
        <di:waypoint x="1550" y="740" />
        <di:waypoint x="1592" y="740" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1umdjbn_di" bpmnElement="Flow_1umdjbn">
        <di:waypoint x="2270" y="1015" />
        <di:waypoint x="2270" y="980" />
        <di:waypoint x="1380" y="980" />
        <di:waypoint x="1380" y="780" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="2182" y="996" width="83" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0ul13x4_di" bpmnElement="Flow_0ul13x4">
        <di:waypoint x="1610" y="722" />
        <di:waypoint x="1610" y="570" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0ddvhia_di" bpmnElement="Flow_0ddvhia">
        <di:waypoint x="1650" y="530" />
        <di:waypoint x="1722" y="530" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_19zgul2_di" bpmnElement="Flow_19zgul2">
        <di:waypoint x="1640" y="1040" />
        <di:waypoint x="1715" y="1040" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_17364zq_di" bpmnElement="Flow_17364zq">
        <di:waypoint x="1815" y="1040" />
        <di:waypoint x="1862" y="1040" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0qjtu1t_di" bpmnElement="Flow_0qjtu1t">
        <di:waypoint x="1898" y="1040" />
        <di:waypoint x="1985" y="1040" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0d2097o_di" bpmnElement="Flow_0d2097o">
        <di:waypoint x="2085" y="1040" />
        <di:waypoint x="2245" y="1040" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0li9f6u_di" bpmnElement="Flow_0li9f6u">
        <di:waypoint x="2295" y="1040" />
        <di:waypoint x="2382" y="1040" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="2274" y="1058" width="87" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1xbdigh_di" bpmnElement="Flow_1xbdigh">
        <di:waypoint x="2014" y="530" />
        <di:waypoint x="2130" y="530" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1uzcs6b_di" bpmnElement="Flow_1uzcs6b">
        <di:waypoint x="2180" y="570" />
        <di:waypoint x="2180" y="700" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1nj9mbb_di" bpmnElement="Flow_1nj9mbb">
        <di:waypoint x="2230" y="740" />
        <di:waypoint x="2300" y="740" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1i705gw_di" bpmnElement="Flow_1i705gw">
        <di:waypoint x="2400" y="740" />
        <di:waypoint x="2442" y="740" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_014mwyn_di" bpmnElement="Flow_014mwyn">
        <di:waypoint x="1964" y="765" />
        <di:waypoint x="1964" y="890" />
        <di:waypoint x="2010" y="890" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1972" y="826" width="15" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_16baqd2_di" bpmnElement="Flow_16baqd2">
        <di:waypoint x="1908" y="740" />
        <di:waypoint x="1939" y="740" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1ljodcx_di" bpmnElement="Flow_1ljodcx">
        <di:waypoint x="1964" y="715" />
        <di:waypoint x="1964" y="570" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1971" y="640" width="18" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0fleqzu_di" bpmnElement="Flow_0fleqzu">
        <di:waypoint x="680" y="1040" />
        <di:waypoint x="715" y="1040" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0z3bk6x_di" bpmnElement="Flow_0z3bk6x">
        <di:waypoint x="555" y="1150" />
        <di:waypoint x="630" y="1150" />
        <di:waypoint x="630" y="1080" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1w2ybps_di" bpmnElement="Flow_1w2ybps">
        <di:waypoint x="555" y="930" />
        <di:waypoint x="630" y="930" />
        <di:waypoint x="630" y="1000" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0qz5ni6_di" bpmnElement="Flow_0qz5ni6">
        <di:waypoint x="2110" y="890" />
        <di:waypoint x="2172" y="890" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1srag8u_di" bpmnElement="Flow_1srag8u">
        <di:waypoint x="2208" y="890" />
        <di:waypoint x="2400" y="890" />
        <di:waypoint x="2400" y="1022" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="Participant_1bbniwu_di" bpmnElement="Participant_1akwafx" isHorizontal="true">
        <dc:Bounds x="160" y="1280" width="470" height="150" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0f0dpx8_di" bpmnElement="Activity_19dz912">
        <dc:Bounds x="450" y="1300" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_0ajnb0i_di" bpmnElement="Event_0661j3a">
        <dc:Bounds x="242" y="1322" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="221" y="1365" width="80" height="40" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_18bhntj_di" bpmnElement="Flow_18bhntj">
        <di:waypoint x="278" y="1340" />
        <di:waypoint x="450" y="1340" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="BPMNShape_1b1hquw" bpmnElement="Participant_14bift5" isHorizontal="true">
        <dc:Bounds x="160" y="80" width="820" height="140" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0v620br_di" bpmnElement="Activity_0pdvvjy">
        <dc:Bounds x="580" y="100" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Participant_0hl6ayn_di" bpmnElement="Participant_0h18pg7" isHorizontal="true">
        <dc:Bounds x="160" y="230" width="2420" height="130" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0pln0b8_di" bpmnElement="Activity_0ycqg0c">
        <dc:Bounds x="580" y="250" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_19tflxt_di" bpmnElement="Activity_1vuq402">
        <dc:Bounds x="1914" y="260" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_0aenrm8_di" bpmnElement="Flow_0aenrm8">
        <di:waypoint x="415" y="360" />
        <di:waypoint x="415" y="722" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0kd099w_di" bpmnElement="Flow_0kd099w">
        <di:waypoint x="505" y="360" />
        <di:waypoint x="505" y="722" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_129eiqu_di" bpmnElement="Flow_129eiqu">
        <di:waypoint x="500" y="1300" />
        <di:waypoint x="500" y="1190" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_07mot98_di" bpmnElement="Flow_07mot98">
        <di:waypoint x="680" y="140" />
        <di:waypoint x="930" y="140" />
        <di:waypoint x="930" y="820" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1ue68w8_di" bpmnElement="Flow_1ue68w8">
        <di:waypoint x="630" y="250" />
        <di:waypoint x="630" y="180" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0sgn3sy_di" bpmnElement="Flow_0sgn3sy">
        <di:waypoint x="1170" y="1100" />
        <di:waypoint x="1170" y="360" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_02yppsp_di" bpmnElement="Flow_02yppsp">
        <di:waypoint x="1765" y="700" />
        <di:waypoint x="1765" y="360" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1yxkxsw_di" bpmnElement="Flow_1yxkxsw">
        <di:waypoint x="1964" y="340" />
        <di:waypoint x="1964" y="490" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0qq9pwj_di" bpmnElement="Flow_0qq9pwj">
        <di:waypoint x="2060" y="850" />
        <di:waypoint x="2060" y="360" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0uxov4k_di" bpmnElement="Flow_0uxov4k">
        <di:waypoint x="650" y="1000" />
        <di:waypoint x="650" y="330" />
      </bpmndi:BPMNEdge>
    </bpmndi:BPMNPlane>
  </bpmndi:BPMNDiagram>
</bpmn:definitions>
