This is an open shared notes document for the HydraConnect 2016 Data
Modeling 101 Workshop. Please feel free to add to, share, reuse, or
comment on as helpful. Thanks!

Shared Workshop Notes
=====================

Workshop Introduction (9-9:15)
------------------------------

Goals from the audience:

-   Getting inside Christina’s brain

-   Communicating about what we are trying to achieve

    -   Communication between service managers and programmers

-   Common workflows, standards

-   How modeling impacts developers

-   Applying data modeling techniques in other places (like archival
    > systems), not just Hydra

-   Data model once, before ingest, not after (getting it right)

Intro to Data Models: How Models Work with Systems (9:15-10:15)
---------------------------------------------------------------

Intro to Data Models: Expressing Models (10:30-10:45)
-----------------------------------------------------

Breakout groups: Examples Introduction & Setup (10:45-11)
---------------------------------------------------------

Breakout groups: Data Modeling Breakouts (11-11:45)
---------------------------------------------------

### PCDM

### IIIF 

### DPLA/EDM

Breakout groups: Breakout Recaps (Noon-12:15)
---------------------------------------------

Wrap-up & Going Forward (12:15-12:30)
-------------------------------------

Shared Workshop Preparation/Reading Notes
=========================================

[*Conceptual Modeling of Information Systems*](http://infocat.ucpel.tche.br/disc/mc/cmis.pdf): Chapter 1, Chapter sections 2.1, 3.1
-----------------------------------------------------------------------------------------------------------------------------------

-   Preface:

    -   Not possible to have concrete knowledge about a domain without a
        > prior general knowledge about that domain.

    -   Concrete knowledge requires prior general knowledge, which is
        > independent of the concrete objects and relationships existing
        > at any point in time.

    -   General knowledge also includes rules that must be obeyed,
        > definitions that allow new knowledge to be obtained from
        > existing knowledge, and details of the actions that the users
        > want the system to perform when a condition is satisfied.

    -   In the Information Systems field, the name **conceptual
        > modeling** is the name for the activity that elicits and
        > describes the general knowledge that a particular
        > \`information system needs to know. The main objective is to
        > obtain that description, which is called a **Conceptual
        > schema**. Conceptual schemas are written in languages called
        > **Conceptual modeling languages**.

    -   Conceptual modeling is an important part of requirements
        > engineering, the first and most important phase in the
        > development of an information system.

-   Chapter 1: Introduction

    -   1.1: Functions of an Information System

        -   Difficult to define an information system precisely. Part of
            > the difficulty comes from fact that information systems
            > can be analyzed from at least 3 different perspectives:

            -   Contribution they make;

                -   Issue with this: it does not clearly establish what
                    > an information system actually is. The wider
                    > system of which an information system is part of
                    > may also require means other than information
                    > systems to achieve objectives. Also, there are
                    > other instruments that can provide similar
                    > contributions w/o actually being
                    > information systems.

            -   Structure and behavior;

                -   Pro of defining information systems from their
                    > structure and behavior: emphasize the structure
                    > and behavior of the physical and abstract elements
                    > that make up an information system.

            -   Functions they perform.

                -   For Conceptual Modeling, defining information
                    > systems based off of the functions they perform is
                    > most useful, as they define what information
                    > systems do without considering why and how they
                    > do it.

        -   **Domain (aka Object System ; Universe of Discourse)**: the
            > usual constraint on the kind of information handled by an
            > information system is that it must refer to the state of a
            > certain domain. The nature of the domain doesn’t influence
            > the definition of an information system.

        -   **Information System**: is a designed system that collects,
            > stores, processes, and distributes information about the
            > state of a domain. These systems have 3 main functions:

            -   Memory: maintain representation of state of a domain ;

                -   Maintains internal representation of the state of a
                    > domain ;

                -   Can be performed on request or autonomously.

            -   Informative: provide information about state of a domain
                > ;

                -   Provides users with information about the state of a
                    > domain ;

                -   Can have extensional or intensional queries ;

                -   Informative functions can be performed on request or
                    > autonomously ;

                -   Informative functions do not change the state of
                    > the domain.

            -   Active: perform actions that change state of a domain .

                -   Performs actions that modify the state of a domain ;

                -   Needs to know what actions the information system
                    > can take, when they can be taken, and how it will
                    > affect the state of the domain ;

                -   can be performed on request or autonomously ;

    -   1.2: Conceptual Modeling

        -   Line of reasoning for conceptual modeling aspects in this
            > text:

            -   For a memory function of an information system to
                > maintain a representation of the state of a domain, we
                > must define the particular state that must be
                > represented ;

            -   State of domains changes over time, so potential changes
                > must be defined ;

            -   Representation of the state in the information system
                > must be consistent. So must define when a
                > representation is consistent ;

            -   Answering queries often requires inference capability by
                > the information system. This requires defining
                > derivation rules.

        -   Objective of memory function of an information system is to
            > maintain a representation of the state of its domain.

            -   State of a domain consists of a set of
                > relevant properties.

            -   Relevant properties depend on information system
                > objectives and on the anticipated contribution of the
                > information system.

        -   In Information Systems field, make fundamental assumption
            > that domain consists of number of objects and
            > relationships between them, which are **classified** into
            > **concepts**.

            -   State of a particular domain, at a given time, therefore
                > consists of a set of objects, set of relationships,
                > and set of concepts into which objects and
                > relationships are classified.

            -   When we assume that a domain consists of objects,
                > relationships, concepts, we commit ourselves to a
                > specific way of viewing domains. This commitment is
                > called **ontological commitment**. In the field of
                > information systems, this commitment to viewing
                > domains in a particular way is called the **Conceptual
                > model**.

        -   The set of concepts used in a particular domain constitutes
            > a **conceptualization** of that domain. The specification
            > of this conceptualization is sometimes called an
            > **ontology** of the domain.

            -   Note that the term **ontology** is used to denote 2
                > different ideas: a branch of philosophy, and a
                > specification of a conceptualization. In computer
                > science, the latter is the usual meaning.

        -   The formal basis of **conceptual modeling languages** (the
            > languages in which conceptual schemas, or ontologies,
            > are written) is logic.

            -   In many projects, the use of logical languages is
                > impractical, and specialized languages are
                > more suitable. One such language is the Unified
                > Modeling Languages (UML).

        -   Distinction between a **concept** and an **object**:

            -   **Concept** is something that we have formed in our mind
                > through generalization from certain instances.

            -   **Classification** is the operation that associates an
                > object with a concept. **Instantiation** gives an
                > instance of a concept (is the inverse
                > of Classification).

            -   The set of objects that constitutes an instance of a
                > concept at a given time is known as the **Population**
                > of the concept at that time.

            -   An **Entity type** is a concept whose instances are
                > individual, identifiable objects.

            -   Objects that are instances of an entity type are called
                > **Entities**.

            -   **Relationship types** are concepts whose instances
                > are relationships.

        -   The set of entity and relationship types used to observe the
            > state of a domain is the **conceptualization of that
            > state**. The description of that conceptualization, as
            > well as other elements that will be mentioned below, is
            > sometimes referred to as the **ontology of the state**,
            > the **conceptual schema of the state**, or simply the
            > **structural schema**. The set formed by the structural
            > schema and the behavioral schema is called the
            > **conceptual schema**.

        -   Not all entities and relationships in a domain need to be
            > represented in an information system. This leads us to the
            > distinction between the **conceptual schema of a domain**
            > and the **conceptual schema of an information system**.
            > The former describes the conceptualization of the domain,
            > which applies irrespective of which entities and
            > relationships will be represented in the
            > information system.

        -   **Information base** is a representation of the entities and
            > relationships of a domain, and their classification into
            > entity and relationship types.

        -   Book uses three distinct terms (conceptual model, conceptual
            > schema, information base) to distinguish three
            > different concepts. The same distinction is well
            > established in the field of databases: there are data
            > models (e.g. relational data models), database schemas
            > (written in a particular data model), and databases, or
            > instances of database schemas.

        -   **Behavioral schema** specifics the valid changes in the
            > domain state, as well as the actions that the system
            > can perform.

        -   **Structural event**: elementary change in the population of
            > an entity or relationship type. In First Order Logic
            > language, there are only 2 kinds of structural event:
            > insertion and removal of facts.

        -   **Domain event**: is a state change consisting of a set of
            > one or more structural events that are perceived as a
            > valid change in the domain. The concept of a domain event
            > is akin to that of a transaction in the field of
            > database systems.

        -   Information systems perform **actions**. The effect of an
            > action is a change in the information base and/or the
            > communication of a certain piece of information or command
            > to one or more recipients. An **action request event** (or
            > simply an action request) is a request to the information
            > system to perform an action.

        -   **Domain event notification** is an external action request
            > whose only effect is a change in the information base that
            > corresponds exactly to a single domain event.

        -   Events, either domain or action requests, are also instances
            > of concepts. An **event type**, then, is a concept whose
            > instances are events. Events have characteristics, which
            > are relationships to other entities. In particular, all
            > events have a relationship with an entity that is a
            > time instance.

        -   The system must know the types of possible domain event.
            > This is general knowledge about the domain.

        -   An information base is **valid** if the facts it contains
            > are true, and is **complete** if it contains all
            > relevant facts.

            -   Validity and completeness are the two components of the
                > integrity of an information base. We say that an
                > information base has **integrity** when all its facts
                > are valid and it contains all relevant facts.

            -   We can establish conditions for the information base
                > such that, if they are satisfied, we may be reasonably
                > confident of its integrity. These conditions are
                > called **integrity constraints**, and are defined in
                > the conceptual schema.

            -   An information base is **consistent** if it satisfies
                > all the integrity constraints defined. A constraint is
                > **violated** when it is not satisfied by the
                > information base.

            -   The set of integrity constraints defined in a conceptual
                > schema must be **consistent** (or **satisfiable**).
                > This means there must be at least one state of the
                > information base that satisfies these constraints. We
                > require that the set of constraints defined in a
                > conceptual schema must be **strongly** satisfiable,
                > that is, satisfiable in finite, nonempty
                > information bases.

        -   Most systems have certain inference capability. This
            > capability requires two main components: **derivation
            > rules** and an **inference mechanism**.

            -   The way in which the inference mechanism works may vary
                > from one information system to another; it is
                > considered to be part of the internal structure of the
                > system and is therefore not specified in the
                > conceptual schema.

            -   A **derivation rule** is an expression that defines how
                > new facts can be inferred from others.

            -   The conceptual schema must include all the derivation
                > rules that can be used in a particular system, but we
                > should explicitly define only those that are specific
                > to our domain.

        -   Every information system embodies a conceptual schema.

    -   1.3: Abstract Architecture of an Information System

        -   The term architecture is used to refer to the main software
            > components and their relationships. In principle, there
            > are several possible architectures for a given system, and
            > choosing the most suitable one for ap articular system
            > depends on several factors.

        -   An **external schema** is a form of representation of the
            > state of the domain, and an **external database** is a
            > virtual representation of the state of the domain in this
            > external schema. In addition to a form of representation,
            > external schemas also include aspects of the manipulation
            > of this form, such as the language used to ask queries or
            > to communicate events.

        -   The system must deal with several external schemas. To do
            > so, the system needs to know the meaning of the
            > representations used and the meaning of the
            > alterations permitted.

        -   The **external processor** is the architectural component
            > that interacts with users. In theory, there is an external
            > processor for each external schema.

        -   The **information processor** is the component that handles
            > the messages sent by the users and performs any active
            > function that may be delegated to the system.

        -   When the information processor asks itself questions such as
            > ‘is the board square in Column 2, Row3 free?’ (for the
            > Chess game example), it behaves as if the information base
            > really existed, when in reality the question will be sent
            > to the internal processor, which will then answer it using
            > the physical database.

        -   The **internal schema** is the form used internally by the
            > system to represent the state of the domain, and the
            > **internal database** is the representation of the state
            > in that schema. Only the internal database
            > exists physically. The internal schema also comprises the
            > set of operations that may be invoked on the database.

        -   In order to perform its task, the internal processor needs
            > to know the internal schema, including its correspondence
            > with the conceptual schema.

        -   Modern architectures of information systems are designed
            > with three logical layers: presentation, domain, and
            > data management.

            -   The equivalent of the external processor is located in
                > the presentation layer;

            -   The equivalent of the information processor is located
                > in the domain layer;

            -   and the equivalent of the internal processor is located
                > in the data management layer.

    -   1.4: Requirements Engineering

        -   **Conceptual schemas** are the common base of external and
            > internal schemas and their processors. Therefore, it is
            > clearly not possible to design the architecture of an
            > information system without a conceptual schema.

        -   The stage that precedes system design is called
            > **requirements engineering**.

        -   During **requirements elicitation**, the future users and
            > the designers of the system analyze their particular
            > problems and needs and the characteristics of the domain.

        -   During this process, a conceptual schema of the existing
            > and/or desired domain may be created if this is considered
            > necessary to achieve a common understanding of
            > the domain(s).

        -   In the **requirements specification process**, the
            > functional and nonfunctional requirements of the new
            > system are defined.

            -   The result is a set of documents (called
                > **specifications**) that precisely describe the system
                > that the users require and that the designers have to
                > design and build.

            -   **Functional requirements** describe what the system
                > must do, while **nonfunctional requirements** describe
                > the global properties of the system, such as response
                > time or portability.

            -   The conceptual schema of an information system is the
                > specification of its functional requirements.

        -   During **requirements validation**, the specifications are
            > checked to ensure that they meet user requirements.

            -   Validation can be performed in several
                > nonexclusive ways. 2 of the best known ways:

                -   To present the conceptual schema (and the
                    > system specification) in a language and form that
                    > are easily understood by users.

                -   To build (partial) prototypes of the system.

    -   1.5: Quality of Conceptual Schemas

        -   The **quality** of a conceptual schema is the degree to
            > which defined, relevant properties are present.

            -   All relevant general static and dynamic aspects of the
                > universe of discourse should be described in the
                > conceptual schema. The information system cannot be
                > held responsible for not meeting those described
                > elsewhere, including in particular those in
                > application programs.

            -   Conceptual schema is the definition of the general
                > domain knowledge that the information system needs to
                > perform its functions; therefore, the conceptual
                > schema must include all the required knowledge.

        -   A conceptual schema is **correct** if the knowledge it
            > defines is true for the domain and relevant to the
            > functions that the system must perform.

        -   Conceptual schemas are described in a particular conceptual
            > modeling language. This language will have a set of rules
            > that must be respected. A conceptual schema is
            > **syntactically correct** if it respects all the rules of
            > the language in which it is written.

        -   Conceptual schemas should be understandable to its relevant
            > audience, and simple schemas are to be preferred - that
            > is - schemas that use fewer language constructs or fewer
            > complex constructs. Simplicity is related
            > to understandability.

        -   **Principle of conceptualization**: a conceptual model
            > should only include conceptually relevant aspects, both
            > static and dynamic, of the universe of discourse, thus
            > excluding all aspects of (external or internal) data
            > representation , physical data organization and access as
            > well as aspects of particular external user representation
            > such as message formats, data structures, etc.

        -   **Stability**: also referred to as flexibility,
            > extensibility, or modifiability. A conceptual schema is
            > tsable if minor changes in the properties of the domain or
            > in the users’ requirements do not entail major changes in
            > the schema.

    -   1.6: A Brief History of Conceptual Modeling

        -   Of particular interest is the mentions of Conceptual
            > Modeling overlapping with Semantic Modeling + Object
            > Oriented modeling/design.

-   Chapter 2: Entity Types

    -   Determining the entity types that exist in a given domain and
        > are relevant to an information system is a fundamental task in
        > conceptual modeling.

    -   2.1: Introduction

        -   **Classification** is an activity that we can perform
            > efficiently and that we need in order to structure our
            > perceptions of the world and our knowledge about it.
            > Classification is fundamental for information systems,
            > which, among other things, maintain a representation of
            > the state of a domain.

            -   Classification operation consistent in determining
                > whether or not the object is an instance of
                > the concept.

        -   Classical theory of concepts states that concepts, called
            > **definitional concepts**, are set of properties that we
            > humans are able to observe in objects. This set of
            > properties is called the **intension** of the concept.

            -   According to the classical theory, an object is an
                > instance of a concept if it has all the properties of
                > that concepts. Therefore, the classification operation
                > consists in checking that the properties of the object
                > include the properties of the concepts.

            -   For this reason, the properties of a concept are
                > classified as defining or non-defining. The
                > **defining** properties are the necessary and
                > sufficient properties for an object to be considered
                > an instance of the concept. The **nondefining**
                > properties are redundant.

            -   An instance of a concept has all its properties
                > (defining and nondefining), but it may have other
                > specific properties…

            -   A concept is an abstraction of the properties of its
                > instances, and classification is an abstraction
                > operation, because it focuses only on some properties
                > of the objects and ignores all the others.

        -   Classification serves several basic functions in our mental
            > life, the most important ones being: cognitive economy and
            > inference ability.

            -   Classification provides cognitive economy because it
                > allows us to structure knowledge about objects into
                > two levels: concept and instance. At the concept
                > level, we find the properties (both defining
                > and nondefining) common to all instances of
                > the concept. At the instance level, we find only the
                > concept of which the object is an instance, and the
                > particular properties of that instance.

            -   Inference ability is related to the fact that not all
                > the properties of a concept need to be defining. There
                > may by many non-defining properties which can be
                > inferred without one needing to observe them directly.

        -   The difficulties inherent in the classical view have led
            > scientists to explore alternative theories that explain
            > concepts which are not strictly **definitional**. One of
            > these theories is based on a **probabilistic** view. In
            > this view, there is a probability that each property of a
            > concept will be present in the instances of that concept.

            -   In this approach the membership of an object in a
                > concept will be more or less likely and not absolute
                > as it was in the definitional view.

            -   A probabilistic concept may be represented by
                > a prototype. A **prototype** is a set of clearly
                > perceivable properties that some instances of the
                > concept, but not all of them, have. A concept
                > represented by a prototype is called a
                > **prototypical** concept.

            -   Many of the properties of a prototype oare nondefining,
                > but they are very effective in classification terms.

        -   Both definitional and prototypical concepts are set of
            > properties that we should somehow store in our minds.
            > However, some researchers challenge this mental
            > association between a concept and a set of properties, and
            > they prefer a theory of concepts based on **exemplars**.

            -   A concept is a set of exemplars, which may include all
                > the known instances of that concept or only a subset
                > of them.

            -   In the exemplar view, the classification of an object
                > into a concept consists in comparing the object with
                > the exemplars of the concept and calculating the
                > degree of similarity of the object ot the exemplars.

-   Chapter 3: Relationship Types

    -   3.1: Definition

        -   There is a similarity between the operation of classifying
            > an object into an entity type and that of classifying a
            > relationship into a relationship type.

            -   However, a relationship is always a relationship
                > between objects.

        -   A **relationship type** is a concept whose instances at a
            > given time are distinct property-entity sets formed by a
            > number n of entities that are instances of their
            > corresponding entity types and are considered to have that
            > relationship in the domain at that time, playing the
            > respective roles of the property.

            -   Relationship types, firstly, are concepts.

            -   Secondly, the definition states that a relationship is a
                > set formed by exactly one pair roles to entity for
                > each of its n number of participants.

            -   Thirdly, the definition states that the instances of a
                > relationship type must be distinct sets.

            -   Finally, instances of relationship type R are sets of
                > entities that are considered to have the relationship
                > R in the domain at that time, playing their
                > respective roles.

        -   A relationship is **synchronous** if, for each of its
            > instances at time t, the entities participating in r are
            > instances of their respectives entity types at t;
            > otherwise, the relationship is **asynchronous**.

        -   The **degree** of a relationship type is the number of
            > participants in that type.

        -   The **pattern sequence** of a relationship type is a
            > declarative sentence in which there is a placeholder for
            > each participant. Pattern sentences help us to understand
            > the meaning of relationship types and may be implicit
            > or explicit.

            -   The derivation of implicit pattern sentences depends on
                > how roles are named. There are two approaches:
                > **noun-based** and **verb-based**.

        -   The information for how many entities can participate in a
            > relationship at the same time can be extracted from
            > **cardinality** constraints.

        -   Normally, relationships are conceived of as having at least
            > 2 participants. Almost all conceptual modeling languages
            > require that relationship types have a degree of at
            > least two.

            -   There can be **unary** relationship types. In languages
                > that do not allow unary relationship types, the
                > concepts can be modeled as new entity types.

                -   Another solution involves modeling a unary type as
                    > a binary.

                -   A third solution, we can have an enumeration of the
                    > unary types.

        -   **Population** of a relationship type R at time t is the set
            > of its instances that exist in the domain at t.

        -   A relationship type is **constant** with respect to a
            > participant if the instances of the relationship in which
            > an instance of a certain entity participates are the same
            > during the temporal interval in which the entities exist.

            -   A relationship type is constant if it is constant with
                > respect to all its participants.

        -   A relationship type is **permanent** with respect to a
            > participant if the instances of R in which an instance e
            > of Entity type participates never cease to exist during
            > the temporal interval in which entity instances exists.

            -   A relationship type is permanent if it is permanent with
                > respect to all its participants.

        -   A relationship **subsumes** a second relationship (or a
            > relationship is a subtype of a second relationship) if all
            > instances of the first relationship must also be instances
            > of the second relationship.

RDF(S) at high level
--------------------

-   [*RDF 1.1 Primer*](https://www.w3.org/TR/rdf11-primer/)

-   [*RDF Schema Spec*](https://www.w3.org/TR/rdf-schema/)

[*Ontology Design Patterns*](http://ontologydesignpatterns.org/wiki/Main_Page)
------------------------------------------------------------------------------
