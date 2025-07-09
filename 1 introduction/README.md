# Introduction

## Background

The capture and exchange of adverse sensitivity data (which encompasses allergy, non-allergic hypersensitivity and intolerance) vary across EHRs. As an effect, much of this data is not interoperable across electronic systems. Confusion regarding the representation and definition of adverse sensitivity data within the EHR presents challenges to organizations that are trying to implement SNOMED CT for electronic data sharing. Further, this uncertainty limits the use of adverse sensitivity data for clinical decision support and longitudinal patient care records. The capture of allergy data must be clearly defined to support patient safety and a comprehensive health record.

Several Standards Development Organizations (SDOs), such as HL7, have provided some general guidance to assist implementers, however specific guidance in using SNOMED CT within this domain is lacking.

## Objective

The overall objective of this guide is to promote interoperability within and between realms in a consistent way by providing clear guidance for structuring adverse sensitivity data as part of a patient’s Electronic Health Record.

In addition, the objective is to enable consistent adoption of SNOMED CT within the domain of adverse sensitivity data by providing guidance on the representation of relevant information with different levels of granularity, with and without the use of post-coordination.

## Scope

The scope of the work presented in this guide includes:

1. Review definitions and reference standards
2. Analyze relevant information models
   1. Review existing information models that are in scope, with special emphasis on HL7® FHIR® that has gained considerable momentum in recent years
3. Create exemplar use cases
   1. Describe the most common and important scenarios for capturing or exchanging adverse sensitivity information
   2. Illustrate how the information can be represented by using FHIR® and SNOMED CT concepts
4. Identify SNOMED CT subset
   1. Identify starter sets for large domains – most commonly used SNOMED CT concepts in clinical settings
   2. Identify value sets for specific data elements e.g., adverse sensitivity types, certainty, criticality, severity
5. Provide practical guidance on the use of SNOMED CT in
   1. Allergy list
   2. Problem list
   3. Clinical decision support

## Audience

SNOMED CT is a comprehensive, multilingual clinical terminology that can be used to standardize and improve the quality of data related to allergies, hypersensitivities, and intolerances. This guide is targeted at the various stakeholders involved with the implementation of SNOMED CT:

* **SNOMED International Members** who are seeking uniform, clear best practices for documenting adverse sensitivity, and understanding how SNOMED CT can be applied in this domain
* **Clinicians** who are interested in understanding how SNOMED CT can support the clinical needs for data collection and acquisition within the field of Allergy, Hypersensitivity, and Intolerance.
* **Information managers** who are looking to learn how SNOMED CT can be integrated into health information models within the domain of Allergy, Hypersensitivity, and Intolerance to support the implementation of SNOMED CT and enhance data interoperability.
* **Software developers** who want to learn how to integrate SNOMED CT into software applications used in the domain of Allergy, Hypersensitivity, and Intolerance.

## Attribution

This SNOMED CT Implementation guide and the underlying work have been developed by the **SNOMED International Clinical Reference Group for Allergies/Hypersensitivity**. The Clinical Reference Group (CRG) is composed of experts in the field of Allergies/Hypersensitivity providing input from the community of practice on the development, maintenance, and use of SNOMED CT in this specific domain. The CRG members have been instrumental in the development of this guide, providing their expertise, knowledge, and experience to ensure that it is accurate, up-to-date, and relevant to the needs of its intended audience. Their dedication and hard work have made this guide possible and SNOMED International is grateful for their contributions. This guide is a product of SNOMED International's ongoing commitment to improving healthcare through the use of high-quality, standardized clinical terminologies.

## Guide Overview

This SNOMED CT Implementation Guide is designed to provide guidance for the use of SNOMED CT within the domain of allergies, hypersensitivity, and intolerance. The guide is organized into five main sections:

* **Introduction** - This chapter provides a background on the guide, including the objectives, scope, and target audience.
* **Clinical Use Cases** - This chapter describes the key use cases that have motivated the creation of this guide and explains scenarios where implementation of SNOMED CT within this domain is needed.
* **Allergy Content in SNOMED CT** - This chapter describes how SNOMED CT addresses the terminological needs within the domain of allergies, hypersensitivities, and intolerances. It also elaborates on relevant editorial policies and concept model rules established to ensure the quality of the content.
* **Information Model and Terminology Binding** - This chapter introduces HL7 FHIR as a recommended information model that can be used within the field of allergies, hypersensitivities, and intolerances to facilitate the harmonization and interoperability of data within this domain. It also clarifies the bindings between this and SNOMED CT.
* **Technical Application** - This chapter presents technical considerations related the implementation of SNOMED CT and FHIR for allergy-related data capture.

In addition, a number of appendices present the results of the analysis performed and provide insights into the evolution of SNOMED CT and available information models.

* [Appendix A: Glossary of Terms](../appendixes/appendix-a-glossary-of-terms.md)
* [Appendix B: Historical SNOMED CT content perspective](../appendixes/appendix-b-historical-snomed-ct-content-perspective.md)
* [Appendix C: Analysis of the HL7 C-CDA model](../appendixes/appendix-c-analysis-of-the-hl7-c-cda-model.md)
* [Appendix D: Analysis of the HL7 Patient Care Domain Analysis Model](../appendixes/appendix-d-analysis-of-the-hl7-patient-care-domain-analysis-model.md)
* [Appendix E: Analysis of the ISO International Patient Summary (IPS)](../appendixes/appendix-e-analysis-of-the-iso-international-patient-summary-ips.md)
* [Appendix F: Analysis of the epSOS information model](../appendixes/appendix-f-analysis-of-the-epsos-information-model.md)
* [Appendix G: Analysis of the openEHR information model](../appendixes/appendix-g-analysis-of-the-openehr-information-model.md)
* [Appendix H: Analysis of the US Federal Health Information Model](../appendixes/appendix-h-analysis-of-the-us-federal-health-information-model.md)
* [Appendix I: Inclusive Information Model](../appendixes/appendix-i-inclusive-information-model.md)

## Review

This SNOMED CT Implementation guide represents the culmination of work started by the Implementation SIG in 2014 and and continued by the **SNOMED International Clinical Reference Group for Allergies/Hypersensitivity** starting in 2020.

We welcome feedback from readers on the guide and encourage them to share their insights and experiences with us. Your comments and suggestions will help us improve the content of the guide and ensure that it is relevant and useful to those who use it. We will review any feedback received and make updates to the guide as needed.

We appreciate your interest in this guide and thank you for your contributions to the improvement of healthcare through the use of high-quality, standardized clinical terminologies like SNOMED CT. Please raise any comments to this document via the feedback button (At the bottom of the page).
