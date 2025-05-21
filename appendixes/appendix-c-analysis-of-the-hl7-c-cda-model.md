# appendix-c-analysis-of-the-hl7-c-cda-model

## Appendix C: Analysis of the HL7 C-CDA model

## C.1 HL7 C-CDA model

The Consolidated Clinical Document Architecture (C-CDA) specification (release 1.1 and 2.0) is required for communication of clinical data at transitions of care by the Office of the National Coordinator (ONC) for Health IT in the US. The ONC 2015 Edition Final Rule updated this requirement to specify the 2.1 version for Meaningful Use Stage 3 certification. The 2.1 C-CDA version includes an updated Allergy - Intolerance Observation (V2) 2.16.840.1.113883.10.20.22.4.7 template which includes a new Criticality Observation 2.16.840.1.113883.10.20.22.4.145 (replacing the previous Severity Observation (V2) at the allergy propensity level – the Severity Observation (V2) continues to be used in the Reaction Observation (V2)). The other relevant templates for use cases in section 3 are: Allergy Concern Act (V3) 2.16.840.1.113883.10.20.22.4.30 and Result Observation (V2) 2.16.840.1.113883.10.20.22.4.2.

The latest information about the HL7® C-CDA® standard can be found here: [http://www.hl7.org/implement/standards/product\_brief.cfm?product\_id=492](http://www.hl7.org/implement/standards/product_brief.cfm?product_id=492)

## C.2 Allergy Concern Act (V3)

This template reflects an ongoing concern on behalf of the provider that placed the allergy on a patient’s allergy list. As long as the underlying condition is of concern to the provider (i.e., as long as the allergy, whether active or resolved, is of ongoing concern and interest to the provider), the statusCode is “active”. Only when the underlying allergy is no longer of concern is the statusCode set to “completed”. The effectiveTime reflects the time that the underlying allergy was felt to be a concern.

The statusCode of the Allergy Concern Act is the definitive indication of the status of the concern, whereas the effectiveTime of the nested Allergy - Intolerance Observation is the definitive indication of whether or not the underlying allergy is resolved.

The effectiveTime/low of the Allergy Concern Act asserts when the concern became active. This equates to the time the concern was authored in the patient's chart. The effectiveTime/high asserts when the concern was completed (e.g., when the clinician deemed there is no longer any need to track the underlying condition).

## C.3 Allergy - Intolerance Observation (V2)

This template reflects a discrete observation about a patient's allergy or intolerance. Because it is a discrete observation, it will have a statusCode of "completed". The effectiveTime, also referred to as the "biologically relevant time" is the time at which the observation holds for the patient. For a provider seeing a patient in the clinic today, observing a history of penicillin allergy that developed five years ago, the effectiveTime is five years ago.

The effectiveTime of the Allergy - Intolerance Observation is the definitive indication of whether or not the underlying allergy/intolerance is resolved. If known to be resolved, then an effectiveTime/high would be present. If the date of resolution is not known, then effectiveTime/high will be present with a nullFlavor of "UNK".

The agent responsible for an allergy or adverse reaction is not always a manufactured material (for example, food allergies), nor is it necessarily consumed. The following constraints reflect limitations in the base CDA R2 specification, and should be used to represent any type of responsible agent, i.e., use playingEntity classCode = "MMAT" for all agents, manufactured or not.\
&#xNAN;**\_\_**

## C.4 Result Observation (V3)

This template represents the results of a laboratory, radiology, or other study performed on a patient.

The result observation includes a statusCode to allow recording the status of an observation. “Pending” results (e.g., a test has been run but results have not been reported yet) should be represented as “active” ActStatus.

For examples of C-CDA templates, see the [C-CDA implementation guide](http://www.hl7.org/implement/standards/product_brief.cfm?product_id=492).
