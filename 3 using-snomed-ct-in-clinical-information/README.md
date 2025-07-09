# Using SNOMED CT in Clinical Information

This section provides an overview of:

* How SNOMED CT supports reuse of clinical information
* Extent of practical use
* Approaches to implementation
* Lessons learnt
* Challenges

## Why is this important?

The objective of SNOMED International and all users of SNOMED CT is to facilitate the accurate recording and sharing of clinical and related health information and the semantic interoperability of health records.

## What is this?

### How SNOMED CT Supports Reuse of Clinical Information

SNOMED CT is a clinical terminology with global scope covering a wide range of clinical specialties, disciplines and requirements. As a result of its broad scope, one of the benefits of SNOMED CT is a reduction of specialty boundary effects that arise from use of different terminologies or coding systems by different clinicians or departments. This allows wider sharing and reuse of structured clinical information. Another benefit of SNOMED CT is that the same data can be processed and presented in ways that serve different purposes. For example, clinical records represented using SNOMED CT can be processed and presented in different ways to support direct patient care, clinical audit, research, epidemiology, management and service planning. Additionally, the global scope of SNOMED CT reduces geographical boundary effects arising from the use of different terminologies or coding systems in different organizations and countries.

With SNOMED CT, clinical information is recorded using identifiers that refer to concepts that are formally defined as part of the terminology. SNOMED CT supports recording of clinical information at appropriate levels of detail using relevant clinical concepts. The structures of SNOMED CT allow information to be entered using synonyms that suit local preferences while recording the information in a consistent and comparable form. Additionally, the hierarchical nature of SNOMED CT permits information to be recorded with different levels of detail to suit particular uses (e.g. <mark style="color:blue;">|</mark>pneumonia<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>bacterial pneumonia<mark style="color:blue;">|</mark> or <mark style="color:blue;">|</mark>pneumococcal pneumonia<mark style="color:blue;">|</mark>). SNOMED CT also allows additional detail to be added by combining concepts where the available concepts are not sufficiently precise. SNOMED CT allows a range of different options for immediate retrieval and subsequent reuse to address immediate and longer term clinical requirements and the requirements of other users. The nature of SNOMED CT hierarchies allow information to be selectively retrieved and reused to meet different requirements at various levels of generalization (e.g. retrieval of subtypes of <mark style="color:blue;">|</mark>lung disorder<mark style="color:blue;">|</mark> or <mark style="color:blue;">|</mark>bacterial infection<mark style="color:blue;">|</mark> would both include <mark style="color:blue;">|</mark>bacterial pneumonia<mark style="color:blue;">|</mark>).

The SNOMED CT concept model also allows additional details to be considered when retrieving data. For example, the concept |pneumococcal pneumonia| specifies that the <mark style="color:blue;">|</mark>causative agent<mark style="color:blue;">|</mark> is <mark style="color:blue;">|</mark>streptococcus pneumoniae<mark style="color:blue;">|</mark> and this allows the organism causing this disease to be analyzed.

### Extent of Practical Use

Many systems use SNOMED CT to represent some types of clinical information. The extent of use is varied in terms of:

* The clinical content captured (i.e. what is included and what is not).
* How the structure of this content relates to the structures in the records.
* The scope and consistency of use and reuse (i.e. within and across national and local organizations, across departments, within proprietary applications or specifically configured instances of proprietary applications).

### Approaches to Implementation

SNOMED CT has been implemented in a variety of ways which differ in the extent to which they harness particular features of the terminology. In some cases, these differences merely reflect the specific requirements of a particular use. Other factors include the design of existing systems prior to the introduction of SNOMED CT, sophistication of available technology and support for a range of other health informatics standards.

Key determinants for effective benefits realization include:

* Representation of stored clinical information.
  * To enable effective reuse of clinical information, SNOMED CT should be used within a record structure (or information model) that stores similar information consistently and in ways that can be readily queried.
* Ease of data entry
  * Different approaches to data entry are valuable and may be mediated in a variety of ways to enable ease of data entry.
  * The method of data entry should not result in inconsistent representations of the same types of clinical information.
  * The most effective approaches constrain data entry specific to the clinical context and reason for use.
  * Unconstrained searches across the entire content of SNOMED CT are rarely appropriate for routine data entry.
  * Constraints that limit data entry to a fixed set of SNOMED CT concepts are useful where the clinical context and reasons for use are narrow.
  * Constraints that alter dynamically to meet requirements of a particular data entry context offer a more generalizable approach that can be configured to meet different requirements.
  * Natural Language Processing (NLP) to parse and tag text with SNOMED CT expressions has been found useful in some applications.
* Communication interfaces, including message structures, need to be designed to retain the common elements of clinical content structure and coding. Communication should enable the receiving system to reuse the clinical information effectively based on the SNOMED CT expressions within it.
* Retrieval, analysis and reuse
  * Record storage and indexing can be designed to optimize use of the semantic features of SNOMED CT for selective retrieval and to support flexible analytics.
  * Retrieval in the patient care setting should result in the display of clinical records including highlighting of critical information selected taking account of the computer processable expressivity of SNOMED CT.
  * Real time decision support ranges from simple flagging of contraindications to guidelines for investigation and management.
  * Batch mode decision support identifies patients with chronic diseases and risk factors who require recalls for review and other scheduled interventions.
  * Analysis of data can be completed for selected populations of patients for a variety of purposes including audit, service planning, epidemiology and clinical research.

### Lessons Learnt

The features of SNOMED CT support reusability of clinical information. However, reusability also requires a consistent structured representation of clinical information that complements the meaning supported by SNOMED CT. Without this, overlaps and conflicts between structural and terminological representations of clinical content can result in ambiguous and potentially conflicting interpretations.

The way in which the use of terminology and structure together contribute to the representation of meaningful information is sometimes referred to as the "model of meaning". To enable widespread clinical information reuse, queries need to be consistently formulated in ways that take account of the way the information is structured and coded. A common model of meaning facilitates widespread reuse of clinical information, ability to reuse queries and a consistent approach to linkage between clinical information and knowledge resources.

Human factors may result in inconsistent recording of similar clinical information. This issue can be minimized by effectively constraining data entry.

### Challenges

An important limitation is the diversity of views related to the structure of clinical information and the overlap between information models and terminology. There are also differing views on application design, different requirements for collection of clinical information and different views on record structures and data entry methods appropriate to different use cases.

SNOMED International is working with other standards bodies including the International Organization for Standardisation (ISO) and Health Level 7 (HL7), as well as various collaborative efforts exploring the relationship between terminology and structured clinical information. The objective is to ensure that the role of SNOMED CT as a key component of clinical information and systems is understood as part of overall efforts towards harmonization and interoperability.






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=Starter+Guide&entry.670899847=Using%20SNOMED%20CT%20in%20Clinical%20Information" class="button primary">Provide Feedback</a>
