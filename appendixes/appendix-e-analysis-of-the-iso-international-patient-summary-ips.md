# Appendix E: Analysis of the ISO International Patient Summary (IPS)

The IPS is designed to provide clinical information to assist care across any jurisdictional (e.g. local, regional, state/provincial, national) or organizational border by providing a minimal but not exhaustive data set useful for subsequent clinical care scenarios. It emphasizes the data required and the associated business rules to support use and the necessary conformance of the use case for an international patient summary. The ISO TC215 International Patient Summary includes a section on Allergies and Intolerances.

**The IPS includes the following conformance attributes:**

M| Mandatory| Shall always be present and - where applicable - shall be instantiated with valid values. No exceptions or empty/null values are allowed in this case.  
---|---|---  
R| Required| A required element shall always be present and - where applicable - should be instantiated with valid values. Exceptions or empty/null values are allowed in this case.  
RK| Required if Known| If there is information available, the element must be present and - where applicable - instantiated with valid values. If there is no information available, the element may be omitted, may be left empty, or may be instantiated with exceptional or null values depending on the implementation.  
C| Conditional| Depending on predicate conditions, the element may assume different conformance strengths (e.g. O, R, RK) or not being present.  
O| Optional| This data element can be omitted from a derived model, including from implementations. Recipient may ignore optional elements.  
  
**The Allergies and Intolerance section of IPS data set includes:**

**Data Element**| **Conformance**| **Datatype**| **Data Element Description**  
---|---|---|---  
Allergies/Intolerances content status| C| coded| As this IPS Section is mandatory for conformance, information about “known absence of allergies” or no information about allergies is required to be stated. Known Content will be accompanied by the conditional list of Allergies and intolerances.  
Allergies and Intolerances| C| List| If present then they shall be listed else give explicit reasons for why none are recorded. An ordered list comprising the name, code, a description of the Allergy/intolerance and Agent details for each Allergy/intolerance.  
1) Allergy/Intolerance| M| Label concept| If allergies present then they shall be listed else give explicit reasons for why none are recorded. An ordered list comprising the name, code, a description of the Allergy/intolerance and Agent details for each Allergy/intolerance.  
a. Allergy/Intolerance description| R| Text| Textual description of the allergy or intolerance.  
b. Clinical status| R| Coded| Provides the current status of the allergy or intolerance (e.g., active)  
c. Onset date| RK| Datetime| It shall be provided with the highest known precision, at least to the year  
d. End Date| C| Datetime| If Clinical Status is non-active then an exception can be raised to indicate inconsistency. It shall be provided with the highest known precision, at least to the year.  
e. Criticality| O| Coded| Represents the gravity of the potential risk for future life-threatening adverse reactions when exposed to a substance known to cause an adverse reaction in that individual.  
f. Certainty| O| Coded| Assertion about certainty associated with the propensity, or potential risk, of a reaction to the identified substance.  
g. Type of propensity| RK| Coded| Type of allergy or intolerance. (e.g., allergy)  
h. Diagnosis| O| Coded| A code indicating the type of reaction and the agent; an alternative option for describing an allergy to the agent. (e.g., lactose intolerant)  
i. Reaction| RK| Label Concept| A Label Concept recognizing that other data concerning the reaction may be made available in later versions of this standard.  
i) Manifestation of the reaction| RK| Coded| Description of the clinical manifestation of the allergic reaction. Example: anaphylactic shock  
ii) Severity| RK| Coded| Coded element that describes the subjective assessment of the severity of the condition as evaluated by the clinician, in the case of an allergy it is used as attribute of a manifestation of a reaction.  
j. Agent| R| Label Concept|   
iii) Agent code| R| Coded| A specific allergen or other agent/substance to which the patient has an adverse reaction propensity.  
iv) Category| O| Coded| Allergy substance category (eg food)  
  
Additional information about FHIR® implementation guide of the International Patient Summary can be found [here](http://hl7.org/fhir/uv/ips/): <http://hl7.org/fhir/uv/ips/> .

  

  

