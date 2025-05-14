# SNOMED CT Starter Guide : 7. SNOMED CT Expressions

This section provides an overview of:

  * Precoordinated Expressions
  * Postcoordinated Expressions

## Why is this important?

SNOMED CT provides a mechanism that enables clinical phrases to be represented, even when a single SNOMED CT concept does not capture the required level of detail. This is important as it enables a wide range of clinical meanings to be captured in a record, without requiring the terminology to include a separate concept for every detailed combination of ideas that may potentially need to be recorded. Application software that supports the use of SNOMED CT expressions enables detailed clinical information to be recorded, retrieved and analyzed.

## What is this?

Clinical expressions using SNOMED CT concepts can be of two types: precoordinated expressions, which use a single SNOMED CT concept identifier; and postcoordinated expressions, which contain more than one SNOMED CT identifier.

SNOMED CT support of the postcoordination technique allows additional clinical detail to be represented if required. For example, |pneumococcal pneumonia| has a |finding site| of |lung structure|, which can be refined to |upper lobe of right lung|.

Postcoordination greatly increases the depth of detail that SNOMED CT can represent without having to include every possible specific site for every possible disorder via a concept. For example, the concept |bacterial pneumonia| has a defining relationship specifying its |causative agent| as |bacteria| and this can be refined to |streptococcus pneumoniae|.

SNOMED CT expressions are a structured combination of one or more concept identifiers used to represent a clinical idea in a logical manner, which is automatically processable. Expressions are represented using the SNOMED CT compositional grammar, which is a lightweight syntax for the representation of SNOMED CT expressions.

The logic on which the SNOMED CT concept model is based allows alternative representations of the same or similar information to be recognized and compared. For example, |pneumococcal pneumonia| refined by |finding site| |upper lobe of right lung| can be computed to have the same meaning as |right upper lobe pneumonia| refined by |causative agent| |streptococcus pneumoniae| and addition of |pathological process| |infectious process|.

### Precoordinated Expressions

Precoordinated expressions are expressions that represent the meaning of individual concepts which are predefined in SNOMED CT. Besides the unique concept identifier and descriptions, each concept also has a formal logic definition represented by a set of defining relationships to other concepts. The figure below shows the precoordinated expression used to record |fracture of tibia|. It illustrates that this can be represented by a single identifier, with or without an accompanying human-readable term. It also illustrates the defining relationships of the concept identified in the expression. This is the precoordinated definitional knowledge which is conveyed by this expression.

Precoordinated expression representing fracture of tibia  
| Identifier only| 31978002  
---|---|---  
With display term| 31978002 |fracture of tibia|  
Graphic view of the defining relationships of the concept |fracture of tibia|| <img src="images/26837128.png" alt="" title="" width="350" height="">  
  

The second example shown below illustrates the fact that some SNOMED CT concepts provide quite a lot of detailed refinement, some of which might otherwise be captured separately. We will return to this example when considering postcoordination.

