# SNOMED CT Concept Model

This section provides an overview of:

* Concept Model – Top Level Hierarchies
* Concept Model Attributes – Representing Characteristics of a Concept

## Why is this important?

The SNOMED CT concept model specifies the way in which SNOMED CT concepts are defined using a combination of formal logic and editorial rules. Concept model rules specify the top level concepts under which concepts are arranged in the subtype hierarchy and the types of relationships that are permitted between concepts in particular branches of the hierarchy.

## What is this?

### Concept Model – Top Level Hierarchies

The top of the SNOMED CT hierarchy is occupied by the root concept (<mark style="color:blue;">|</mark>SNOMED CT concept<mark style="color:blue;">|</mark>). All concepts are descended from this root concept through at least one sequence of <mark style="color:blue;">|</mark>is a<mark style="color:blue;">|</mark> relationships. This means that the root concept is a supertype of all other concepts and all other concepts are subtypes of the root concept.

The direct subtypes of the root concept are referred to as 'Top Level Concepts'. These concepts are used to name the main branches of the hierarchy. Each of these Top Level Concepts, together with their many subtype descendants, forms a major branch of the SNOMED CT hierarchy and contains similar types of concepts. As the hierarchies descend (that is, more <mark style="color:blue;">|</mark>is a<mark style="color:blue;">|</mark> relationships are added below the Top Level Concepts) the concepts within them become increasingly specific.

Below is a list of the Top Level Concepts with a brief description of the content represented in their branch of the hierarchy.

