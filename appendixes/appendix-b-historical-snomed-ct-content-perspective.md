# Appendix B: Historical SNOMED CT content perspective

Efforts to revise the allergy-related hierarchies in SNOMED can be traced back to at least 2005 during which time several deficiencies were identified in the modeling of allergies and adverse reactions involving the inconsistent use of the causative agent role and the need to clearly differentiate the propensity to react from the reaction itself in order to better integrate with proposed HL7® models for allergy. Thus, allergy (disorder) was replaced by allergic state (disorder) as a child of 420134006 <mark style="color:blue;">|</mark> Propensity to adverse reactions (disorder)<mark style="color:blue;">|</mark> and adverse reactions/allergy to various substances, food and drugs were updated in the 2006 release of SNOMED CT. Additional revisions to the SNOMED CT allergy content occurred in 2006 included an attempt to align the terminology with the nomenclature for allergy developed by the WAO/EAAACI in 2001.

Another update to the allergy terminology was implemented for the July 2013 release of SNOMED CT. This update organized all of the three main allergy classes (_conditions, propensities and reactions_) which up to this point resided in three unrelated hierarchies under a single “allergy condition” hierarchy. Additionally, the July 2013 release included a more robust concept model for hypersensitivity/allergy conditions, particularly for the allergy propensity class (since named allergic disposition). Text definitions for the major organizing classes were also included for the first time.

Revising SNOMED CT to the three classes model meant that hypersensitivity data were represented by:

* Abnormal structures, which are diseases that may have a finding site and a morphology e.g. allergic rhinitis
* Dispositions (propensities), which model the patient state of an “Allergy to x”. <<420134006 <mark style="color:blue;">|</mark>Propensity to adverse reactions(finding)<mark style="color:blue;">|</mark>
* Processes (reactions) Example: “Allergic reaction to x”. <<281647001 <mark style="color:blue;">|</mark>adverse reaction (disorder)<mark style="color:blue;">|</mark>
* Conditions, which represent disorders characterized by abnormal structures, propensities that may be realized as pathologic processes (i.e. reactions) or the reactions themselves.
  * Example
    * 473011001 <mark style="color:blue;">|</mark>Allergic condition (finding)<mark style="color:blue;">|</mark>
      * 781474001 <mark style="color:blue;">|</mark>Allergic disorder (disorder)<mark style="color:blue;">|</mark>
      * 419076005 <mark style="color:blue;">|</mark>Allergic reaction (disorder)<mark style="color:blue;">|</mark>
      * 609328004 <mark style="color:blue;">|</mark>Allergic disposition (finding)<mark style="color:blue;">|</mark>







<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=Allergy+IG&entry.670899847=Appendix%20B%3A%20Historical%20SNOMED%20CT%20content%20perspective" class="button primary">Provide Feedback</a>
