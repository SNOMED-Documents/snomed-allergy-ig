# Appendix D: Analysis of the HL7 Patient Care Domain Analysis Model

This domain analysis model for allergy records was developed by the HL7 Patient Care Work Group and has been used to inform the allergy/intolerance modeling in the C-CDA® and FHIR® specifications.

<http://www.hl7.org/implement/standards/product_brief.cfm?product_id=308>

Figure 7: Patient Care Domain Analysis Model

**

<figure><img src="images/180920429.png" alt="" title=""><figcaption><p>**</p></figcaption></figure>

**Selected attribute definitions**

**Attribute name**| **Datatype**| **Definition**  
---|---|---  
**Adverse reaction**  
severity| Coded| Assessment of the severity of the reaction  
didNotOccurFlag| Boolean| Indicates a reaction did not occur at contact with substance  
OccurrenceDate| DateTime| Time stamp for manifestation of the reaction  
**Health condition**  
status| Coded| Current status of the concern  
**Adverse sensitivity to substance**  
criticality| Coded| Clinical judgement regarding potential seriousness of a future reaction.  
sensitivityType| Coded| Allergy; intolerance  
createdDate| Date Time| Date time the entry was created  
**Substance**  
identifier| Coded| Coded reference to the substance involved in the reaction  
name| String| Name of the substance  
**Exposure**  
exposureDate| Date Time| Date time when the exposure occurred; may be approximated  
exposureType| Coded| How the exposure occurred, eg vaccination, prescription, administration, accidental  
**Manifestation**  
severity| Coded| Severity of the manifestation of the reaction  
reactionType| Coded| Clinical finding characterizing the reaction, eg code for rash or hives  
**Sensitivity test**  
identifier| Identifier| Identifier pointing to results of the sensitivity test  
name| String| Name of the test