* <mark style="color:blue;">|</mark>**Clinical finding**<mark style="color:blue;">|</mark> represents the result of a clinical observation, assessment or judgment and includes normal and abnormal clinical states (e.g. <mark style="color:blue;">|</mark>asthma<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>headache<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>normal breath sounds<mark style="color:blue;">|</mark>). The <mark style="color:blue;">|</mark>clinical finding<mark style="color:blue;">|</mark> hierarchy includes concepts used to represent diagnoses.
* <mark style="color:blue;">|</mark>**Procedure**<mark style="color:blue;">|</mark> represents activities performed in the provision of health care. This includes not only invasive procedures but also administration of medicines, imaging, education, therapies and administrative procedures (e.g. <mark style="color:blue;">|</mark>appendectomy<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>physiotherapy<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>injection into subcutaneous tissue<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Situation with explicit context**<mark style="color:blue;">|</mark> represents concepts in which the clinical context is specified as part of the definition of the concept itself. These include presence or absence of a condition, whether a clinical finding is current, in the past or relates to someone other than the subject of the record (e.g. <mark style="color:blue;">|</mark>endoscopy arranged<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>past history of myocardial infarction<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>family history of glaucoma<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Observable entity**<mark style="color:blue;">|</mark> represents a question or assessment which can produce an answer or result (e.g. <mark style="color:blue;">|</mark>systolic blood pressure<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>color of iris<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>gender<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Body structure**<mark style="color:blue;">|</mark> represents normal and abnormal anatomical structures (e.g. <mark style="color:blue;">|</mark>mitral valve structure<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>adenosarcoma<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Organism**<mark style="color:blue;">|</mark> represents organisms of significance in human medicine (e.g. <mark style="color:blue;">|</mark>streptococcus pyogenes<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>domain Bacteria<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>glossina<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Substance**<mark style="color:blue;">|</mark> represents general substances, the chemical constituents of pharmaceutical/biological products, body substances, dietary substances and diagnostic substances (e.g. <mark style="color:blue;">|</mark>methane<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>insulin<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>albumin<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Pharmaceutical**/**biologic product**<mark style="color:blue;">|</mark> represents drug products (e.g. <mark style="color:blue;">|</mark>amoxicillin 250mg oral capsule<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>product containing codeine and paracetamol<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Specimen**<mark style="color:blue;">|</mark> represents entities that are obtained (usually from the patient) for examination or analysis (e.g. <mark style="color:blue;">|</mark>urine specimen<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>specimen from prostate obtained by needle biopsy<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Special concept**<mark style="color:blue;">|</mark> represents concepts that do not play a part in the formal logic of the concept model of the terminology, but which may be useful for specific use cases (e.g. <mark style="color:blue;">|</mark>navigational concept<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>alternative medicine poisoning<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Physical object**<mark style="color:blue;">|</mark> represents natural and man-made physical objects (e.g. <mark style="color:blue;">|</mark>vena cava filter<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>implant device<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>automobile<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Physical force**<mark style="color:blue;">|</mark> represents physical forces that can play a role as mechanisms of injury (e.g. <mark style="color:blue;">|</mark>friction<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>radiation<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>alternating current<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Event**<mark style="color:blue;">|</mark> represents occurrences excluding procedures and interventions (e.g. <mark style="color:blue;">|</mark>flood<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>earthquake<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Environments and geographical locations**<mark style="color:blue;">|</mark> represents types of environments as well as named locations such as countries, states and regions (e.g. <mark style="color:blue;">|</mark>intensive care unit<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>academic medical center<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>Denmark<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Social context**<mark style="color:blue;">|</mark> represents social conditions and circumstances significant to health care (e.g. <mark style="color:blue;">|</mark>occupation<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>spiritual or religious belief<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Staging and scales**<mark style="color:blue;">|</mark> represents assessment scales and tumor staging systems (e.g. <mark style="color:blue;">|</mark>Glasgow Coma Scale<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>FIGO staging system of gynecological malignancy<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Qualifier value**<mark style="color:blue;">|</mark> represents the values for some SNOMED CT attributes, where those values are not subtypes of other top level concepts. (e.g. <mark style="color:blue;">|</mark>left<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>abnormal result<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>severe<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**Record artifact**<mark style="color:blue;">|</mark> represents content created for the purpose of providing other people with information about record events or states of affairs. (e.g. <mark style="color:blue;">|</mark>patient held record<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>record entry<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>family history section<mark style="color:blue;">|</mark>).
* <mark style="color:blue;">|</mark>**SNOMED CT Model Component**<mark style="color:blue;">|</mark> contains technical metadata supporting the SNOMED CT release.

### Concept Model Attributes – Representing Characteristics of a Concept

SNOMED CT attributes (or relationship types) are used to represent a characteristic of the meaning of a concept. SNOMED CT currently uses more than one hundred defining attributes when defining the meaning of concepts. Each SNOMED CT attribute can be applied to concepts in one or more branches of the hierarchy. The set of concepts to which an attribute can be applied is called the 'domain' of the attribute. The permitted set of values for each attribute is called the 'range' of the attribute.

#### _**Domain**_

The _domain_ is the hierarchy to which a specific attribute can be applied.

For example:

The domain of the attribute <mark style="color:blue;">|</mark>associated morphology<mark style="color:blue;">|</mark> is the <mark style="color:blue;">|</mark>clinical finding<mark style="color:blue;">|</mark> hierarchy. Therefore, a <mark style="color:blue;">|</mark>procedure<mark style="color:blue;">|</mark> cannot have an <mark style="color:blue;">|</mark>associated morphology<mark style="color:blue;">|</mark>. However, a <mark style="color:blue;">|</mark>procedure<mark style="color:blue;">|</mark> can have a <mark style="color:blue;">|</mark>procedure morphology<mark style="color:blue;">|</mark>.

#### _**Range**_

The _range_ is the set of SNOMED CT concepts or concrete values that are allowed as the value of a specified attribute.

For example:

The range for the attribute |associated morphology| is the concept <mark style="color:blue;">|</mark>morphologically abnormal structure<mark style="color:blue;">|</mark> and its subtype descendants. The range for the attribute <mark style="color:blue;">|</mark>finding site<mark style="color:blue;">|</mark> is <mark style="color:blue;">|</mark>anatomical or acquired body structure<mark style="color:blue;">|</mark> and its subtype descendants in the <mark style="color:blue;">|</mark>body structure<mark style="color:blue;">|</mark> hierarchy.

_Examples of the domain and range specified for the attributes_ _<mark style="color:blue;">|</mark>finding site<mark style="color:blue;">|</mark>_ _and_ _<mark style="color:blue;">|</mark>laterality<mark style="color:blue;">|</mark>_

<figure><img src="../images/29952962.png" alt=""><figcaption></figcaption></figure>

Some SNOMED CT attributes (or relationship types) have a hierarchical relationship to one another. The hierarchy formed from such relationships is known as an 'attribute hierarchy'. In an attribute hierarchy, one general attribute is the parent of one or more specific subtypes of that attribute. Subtypes of a concept defined using the more general attribute can be defined using a more specific subtype of that attribute. For example, <mark style="color:blue;">|</mark>after<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>causative agent<mark style="color:blue;">|</mark> and <mark style="color:blue;">|</mark>due to<mark style="color:blue;">|</mark> are subtypes of <mark style="color:blue;">|</mark>associated with<mark style="color:blue;">|</mark>, because they have a more specific meaning.

### Concept Model and Editorial Guidance

#### Editorial Guide

SNOMED CT is an evolving terminology, which means that the attributes used to define concepts in specific hierarchies may change over time. Additionally, editorial principles, that are specified to ensure consistent representation of the same type of concepts may also change. When authoring SNOMED CT content, it is therefore important to always refer to the current SNOMED CT Editorial Guide. The Editorial Guide specifies the attributes that are valid to use within each hierarchy and the valid values that can be assigned to each attribute. It also presents general editorial rules for SNOMED CT content, along with specific guidance on authoring concepts within each hierarchy.

#### Machine Readable Concept Model

The Machine Readable Concept Model (MRCM) represents rules in the SNOMED CT concept model in a form that can be read by a computer and applied to test that concept definitions and expressions comply with the rules. The MRCM may be used for a variety of purposes, including the authoring and validation of SNOMED CT concepts, expressions, expression constraints and queries, Natural Language Processing and terminology binding to support semantic interoperability. For further information, please visit the guide on the Machine Readable Concept Model or visit the MRCM Browser.

### Attributes Used to Define SNOMED CT Concepts

The SNOMED CT defining attributes are used to represent the meaning of concepts in many hierarchies, for example:

* Clinical finding concepts
* Procedure concepts

For further information, please refer to the SNOMED CT Editorial Guide.

#### Attributes Used to Define Clinical Finding Concepts

Below is a list of some of the attributes used to define |clinical finding| concepts, and a brief description of their meaning:

<mark style="color:blue;">|</mark>**Finding site**<mark style="color:blue;">|</mark> specifies the body site affected by a condition.

<mark style="color:blue;">|</mark>**Associated morphology**<mark style="color:blue;">|</mark> specifies the morphologic changes seen at the tissue or cellular level that are characteristic features of a disease.

<mark style="color:blue;">|</mark>**Associated with**<mark style="color:blue;">|</mark> represents a clinically relevant association between concepts without either asserting or excluding a causal or sequential relationship between the two.

<mark style="color:blue;">|</mark>**After**<mark style="color:blue;">|</mark> represents a sequence of events where a clinical finding occurs after another <mark style="color:blue;">|</mark>clinical finding<mark style="color:blue;">|</mark> or <mark style="color:blue;">|</mark>procedure<mark style="color:blue;">|</mark> or <mark style="color:blue;">|</mark>event<mark style="color:blue;">|</mark>.

<mark style="color:blue;">|</mark>**Due to**<mark style="color:blue;">|</mark> relates a <mark style="color:blue;">|</mark>clinical finding<mark style="color:blue;">|</mark> directly to a cause such as another <mark style="color:blue;">|</mark>clinical finding<mark style="color:blue;">|</mark> or a <mark style="color:blue;">|</mark>procedure<mark style="color:blue;">|</mark>.

<mark style="color:blue;">|</mark>**Causative agent**<mark style="color:blue;">|</mark> identifies the direct causative agent of a disease such as an <mark style="color:blue;">|</mark>organism<mark style="color:blue;">|</mark>, <mark style="color:blue;">|</mark>substance<mark style="color:blue;">|</mark> or <mark style="color:blue;">|</mark>physical force<mark style="color:blue;">|</mark>. (Note: This attribute is not used for vectors, such as mosquitos transmitting malaria).

<mark style="color:blue;">|</mark>**Severity**<mark style="color:blue;">|</mark> used to sub-class a |clinical finding| concept according to its relative severity.

<mark style="color:blue;">|</mark>**Clinical course**<mark style="color:blue;">|</mark> represents both the onset and course of a disease.

<mark style="color:blue;">|</mark>**Episodicity**<mark style="color:blue;">|</mark> represents episodes of care provided by a physician or other care provider, such as a general practitioner. This attribute is not used to represent episodes of disease experienced by the patient.

<mark style="color:blue;">|</mark>**Interprets**<mark style="color:blue;">|</mark> refers to the entity being evaluated or interpreted, when an evaluation, interpretation or judgment is intrinsic to the meaning of a concept.

<mark style="color:blue;">|</mark>**Has interpretation**<mark style="color:blue;">|</mark> when grouped with the attribute <mark style="color:blue;">|</mark>interprets<mark style="color:blue;">|</mark>, designates the judgment aspect being evaluated or interpreted for a concept. (e.g. presence, absence etc.)

<mark style="color:blue;">|</mark>**Pathological process**<mark style="color:blue;">|</mark> provides information about the underlying pathological process of a disorder, i.e. it describes the process that results in the structural or morphologic change.

<mark style="color:blue;">|</mark>**Occurrence**<mark style="color:blue;">|</mark> refers to a specific period of life during which a condition first presents.

<mark style="color:blue;">|</mark>**Finding method**<mark style="color:blue;">|</mark> specifies the means by which a clinical finding was determined. This attribute is frequently used in conjunction with |finding informer|.

<mark style="color:blue;">|</mark>**Finding informer**<mark style="color:blue;">|</mark> specifies the person (by role) or other entity (e.g. a monitoring device) from which the clinical finding information was obtained. This attribute is frequently used in conjunction with <mark style="color:blue;">|</mark>finding method<mark style="color:blue;">|</mark>.

#### Attributes Used to Define Procedure Concepts

Below is a list of some of the attributes used to define |procedure| concepts, and a brief description of their meaning:

<mark style="color:blue;">|</mark>**Procedure site**<mark style="color:blue;">|</mark> describes the body site acted on or affected by a procedure.

<mark style="color:blue;">|</mark>**Procedure morphology**<mark style="color:blue;">|</mark> specifies the morphology or abnormal structure involved in a procedure.

<mark style="color:blue;">|</mark>**Method**<mark style="color:blue;">|</mark> represents the action being performed to accomplish the procedure. It does not include the surgical approach, equipment or physical forces.

<mark style="color:blue;">|</mark>**Procedure device**<mark style="color:blue;">|</mark> describes the devices associated with a procedure.

<mark style="color:blue;">|</mark>**Access**<mark style="color:blue;">|</mark> describes the route used to access the site of the procedure.

<mark style="color:blue;">|</mark>**Direct substance**<mark style="color:blue;">|</mark> describes the <mark style="color:blue;">|</mark>substance<mark style="color:blue;">|</mark> or <mark style="color:blue;">|</mark>pharmaceutical / biologic product<mark style="color:blue;">|</mark> on which the procedure's method directly acts.

<mark style="color:blue;">|</mark>**Occurrence**<mark style="color:blue;">|</mark> refers to a specific period of life during which a procedure is undertaken.

<mark style="color:blue;">|</mark>**Priority**<mark style="color:blue;">|</mark> refers to the priority assigned to a procedure.

<mark style="color:blue;">|</mark>**Has focus**<mark style="color:blue;">|</mark> specifies the <mark style="color:blue;">|</mark>clinical finding<mark style="color:blue;">|</mark> or <mark style="color:blue;">|</mark>procedure<mark style="color:blue;">|</mark> which is the focus of a procedure.

<mark style="color:blue;">|</mark>**Has intent**<mark style="color:blue;">|</mark> specifies the intent of a procedure.

<mark style="color:blue;">|</mark>**Recipient category**<mark style="color:blue;">|</mark> specifies the type of individual or group upon which the action of the procedure is performed.

<mark style="color:blue;">|</mark>**Revision status**<mark style="color:blue;">|</mark> specifies whether a procedure is primary or a revision.

<mark style="color:blue;">|</mark>**Using substance**<mark style="color:blue;">|</mark> describes the substance used to execute the action of a procedure, but it is not the substance on which the procedure's method directly acts.

<mark style="color:blue;">|</mark>**Using energy**<mark style="color:blue;">|</mark> describes the energy used to execute an action.

#### All Attributes Values Used to Define SNOMED CT Concepts

For attribute values or range, please consult the Editorial Guide (refer to section on [Domain Specific Modeling](https://docs.snomed.org/snomed-ct-specifications/snomed-ct-editorial-guide/readme/authoring/domain-specific-modeling), then the appropriate Attributes Summary) or the [MRCM Browser](https://browser.ihtsdotools.org/mrcm).

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=Starter+Guide&#x26;entry.670899847=SNOMED%20CT%20Concept%20Model" class="button primary">Provide Feedback</a>
