# 4. SNOMED CT Basics

This section provides an overview of:

  * [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") features

  * Exploring [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT")

  * [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") design and development

  * [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") [components](https://confluence.ihtsdotools.org/display/DOCGLOSS/component "Glossary link: components") components and [hierarchies](https://confluence.ihtsdotools.org/display/DOCGLOSS/hierarchy "Glossary link: hierarchies")

  * SNOMED CT characteristics
  * SNOMED CT supporting different languages
  * SNOMED CT products and services

## Why is this important?

An awareness of [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") features, [components](https://confluence.ihtsdotools.org/display/DOCGLOSS/component "Glossary link: components"), characteristics and products provides an initial foundation on which to build greater understanding. It also informs discussions leading to decisions about adoption, implementation and use of this terminology.

## What is this?

### SNOMED CT Features

[SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT"):

  * Is the most comprehensive, multilingual clinical healthcare terminology in the world.
  * Is a resource with comprehensive, scientifically validated clinical content.
  * Enables consistent, processable representation of clinical content in [electronic health records](https://confluence.ihtsdotools.org/display/DOCGLOSS/electronic+health+record "Glossary link: electronic health records").

  * Is mapped to other international standards.
  * Is already used in more than eighty countries.

When implemented in software applications, [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") can be used to represent clinically relevant information consistently, reliably and comprehensively as an integral part of producing electronic health information.

Implementation requires an understanding of the way that [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") content is represented by [components](https://confluence.ihtsdotools.org/display/DOCGLOSS/component "Glossary link: components") and supported by [reference sets](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference sets") (Refsets).

### Exploring SNOMED CT

While reading the guide, you may find it useful to explore the content of [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT"). You can do this using one of a range of online [browsers](https://confluence.ihtsdotools.org/display/DOCGLOSS/browser "Glossary link: browsers") listed on our web site at <https://www.implementation.snomed.org/browsers>. Note that the listed [browsers](https://confluence.ihtsdotools.org/display/DOCGLOSS/browser "Glossary link: browsers") are not endorsed by [SNOMED International](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+International "Glossary link: SNOMED International") and they should only be used to a get feel for the content and structure of the terminology. It is useful to experiment with several different [browsers](https://confluence.ihtsdotools.org/display/DOCGLOSS/browser "Glossary link: browsers") as they vary in the way they present particular features of the terminology.

<img src="images/29952942.png" alt="" title="" width="" height="">

## SNOMED CT Design and Development

### SNOMED CT Components

SNOMED CT is a core clinical healthcare terminology that contains [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts") with unique meanings and formal logic based definitions organized into [hierarchies](https://confluence.ihtsdotools.org/display/DOCGLOSS/hierarchy "Glossary link: hierarchies"). [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") content is represented using three types of [components](https://confluence.ihtsdotools.org/display/DOCGLOSS/component "Glossary link: components"):

  * [Concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/Concept "Glossary link: Concepts") representing clinical meanings that are organized into hierarchies.

  * [Descriptions](https://confluence.ihtsdotools.org/display/DOCGLOSS/Description "Glossary link: Descriptions") which link appropriate human readable [terms](https://confluence.ihtsdotools.org/display/DOCGLOSS/term "Glossary link: terms") to [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts").

  * [Relationships](https://confluence.ihtsdotools.org/display/DOCGLOSS/Relationship "Glossary link: Relationships") which link each concept to other related [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts").

These [components](https://confluence.ihtsdotools.org/display/DOCGLOSS/component "Glossary link: components") are supplemented by [reference sets](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference sets"), which provide additional flexible features and enable configuration of the terminology to address different requirements.

#### Concepts

[SNOMED CT concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+concept "Glossary link: SNOMED CT concepts") represent clinical thoughts, ranging from |abscess| to |zygote|. Every [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") has a unique numeric [concept identifier](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept+identifier "Glossary link: concept identifier"). Within each [hierarchy](https://confluence.ihtsdotools.org/display/DOCGLOSS/hierarchy "Glossary link: hierarchy"), [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts") are organized from the general to the more detailed. This allows detailed clinical data to be recorded and later accessed or aggregated at a more general level.

#### Descriptions

[SNOMED CT descriptions](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+description "Glossary link: SNOMED CT descriptions") link appropriate human readable terms to [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts"). A [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") can have several associated [descriptions](https://confluence.ihtsdotools.org/display/DOCGLOSS/description "Glossary link: descriptions"), each representing a [synonym](https://confluence.ihtsdotools.org/display/DOCGLOSS/synonym "Glossary link: synonym") that describes the same clinical concept. Each [translation](https://confluence.ihtsdotools.org/display/DOCGLOSS/translation "Glossary link: translation") of [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") includes an additional set of [descriptions](https://confluence.ihtsdotools.org/display/DOCGLOSS/description "Glossary link: descriptions"), which link [terms](https://confluence.ihtsdotools.org/display/DOCGLOSS/term "Glossary link: terms") in another [language](https://confluence.ihtsdotools.org/display/DOCGLOSS/language "Glossary link: language") to the same [SNOMED CT concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+concept "Glossary link: SNOMED CT concepts"). Every [description](https://confluence.ihtsdotools.org/display/DOCGLOSS/description "Glossary link: description") has a unique numeric [description identifier](https://confluence.ihtsdotools.org/display/DOCGLOSS/description+identifier "Glossary link: description identifier").

#### Relationships

[SNOMED CT relationships](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+relationship "Glossary link: SNOMED CT relationships") link concepts to other [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts") whose meaning is related in some way. These [relationships](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship "Glossary link: relationships") provide formal definitions and other properties of the [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept"). One type of [relationship](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship "Glossary link: relationship") is the [is a](https://confluence.ihtsdotools.org/display/DOCGLOSS/is+a "Glossary link: is a") relationship which relates a [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") to more general [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts"). These [is a](https://confluence.ihtsdotools.org/display/DOCGLOSS/is+a "Glossary link: is a") relationships define the [hierarchy](https://confluence.ihtsdotools.org/display/DOCGLOSS/hierarchy "Glossary link: hierarchy") of [SNOMED CT concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+concept "Glossary link: SNOMED CT concepts").

  * For example, the [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts") |bacterial pneumonia| and |viral pneumonia| both have an |is a| relationship to |infective pneumonia| which has an |is a| relationship to the more general [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") |pneumonia|.

Other types of [relationships](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship "Glossary link: relationships") represent aspects of the meaning of a [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept").

  * For example, the [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") |viral pneumonia| has a |causative agent| relationship to the [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") |virus| and a |finding site| [relationship](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship "Glossary link: relationship") to the [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") |lung|.

Every [relationship](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship "Glossary link: relationship") has a unique numeric [relationship](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship "Glossary link: relationship") [identifier](https://confluence.ihtsdotools.org/display/DOCGLOSS/identifier "Glossary link: identifier").

#### Reference sets

[Reference sets](https://confluence.ihtsdotools.org/display/DOCGLOSS/Reference+set "Glossary link: Reference sets") (Refsets) are a flexible standard approach used by [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") to support a variety of requirements for customization and enhancement of [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT"). These include the representation of [subsets](https://confluence.ihtsdotools.org/display/DOCGLOSS/subset "Glossary link: subsets"), language preferences for use of particular [terms](https://confluence.ihtsdotools.org/display/DOCGLOSS/term "Glossary link: terms") and [mapping](https://confluence.ihtsdotools.org/display/DOCGLOSS/mapping "Glossary link: mapping") from or to other code systems. Every [reference set](https://confluence.ihtsdotools.org/display/DOCGLOSS/reference+set "Glossary link: reference set") has a unique numeric [concept identifier](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept+identifier "Glossary link: concept identifier").

### SNOMED CT Hierarchies

[SNOMED CT concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+concept "Glossary link: SNOMED CT concepts") are organized in hierarchies. Within a [hierarchy](https://confluence.ihtsdotools.org/display/DOCGLOSS/hierarchy "Glossary link: hierarchy") [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts") range from the more general to the more detailed. Related [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts") in the [hierarchy](https://confluence.ihtsdotools.org/display/DOCGLOSS/hierarchy "Glossary link: hierarchy") are linked using the |is a| relationship.

  * Examples of some of the hierarchies include |clinical finding|, |procedure|, |observable entity|, |body structure| and |organism|.

### SNOMED CT Characteristics - Comprehensive, Scalable and Flexible

[SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") has a broad coverage of health related topics. It can be used to describe a patient's medical history, the details of an orthopedic procedure, the spread of epidemics, and much more. At the same time, the terminology has an unmatched depth, which enables clinicians to record data at the appropriate level of granularity.

Specific applications tend to focus on a restricted set of [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT"), such as [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts") related to ophthalmology. These [subsets](https://confluence.ihtsdotools.org/display/DOCGLOSS/subset "Glossary link: subsets") can be used to present relevant parts of the terminology, depending on the clinical context and local requirements. This means for example, that a drop down list to select diagnoses in an [electronic health record](https://confluence.ihtsdotools.org/display/DOCGLOSS/electronic+health+record "Glossary link: electronic health record") in a mental health facility can be tailored to that setting. Similarly, [subsets](https://confluence.ihtsdotools.org/display/DOCGLOSS/subset "Glossary link: subsets") can be defined for problem lists for physician specialties or to provide appropriate medication lists for nurses in community care.

When individual jurisdictions have needs beyond those that can be reflected in a global terminology, perhaps due to requirements in local legislation, they can develop local or national [extensions](https://confluence.ihtsdotools.org/display/DOCGLOSS/extension "Glossary link: extensions"). Thus, even though [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") is global in scope, it can be adapted to each country's or areas requirements. [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") maps work to provide explicit links to health related classifications and coding schemes in use around the world, e.g. [statistical classifications](https://confluence.ihtsdotools.org/display/DOCGLOSS/statistical+classification "Glossary link: statistical classifications") such as [ICD-9-CM](https://confluence.ihtsdotools.org/display/DOCGLOSS/ICD-9-CM "Glossary link: ICD-9-CM"), [ICD-10](https://confluence.ihtsdotools.org/display/DOCGLOSS/ICD-10 "Glossary link: ICD-10"), and [ICD-O3](https://confluence.ihtsdotools.org/display/DOCGLOSS/ICD-O3 "Glossary link: ICD-O3"). Maps to or from several national code systems are also available from, or under development, by [Members](https://confluence.ihtsdotools.org/display/DOCGLOSS/Member "Glossary link: Members"). Maps to or from clinical domain specific code systems are also maintained by specialty groups with which [SNOMED International](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+International "Glossary link: SNOMED International") has collaborative agreement. Maps facilitate reuse of [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") based clinical data for other purposes, such as reimbursement or statistical reporting.

### Supporting Different Languages

[SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") is a multinational, multilingual terminology. It has a built-in framework to manage different [languages](https://confluence.ihtsdotools.org/display/DOCGLOSS/language "Glossary link: languages") and [dialects](https://confluence.ihtsdotools.org/display/DOCGLOSS/dialect "Glossary link: dialects"). The [International Release](https://confluence.ihtsdotools.org/display/DOCGLOSS/International+Release "Glossary link: International Release") includes a set of language independent [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts") and [relationships](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship "Glossary link: relationships"). Today, [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") is available in many [languages](https://confluence.ihtsdotools.org/display/DOCGLOSS/language "Glossary link: languages") that can be viewed in the [SNOMED International SNOMED CT Browser](https://browser.ihtsdotools.org/). The basic objective of any [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") [translation](https://confluence.ihtsdotools.org/display/DOCGLOSS/translation "Glossary link: translation") is to provide accurate representations of [SNOMED CT concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT+concept "Glossary link: SNOMED CT concepts") in a way that is understandable, usable, and safe. [Translation](https://confluence.ihtsdotools.org/display/DOCGLOSS/Translation "Glossary link: Translation") must be [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") based. Translators need to analyse [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts") based on the [fully specified name](https://confluence.ihtsdotools.org/display/DOCGLOSS/fully+specified+name "Glossary link: fully specified name") and take account of its position within the [hierarchy](https://confluence.ihtsdotools.org/display/DOCGLOSS/hierarchy "Glossary link: hierarchy"), its [descriptions](https://confluence.ihtsdotools.org/display/DOCGLOSS/description "Glossary link: descriptions"), and its [relationships](https://confluence.ihtsdotools.org/display/DOCGLOSS/relationship "Glossary link: relationships") to other [concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concepts"). This enables a meaningful [translation](https://confluence.ihtsdotools.org/display/DOCGLOSS/translation "Glossary link: translation") of a [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") based on phrases that are well used and clearly understood in all countries. [SNOMED International](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+International "Glossary link: SNOMED International") maintains guidelines and other materials to support countries undertaking translations.

### SNOMED CT Products and Services

[Members](https://confluence.ihtsdotools.org/display/DOCGLOSS/Member "Glossary link: Members") and organizations covered by the SNOMED CT [Affiliate License](https://confluence.ihtsdotools.org/display/DOCGLOSS/Affiliate+License "Glossary link: Affiliate License") have access to a range of products and services, including:

  * SNOMED CT terminology files consisting of:
    * [Concepts](https://confluence.ihtsdotools.org/display/DOCGLOSS/Concept "Glossary link: Concepts")

    * [Descriptions](https://confluence.ihtsdotools.org/display/DOCGLOSS/Description "Glossary link: Descriptions")

    * [Relationships](https://confluence.ihtsdotools.org/display/DOCGLOSS/Relationship "Glossary link: Relationships")

  * [Derivative](https://confluence.ihtsdotools.org/display/DOCGLOSS/Derivative "Glossary link: Derivative") works that help in the uptake and use of [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT"), including [Reference Sets](https://confluence.ihtsdotools.org/display/DOCGLOSS/Reference+Set "Glossary link: Reference Sets") that support:

    * Identification of [subsets](https://confluence.ihtsdotools.org/display/DOCGLOSS/subset "Glossary link: subsets") of SNOMED CT content

    * [Language](https://confluence.ihtsdotools.org/display/DOCGLOSS/Language "Glossary link: Language") or [dialect](https://confluence.ihtsdotools.org/display/DOCGLOSS/dialect "Glossary link: dialect") preferences for use of particular [descriptions](https://confluence.ihtsdotools.org/display/DOCGLOSS/description "Glossary link: descriptions")

    * Maps to other code systems and classifications
    * Other relevant [metadata](https://confluence.ihtsdotools.org/display/DOCGLOSS/metadata "Glossary link: metadata") to support use of [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") [components](https://confluence.ihtsdotools.org/display/DOCGLOSS/component "Glossary link: components").

  * Implementation guidance for successful use of [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") including:

    * Implementation guidance
    * Translation guidance
    * Editorial guidance for content development
  * Access to services supporting submission of requests for changes or additions to content and documentation.
  * Participation in the global [SNOMED International](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+International "Glossary link: SNOMED International") community through an electronic collaborative space and meeting of special interest groups.

  

  

