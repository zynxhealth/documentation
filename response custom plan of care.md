Response Custom Plan of Care

<PlanDefinition xmlns="http://hl7.org/fhir">
   <id value="49d3a680-7258-46f3-820a-34b0e966e8fd"/>
   <meta>
      <versionId value="1"/>
      <lastUpdated value="2021-04-08T20:25:13.000+00:00"/>
   </meta>
   <identifier>
      <use value="official"/>
      <system value="http://www.zynxhealth.com/codings/id/custom/contentid"/>
      <value value="S:5591:C:POC-1001002"/>
   </identifier>
   <version value="2.1.0"/>
   <name value="patient problems - pain (starter plan of care)"/>
   <title value="Patient Problems - Pain (Starter Plan of Care)"/>
   <type>
      <coding>
         <code value="protocol"/>
      </coding>
   </type>
   <status value="active"/>
   <date value="2021-04-08T20:25:13.217"/>
   <publisher value="Zynx Health"/>
   <useContext>
      <code>
         <system value="http://hl7.org/fhir/usage-context-type"/>
         <code value="focus"/>
      </code>
      <valueCodeableConcept>
         <coding>
            <system value="http://www.zynxhealth.com/codings/focuses"/>
            <code value="44ca44c3-aedb-4019-b95c-b259ab3cead2"/>
            <display value="Patient Problems"/>
         </coding>
      </valueCodeableConcept>
   </useContext>
   <useContext>
      <code>
         <system value="http://hl7.org/fhir/usage-context-type"/>
         <code value="venue"/>
      </code>
      <valueCodeableConcept>
         <coding>
            <system value="http://www.zynxhealth.com/codings/venues"/>
            <code value="5af1f0c0-bda1-47b5-9f38-5cb0a7120423"/>
            <display value="Hospital"/>
         </coding>
      </valueCodeableConcept>
   </useContext>
   <contact>
      <telecom>
         <system value="url"/>
         <value value="http://www.zynxhealth.com"/>
      </telecom>
      <telecom>
         <system value="email"/>
         <value value="support@zynx.com"/>
      </telecom>
   </contact>
   <copyright value="© 2017-2021 Zynx Health Corporation. All rights reserved."/>
   <goal>
      <description>
         <text value="Reduced pain sensation"/>
      </description>
      <addresses>
         <coding>
            <system value="http://www.zynxhealth.com/codings/problems"/>
            <code value="85385"/>
         </coding>
      </addresses>
      <documentation>
         <type value="justification"/>
         <display value="Patient Problems>Pain>Evaluation/Outcome>Performance Measures"/>
         <url value="https://www.zynx.com/Reference/Content.aspx?ItemID=228682"/>
      </documentation>
      <documentation>
         <extension url="http://www.zynxhealth.com/codings/quality-measures">
            <valueInteger value="59"/>
         </extension>
         <type value="citation"/>
         <display value="The Joint Commission Pain Management Standard"/>
      </documentation>
      <documentation>
         <extension url="http://www.zynxhealth.com/codings/quality-measures">
            <valueInteger value="114"/>
         </extension>
         <type value="citation"/>
         <display value="CMS Promoting Interoperability Program Measure for Eligible Hospitals and Critical Access Hospitals"/>
      </documentation>
   </goal>
   <action>
      <title value="Pain"/>
      <textEquivalent value="Pain"/>
      <code>
         <coding>
            <system value="http://www.zynxhealth.com/codings/item-types"/>
            <code value="8"/>
         </coding>
         <text value="Problem"/>
      </code>
      <code>
         <coding>
            <system value="http://www.zynxhealth.com/codings/problems"/>
            <code value="85385"/>
         </coding>
         <text value="Pain"/>
      </code>
      <groupingBehavior value="logical-group"/>
      <requiredBehavior value="could"/>
      <action>
         <title value="Interventions"/>
         <textEquivalent value="Interventions"/>
         <code>
            <coding>
               <system value="http://www.zynxhealth.com/codings/item-types"/>
               <code value="2"/>
            </coding>
            <text value="Section"/>
         </code>
         <groupingBehavior value="logical-group"/>
         <action>
            <title value="Assessments"/>
            <textEquivalent value="Assessments"/>
            <code>
               <coding>
                  <system value="http://www.zynxhealth.com/codings/item-types"/>
                  <code value="2"/>
               </coding>
               <text value="Section"/>
            </code>
            <groupingBehavior value="logical-group"/>
            <action>
               <textEquivalent value="Functional status assessment – physical"/>
               <code>
                  <coding>
                     <system value="http://www.zynxhealth.com/codings/item-types"/>
                     <code value="12"/>
                  </coding>
                  <text value="Activity"/>
               </code>
               <documentation>
                  <type value="justification"/>
                  <display value="Patient Problems>Pain>Assessment/Diagnosis>Assessment Components"/>
                  <url value="https://www.zynx.com/Reference/Content.aspx?ItemID=192403"/>
               </documentation>
               <selectionBehavior value="all-or-none"/>
               <requiredBehavior value="could"/>
               <action>
                  <textEquivalent value="Mobility status"/>
                  <code>
                     <coding>
                        <system value="http://www.zynxhealth.com/codings/item-types"/>
                        <code value="15"/>
                     </coding>
                     <text value="Activitylet"/>
                  </code>
                  <requiredBehavior value="could"/>
               </action>
            </action>
            <action>
               <title value="For patients with a history of substance abuse, routinely perform a comprehensive pain assessment, perform physical and psychological assessments and current drug use screening"/>
               <code>
                  <coding>
                     <system value="http://www.zynxhealth.com/codings/item-types"/>
                     <code value="4"/>
                  </coding>
                  <text value="Reminder"/>
               </code>
               <documentation>
                  <type value="justification"/>
                  <display value="Patient Problems>Pain>Assessment/Diagnosis>Assessment>Substance Abuse"/>
                  <url value="https://www.zynx.com/Reference/Content.aspx?ItemID=180147"/>
               </documentation>
               <documentation>
                  <extension url="http://www.zynxhealth.com/codings/quality-measures">
                     <valueInteger value="59"/>
                  </extension>
                  <type value="citation"/>
                  <display value="The Joint Commission Pain Management Standard"/>
               </documentation>
            </action>
         </action>
         <action>
            <title value="Education"/>
            <textEquivalent value="Education"/>
            <code>
               <coding>
                  <system value="http://www.zynxhealth.com/codings/item-types"/>
                  <code value="2"/>
               </coding>
               <text value="Section"/>
            </code>
            <groupingBehavior value="logical-group"/>
            <action>
               <textEquivalent value="Education, herbal medicine supplementation"/>
               <code>
                  <coding>
                     <system value="http://www.zynxhealth.com/codings/item-types"/>
                     <code value="12"/>
                  </coding>
                  <text value="Activity"/>
               </code>
               <code>
                  <coding>
                     <system value="http://snomed.info/sct"/>
                     <code value="409073007"/>
                  </coding>
                  <text value="Education (procedure)"/>
               </code>
               <documentation>
                  <type value="justification"/>
                  <display value="Patient Problems>Pain>Planning/Implementation>Medications>Herbal Drugs"/>
                  <url value="https://www.zynx.com/Reference/Content.aspx?ItemID=220991"/>
               </documentation>
               <selectionBehavior value="all-or-none"/>
               <requiredBehavior value="could"/>
               <action>
                  <textEquivalent value="Aromatherapy"/>
                  <code>
                     <coding>
                        <system value="http://www.zynxhealth.com/codings/item-types"/>
                        <code value="15"/>
                     </coding>
                     <text value="Activitylet"/>
                  </code>
                  <requiredBehavior value="could"/>
               </action>
               <action>
                  <textEquivalent value="Oral herbal supplements"/>
                  <code>
                     <coding>
                        <system value="http://www.zynxhealth.com/codings/item-types"/>
                        <code value="15"/>
                     </coding>
                     <text value="Activitylet"/>
                  </code>
                  <requiredBehavior value="could"/>
               </action>
            </action>
            <action>
               <textEquivalent value="Education, pain communication"/>
               <code>
                  <coding>
                     <system value="http://www.zynxhealth.com/codings/item-types"/>
                     <code value="12"/>
                  </coding>
                  <text value="Activity"/>
               </code>
               <code>
                  <coding>
                     <system value="http://snomed.info/sct"/>
                     <code value="409073007"/>
                  </coding>
                  <text value="Education (procedure)"/>
               </code>
               <documentation>
                  <type value="justification"/>
                  <display value="Patient Problems>Pain>Planning/Implementation>Education>Pain Communication"/>
                  <url value="https://www.zynx.com/Reference/Content.aspx?ItemID=212692"/>
               </documentation>
               <documentation>
                  <extension url="http://www.zynxhealth.com/codings/quality-measures">
                     <valueInteger value="59"/>
                  </extension>
                  <type value="citation"/>
                  <display value="The Joint Commission Pain Management Standard"/>
               </documentation>
               <selectionBehavior value="all-or-none"/>
               <requiredBehavior value="could"/>
            </action>
         </action>
      </action>
   </action>
</PlanDefinition>
