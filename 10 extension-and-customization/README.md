# 10. Extension and Customization

This section provides an overview of:

  * Extension Content
  * Reference Sets

## Why is this important?

SNOMED CT is designed to allow the International Edition to be enhanced by adding Extensions that address national or local requirements. Additional content required to support national, local or organizational needs that may not have international relevance or may not meet the editorial guideline for inclusion in the International Edition.

SNOMED CT design also includes the Reference Set mechanism which provides a standard way to customize and enhance content for use in a particular country, language, specialty, application or context. Reference Sets developed nationally or locally can modify search and display of content from the International Edition as well as enhancing Extension content.

## What is this?

### Extension Content

Many clinical concepts are relevant in all countries, organizations and specialties but some concepts are relevant only to a particular environment. SNOMED CT is designed to allow the International Edition to be enhanced by adding Extensions to meet national or local requirements without compromising the main body of SNOMED CT. This is intended to meet the needs of different specialties and countries, regions, vendors and healthcare institutions.

Extensions are managed by Members or Affiliates who have been issued with a Namespace Identifier. A Namespace Identifier distinguishes the Identifiers of the Components created by an organization. The responsibilities of organizations that create an Extension and provide it for use by other organizations include:

  * Maintaining Concept, Descriptions, Relationships, and Reference Sets that they create.
  * Inactivating these components as appropriate (duplication, ambiguous, outdated, etc.)

The Concepts, Descriptions, Relationship and Reference Sets that form an Extension use a namespace identifier, which ensures that their SNOMED CT identifier is different from components in:

  * SNOMED CT International Release,
  * Other SNOMED CT Extensions

The namespace identifier is part of the component identifier. Therefore, components are distinguishable not only in the thesaurus, but also when stored in a patient record, query or decision support protocol.

Extensions use the same file structure as the core International Release. This ensures that:

  * SNOMED CT enabled implementations can benefit from the content in these Extensions without the need for any additional software development;
  * The same application software can be used to enter, store and process information from different extensions;
  * Reference Sets can be constructed that refer to content from the International Release and a variety of Extensions.

Software applications should allow the users or user communities to specify the Extensions to be recognized by their systems.

An Extension should only be recognized if:

  * It has been supplied by SNOMED International or another organization authorized by SNOMED International to provide such Extensions;
  * The recognizing organization is satisfied with the quality control procedures of the providing organization.

The fact that an organization is permitted to produce Extensions does not imply a seal of approval of the quality of Extensions that organization produces. Therefore a person or organization that authorizes or installs an Extension does so entirely at their own risk.

### Reference Sets

SNOMED CT has a broad clinical coverage and includes a depth of detail appropriate to a range of health care disciplines and clinical specialties. As a result, it has extensive content, different parts of which are needed in particular environments. The SNOMED CT design includes the Reference Set mechanism, which provides a standard way to refer to a set of SNOMED CT components and to add customized information to a component.

Organizations implementing SNOMED CT benefit from Reference Sets because they allow requirements for use of particular descriptions and concepts to be represented in a standard form that can be applied to any SNOMED CT enabled application. This allows Reference Sets to be shared throughout and between organizations, even when different software is used to meet local or departmental requirements.

Software developers and vendors benefit because Reference Sets provide a common, machine processable representation of requirements for different patterns of use of SNOMED CT. This simplifies local configuration and enhances interoperability with other SNOMED CT enabled applications.

Reference sets can be used for many different purposes, including:

  * **Language and dialects** are represented as Language Reference Sets (see Chapter 11 - Translations and Language Preferences).
  * **Maps to and from other code systems and classifications** are represented as Simple, Complex or Extended Map Reference Sets (see Chapter 12 - Mapping).
  * **Subsets of concepts, description or relationships** are represented as Simple Reference Sets. The only information that a Simple Reference Set provides is that a component is part of this subset. Subsets may be used for a variety of general and specific purposes, some of which are identified in the following examples.
  * **Ordered lists and navigation hierarchies** are represented as Ordered Reference Sets. These offer additional functionality to meet advanced variants of the requirements addressed by component subsets.

#### General use cases for subsets represented as Simple Reference Sets

  * **Excluding content**  

    * Reference sets can be used to exclude concepts that are not required by a particular use case.
  * **Including content**  

    * Limiting searches to content of specific interest to a specialty or specific data entry context
    * In some cases very limited subsets can be presented as dropdown lists or option boxes rather than searches.
  * **Prioritizing content**  

    * In some cases, a subset represents an initial priority list of options but the full content of SNOMED CT is searchable when required.
    * Note that Ordered Reference Sets support more flexible prioritization.
  * **Managing use of codes in messages and communications**
    * A Simple Reference Set may represent a value set applicable to a particular field in a message.

#### Specific use cases for subsets represented as Simple Reference Sets

  * **National, jurisdictional or organizational requirements**  

    * Collecting particular minimum sets of data using specific codes.
  * **Regional variations in disease prevalence**  

    * Providing prioritized access to diseases that are prevalent in the region where data is being collected.
  * **Specialty and discipline****variations**  

    * The frequency of use of particular concepts depends on the professional discipline and/or clinical specialty of the user. Specialty subsets can optimize data entry.
  * **Supporting data entry protocols**  

    * Different subsets of concepts are relevant at different points in different data entry protocols. Subsets represented as Simple Reference Sets can be used to restrict the available options to match the requirements at particular points in a data entry protocol.  

#### Reference set development

Generic data structures for Reference Sets have been used to create a simple core structure that can be extended to meet a variety of requirements. This has been done rather than developing a complex and inextensible structure that can only be used in a finite and constrained number of ways to enforce editorial policy.

Creating a new Reference Set requires access to a namespace in order to generate SNOMED CT Ids. Within that namespace, at least one module ID concept (with an FSN and Preferred Term) should be added under the |module| sub-hierarchy (within the Core Metadata) for each of the authoring organizations. The steps required to create a new reference set include:

  1. Create the Reference Set Concept in the Foundation Metadata hierarchy.
  2. Define the Reference Set Attributes within the metadata hierarchy.
  3. Create the Descriptor for the Reference Set (by adding members to the Reference Set Descriptor Reference Set).
  4. Add members to the Reference Set.

Please note that step 2 does not need to be performed if using one of the standard Reference Set types that have been predefined in the international release of SNOMED CT. The Reference Set Attributes for these predefined Reference Set types have already been added to the international release.

It is recommended that for each reference set, there is formal documentation that records (at a minimum) the rules, principles and approach used to determine the members of that reference set.

Reference Sets need to be maintained and the content re-examined when new releases of SNOMED CT are made available. Processes need to be established to address the concepts that have become inactive and the new concepts added in each new release.
