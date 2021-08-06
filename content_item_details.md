## Functionality by Content Item Type

| Text or Display Value   | Code Value    |   Functionality|   Example|
| :---------------- | :-----------: | :---------- | :---------- |
|Section|2|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Section|2|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation> ```|
|Section|2|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Orderable (Med)|3|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Reminder|4|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Orderable|5|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Problem|8|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation> ```|
|Problem|8|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Problem|8|Snomed Code Mapping|``` <coding> <system value="http://snomed.info/sct"></system> <code value="370388006"> </code> </coding> ```|
|Problem|8|Unique Id| ``` <coding> <system value="http://www.zynxhealth.com/codings/problems"> </system><code value="941562.91778"> </code> </coding> ```|
|Outcome|10|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation>  ```|
|Outcome|10|Functional Goal| ``` <documentation> <type value="documentation"/> <display value="(CMS LTCH CARE, CMS IRF PAI)"/> </documentation> ```|
|Activity|12|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation>  ```|
|Activity|12|Discipline| ``` <participant><type value="practitioner"/><role><coding><system value="http://www.zynxhealth.com/fhir/StructureDefinition/discipline/code"/>         <code value="CMSW"/></coding><text value="Case Manager/Social Worker"/></role></participant> ``` |
|Activity|12|Education Flag|```  <code> <coding> <system value="http://snomed.info/sct"></system> <code value="409073007"></code> </coding> <text value="Education (procedure)"> </text> </code>  ```|
|Activity|12|Frequency| ``` <extension url="http://www.zynxhealth.com/fhir/StructureDefinition/frequency"> <valueCodeableConcept> <coding> <system value="http://www.zynxhealth.com/fhir/StructureDefinition/frequency/code"> </system><code value="PRN"> </code></coding><text value="PRN - as needed"> </text></valueCodeableConcept> </extension> ``` |
|Activity|12|Gold Key\Key Clinical Process| ``` <reason> <coding> <system value="http://www.zynxhealth.com/codings/key-clinical-processes"/> ```|
|Activitylet|15|Additional Info| ``` <documentation> <type value="documentation"></type> <display value="additional info text"> </display> </documentation>  ```|
