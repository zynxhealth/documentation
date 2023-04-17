## Functionality by Content Type \ Content Item Type
<br>
### ZynxCare
Includes ZynxCare Extended, ZynxCare for Home Health, and ZynxCare for Rehabilitation <br>
<br>
| FHIR Display Value \ [Description]   | Code Value    |   Functionality|   Example|
| :---------------- | :-----------: | :---------- | :---------- |
|Problem|8|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Problem|8|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Problem|8|Snomed Code Mapping|``` <coding> <system value="http://snomed.info/sct"></system> <code value="370388006"> </code> </coding> ```|
|Problem|8|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Outcome|10|Functional Goal| ``` <documentation> <type value="documentation"/> <display value="(CMS LTCH CARE, CMS IRF PAI)"/> </documentation> ```|
|Outcome|10|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Outcome|10|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Reminder|4|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Reminder|4|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Reminder|4|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Reminder \ [Patient Engagement]|12|Discipline(s)| ``` <participant><type value="practitioner"/><role><coding><system value="http://www.zynxhealth.com/fhir/StructureDefinition/discipline/code"/>         <code value="CMSW"/></coding><text value="Case Manager/Social Worker"/></role></participant> ``` |
|Reminder \ [Patient Engagement]|12|Education Flag|```  <code> <coding> <system value="http://snomed.info/sct"></system> <code value="409073007"></code> </coding> <text value="Education (procedure)"> </text> </code>  ```|
|Activity|12|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Activity|12|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Activity|12|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Activitylet \ [Activity Detail]|15|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Activitylet \ [Activity Detail]|15|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
<br>
### ZynxCare for Chronic Conditions Management
<br>
|Problem|8|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Problem|8|Snomed Code Mapping|``` <coding> <system value="http://snomed.info/sct"></system> <code value="370388006"> </code> </coding> ```|
|Problem|8|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Outcome|10|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Outcome|10|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Patient Engagement|4|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Patient Engagement|4|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Activity|12|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Activity|12|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Frequency|16|Frequency| ``` <extension url="http://www.zynxhealth.com/fhir/StructureDefinition/frequency"> <valueCodeableConcept> <coding> <system value="http://www.zynxhealth.com/fhir/StructureDefinition/frequency/code"> </system><code value="PRN"> </code></coding><text value="PRN - as needed"> </text></valueCodeableConcept> </extension> ``` |
|Activitylet \ [Activity Detail]|15|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Activitylet \ [Activity Detail]|15|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
<br>
### ZynxOrder
<br>
| FHIR Display Value \ [Description]  | Code Value    |   Functionality|   Example|
| :---------------- | :-----------: | :---------- | :---------- |
|Section|2|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Section|2|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Section|2|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Reminder|4|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Reminder|4|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Reminder|4|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Orderable (Med)|3|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Orderable|5|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
<br>
### Custom Order Sets
<br>
| FHIR Display Value \ [Description]  | Code Value    |   Functionality|   Example|
| :---------------- | :-----------: | :---------- | :---------- |
|Section|2|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation> ```|
|Section|2|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Section|2|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Section|2|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Reminder|4|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Reminder|4|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Reminder|4|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Orderable (Med)|3|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation> ```|
|Orderable (Med)|3|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Orderable|5|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation> ```|
|Orderable|5|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
<br>
### Custom Plans of Care
<br>
| FHIR Display Value \ [Description]  | Code Value    |   Functionality|   Example|
| :---------------- | :-----------: | :---------- | :---------- |
|Problem|8|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation> ```|
|Problem|8|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Problem|8|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Problem|8|Snomed Code Mapping|``` <coding> <system value="http://snomed.info/sct"></system> <code value="370388006"> </code> </coding> ```|
|Problem|8|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Outcome|10|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation>  ```|
|Outcome|10|Functional Goal| ``` <documentation> <type value="documentation"/> <display value="(CMS LTCH CARE, CMS IRF PAI)"/> </documentation> ```|
|Outcome|10|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Outcome|10|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Reminder|12|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation>  ```|
|Reminder|4|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Reminder|4|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Reminder|4|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Reminder|12|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation>  ```|
|Reminder \ [Patient Engagement]|12|Discipline(s)| ``` <participant><type value="practitioner"/><role><coding><system value="http://www.zynxhealth.com/fhir/StructureDefinition/discipline/code"/>         <code value="CMSW"/></coding><text value="Case Manager/Social Worker"/></role></participant> ``` |
|Reminder \ [Patient Engagement]|12|Education Flag|```  <code> <coding> <system value="http://snomed.info/sct"></system> <code value="409073007"></code> </coding> <text value="Education (procedure)"> </text> </code>  ```|
|Activitylet \ [Activity Detail]|15|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation>  ```|
|Activity|12|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Activity|12|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Activity|12|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
|Activitylet \ [Activity Detail]|15|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation>  ```|
|Activitylet \ [Activity Detail]|15|Semantic ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/semantic-id"/> <code value=""/> ```|
|Activitylet \ [Activity Detail]|15|Unique ID | ``` <code> <coding> <system value="http://www.zynxhealth.com/codings/unique-id"/> <code value=""/> ```|
<br>