**Example: Precoordinated representation of "Laparoscopic emergency appendectomy"**  
SNOMED CT contains the concept 174041007 |laparoscopic emergency appendectomy|. The identifier of this concept (174041007) can be used (with or without the associated term) as a precoordinated expression to record an instance of this procedure.   
The procedure 'laparoscopic emergency appendectomy' has at least three distinct facets: 'excision of appendix', 'using a laparoscope' as 'emergency procedure'. The [SNOMED CT](https://confluence.ihtsdotools.org/display/DOCGLOSS/SNOMED+CT "Glossary link: SNOMED CT") [concept](https://confluence.ihtsdotools.org/display/DOCGLOSS/concept "Glossary link: concept") 174041007 |laparoscopic emergency appendectomy| precoordinates these facets as its definition includes the following defining relationships:

  * 116680003 |is a| = 80146002| appendectomy|
  * 260870009 |priority| = 25876001 |emergency|
  * 425391005 |using access device| = 86174004 |laparoscope|

  
  
### Postcoordinated Expressions

Expressions that contain two or more concept identifiers are referred to as postcoordinated expressions. Postcoordination combines concepts and allows more detail to be added to the meaning represented by a single concept. A postcoordinated expression is not just a list of concept identifiers, it follows a set of rules that mimic the way attributes and values are used to define SNOMED CT concepts.

**Example: Postcoordinated representation of "Laparoscopic emergency appendectomy"**  
Although SNOMED CT contains the concept |laparoscopic emergency appendectomy|, it is also possible to represent this clinical phrase using the following postcoordinated expression.

  * 80146002 |appendectomy| :260870009 |priority| = 25876001 |emergency|, 425391005 |using access device| = 86174004 |laparoscope|  
  
This postcoordinated expression has exactly the same meaning as the precoordinated expression
  * 174041007 |laparoscopic emergency appendectomy|  
  
The fact that the two expressions have the same meaning can be computed because
  * 174041007 |laparoscopic emergency appendectomy| is a fully-defined subtype descendant of 80146002 |appendectomy| ; and
  * the only differences between the defining attributes of these concepts are the addition of   

    * 260870009 |priority| = 25876001 |emergency|
    * 425391005 |using access device| = 86174004 |laparoscope|

  
  
The example above shows that postcoordination can be applied even when a single concept is available to represent the required meaning. However, the real strength of postcoordination is that it allows a clinical phrase to be represented even when the precise concept is not present in SNOMED CT. In these cases, postcoordinated refinements can be applied to an existing concept to more precisely capture the required meaning.

**Example: Postcoordinated representation of "Laparoscopic removal of device from abdomen"**  
SNOMED CT does not contain a concept that represents this clinical idea. However, it is possible to represent it using the following postcoordinated expression.   
68526006 |removal of device from abdomen| : 425391005| using access device| = 6174004 |laparoscope|  
---  
  
Postcoordinated expressions may be created at run-time by selection of individual facets of a concept. For example, to indicate the nature and location of a fracture for a particular bone and, where relevant, whether the bone affected is on the right or left. Some applications allow generation of postcoordinated expression using natural language processing. Alternatively, postcoordinated expression can be selected during user interface design and bound to simple data entry options. In these cases, the user may not be aware that the information is being captured in a postcoordinated form.

#### Representing Postcoordination

There are several valid ways to represent and store postcoordinated expressions. However, to support interoperability, SNOMED International has specified a standard SNOMED CT compositional grammar form that is both human-readable and computer processable. The examples of expression that you see in this guide use this grammar.

**The basics of SNOMED CT compositional grammar**

  * At its simplest level a single SNOMED CT concept identifier is a valid expression.   

    * 80146002
  * A concept identifier can optionally be followed by a term associated with that concept enclosed between two pipe characters   

    * 80146002 **|** appendectomy**|**
  * A concept identifier (with or without a following term) can be followed by a refinement. The refinement follows a colon   

    * 80146002 |appendectomy| **:**_< refinement>_
  * A refinement consists of a sequence of one or more attribute-value pairs. Both the attribute and the value are represented by a concept identifier (with or without a following term). The attribute is separated from the value by an equals sign   

    * 80146002 |appendectomy| **:** 260870009 |priority| **=** 25876001 |emergency|
  * If there is more than one attribute-value pair, the pairs are separated by commas   

    * 80146002 |appendectomy| : 260870009 |priority| = 25876001 |emergency|**,** 425391005 |using access device| = 86174004 |laparoscope|
  * Curly braces represent grouping of attributes within a refinement, for example to indicate that the method applies to a specific site   

    * 80146002 |appendectomy| : **{** 260686004 |method| = 129304002 |excision - action|, 405813007 |procedure site - direct| = 181255000 |entire appendix| **}**
  * Round brackets represent nesting to allow the value of an attribute to be refined   

    * 161615003 |history of surgery| : 363589002 |associated procedure| = **(** 80146002 |appendectomy| : 260870009 |priority| = 25876001| emergency| **)**

  
  
#### Postcoordination and the Concept Model

The refinements used in postcoordinated expressions should follow the same concept model rules that are applied when concepts are defined. Attributes should only be applied to concepts that are in the specified 'domain' for that attribute. The values applied to attributes should be limited to the specified 'range' for that attribute. These rules may sometimes seem to limit flexibility but these rules are important, because if they are followed, it is possible to compute similarities and subtype relationships between different expressions. This ability to compute subtypes is the key to effective meaning-based retrieval of postcoordinated expressions.

**Example: Postcoordination and concept model rules**  
A disease with a particular morphological abnormality at a particular site is represented in the following way:

  * 64572001 |_disease_ | : { 363698007 |finding site| = 91723000 |_anatomical structure_ |, 116676008 |associated morphology| = 49755003 |_morphologically abnormal structure_ | }  
  
It must **not** be represented in other ways that conflict with concept model rules such as:
  * 49755003| _morphologically abnormal structure_ | : 363698007 |finding site| = 91723000 |_anatomical structure_ |
  * 64572001 |_disease_ | : 363698007 |finding site| = ( 91723000| _anatomical structure_ | : 116676008 |associated morphology| = 49755003 |_morphologically abnormal structure_ | )
  * 64572001 |_disease_ | : 116676008| associated morphology|=(49755003 |_morphologically abnormal structure_ | : 363698007 |finding site| = 91723000 |_anatomical structure_ | )

  
  

In some cases, postcoordination may be simply a matter of choosing one of the subtypes of a defining attribute value. For example the definition of |total hip replacement| includes the attribute |direct device| with the value |total hip replacement prosthesis|. The subtypes of this value include different types of prosthesis, some of which are shown in the graphical view of the concept definition below. One of these more specific values can be selected to specify the type of prosthesis actually used.

  

<img src="images/26837129.png" alt="" title="" width="602" height="383">

In the same way clinical situations, such as family history, can be recorded for any disorder and are not limited to a predefined set of conditions.

**Example: Postcoordination of family history**  
The definition includes 246090004 |associated finding| = 246090004 |disease|. This value can be refined to refer to a particular disease. For example:

  * 281666001 |family history of disorder| : 246090004 |associated finding| = 22298006 |myocardial infarction|  
  
The definition of |family history of disorder| specifies that the |subject relationship context| is |person in the family|. This value indicates that the finding applies to a family member rather than the patient and can be refined to refer to a particular family member. For example:
  * 281666001 |family history of disorder| : { 246090004 |associated finding| = 22298006| myocardial infarction|, 408732007 |subject relationship context| = 66839005 |father| }

  
  
## Consistent Retrieval of Precoordinated and Postcoordinated Expressions

SNOMED CT expressions support consistent and comparable representation of meaning using both precoordinated and postcoordinated expressions. This facilitates retrieval of all instances of expressions that match a set of criteria specified using the subtype hierarchy and other defining relationships.

**Example: Laparoscopic procedures**  
Several earlier examples in this chapter have represented procedures. If there was a requirement to retrieve all laparoscopic procedures the first step would be to establish the criteria for inclusion. The requirement could be expressed as follows.

  * 51316009 |laparoscopic procedure| and all its subtypes   
  
In some cases, it is simply a question of looking at the subtype hierarchy.   
For example
  * 174041007 |laparoscopic emergency appendectomy| is the source of a sequence of |is a| relationships which lead to 51316009 |laparoscopic procedure|.   
  
In other cases, it is necessary to look at the definition of |laparoscopic procedure| and compare this with the equivalent expression. |laparoscopic procedure| is fully-defined as follows.
  * 71388002 |procedure| : 425391005 |using access device| = 86174004 |laparoscope|  
  
Therefore, queries looking for instances of laparoscopic procedures should also retrieve postcoordinated expressions in which both of the following are true:
  * The focus concept is a subtype of 71388002 |procedure|
  * The attribute 425391005 |using access device| is present with the value 86174004 |laparoscope| or a subtype of that concept.   
  
This rule would include postcoordinated representations, such as the following expression, for which there is no existing SNOMED CT concept:
  * 68526006 |removal of device from abdomen| : 425391005 |using access device| = 6174004 |laparoscope|

  
  
The following graphics illustrate the ways in which query predicates based on SNOMED CT concept definitions can be used to retrieve data based on different criteria. In each case, the data retrieved includes expressions that either have attributes matching the criteria or refer to a concept with defining relationships that match the query criteria.

|  <img src="images/29952965.png" alt="" title="" width="" height="">  
---  
  
__Example: Result of retrieving concepts with_  _|__associated morphology_ _|_  _specified as_  _|__benign neoplasm_ _|__

__  
__

|  <img src="images/29952967.png" alt="" title="" width="" height="">  
---  
  
__Example: Result of retrieving concepts with_  _|__finding site_ _|_  _specified as_  _|__kidney_ _|__
