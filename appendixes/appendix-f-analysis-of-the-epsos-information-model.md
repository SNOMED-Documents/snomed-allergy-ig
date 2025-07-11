# Appendix F: Analysis of the epSOS information model

Several models were discussed for representing the Allergy information. Especially because there was set a requirement that the information should express the difference between an allergy and intolerance, which have clinically very different meanings. Should be build a model on our own or did a standard models exist which matched our use case? The Semantic team was considering adoption the HL7® CDA/CCD model for allergies where "adverse event type" is used with a terminology such as SNOMED high-level classification, so that the distinction between allergies versus intolerances can be managed. The whole model was not adopted, but a simplified version of it due the fact it contained too many dimensions, which were out of scope for the PS use case.

The distinction between reactions to substances/food versus drugs was also a request and thereby explicit handled, with appropriate value sets.

SNOMED CT was selected for three attributes in the proposed Allergy model:

**Reaction Allergy:**

The Value Set was selected to code the clinical manifestations of allergy developed by patient in the "Allergies and Other Adverse Reactions" section of the patient Summary (along with epSOSActiveIngredient). This value set was inherited as defined in CDA/CCD Allergy Model, since the choice of the Allergy model was taken.

**AdverseEventType:**

The value set was selected to cods the patient's kind of adverse reactions against substance, food or drugs. This value set was inherited as defined in CDA/CCD Allergy Model, since the choice of the Allergy model was taken.

**Allergen No drugs:**

The Value Set was created to code the allergenic agents (apart from drugs) against which the patient has developed an adverse reaction due to the fact that this type of information was not part of the CDA/CCD Allergy Model. The value set was created in a 5-step workflow (created, review by clinician, reviewed by semantic team, revised by clinician, reviewed and approved by Semantic Team). Relevant sub-hierarchies in SNOMED CT were selected and some single terms. The value set was validated by the Semantic Team for acceptance as a minimum value set/data set.

<table data-header-hidden><thead><tr><th width="159.5078125"></th><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td>Data<br>element<br>level 1<br>(cardinality)</td><td>Data element level 3<br>(cardinality)</td><td>COMMENTS</td><td>BASIC (Basic)<br>/ EXTENDED<br>(Ext)<br>DATASET</td><td>Null flavour Yes/No</td></tr><tr><td>Allergy</td><td>Allergy Display name</td><td><br></td><td>Basic</td><td>Yes</td></tr><tr><td>Allergy</td><td>Allergy code</td><td>The code of the allergy</td><td>Basic</td><td>Yes</td></tr><tr><td>Allergy</td><td>Onset date</td><td>Date when the allergy started</td><td>Ext</td><td>No</td></tr><tr><td>Allergy</td><td>Agent description</td><td>Description of the allergen agent</td><td>Basic</td><td>Ext</td></tr><tr><td>Allergy</td><td>Agent code</td><td>The code of the allergen agent</td><td>Basic</td><td>Ext</td></tr></tbody></table>

## <mark style="color:blue;">Value Sets:</mark>

epSOSReactionAllergy

2.16.840.1.113883.6.96

If referred to the type (e.g. not allergic intolerance)

epSOSAdverseEventType

2.16.840.1.113883.6.96

WHO ATC

2.16.840.1.113883.6.73

If not:

epSOSAllergennoDrugs

2.16.840.1.113883.6.96






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=Allergy+IG&entry.670899847=Appendix%20F%3A%20Analysis%20of%20the%20epSOS%20information%20model" class="button primary">Provide Feedback</a>
