# Modifications from openvalue/ovn

### In Relationship.js

Symmetric --> SymmetrichasRelationship

Status --> relationshipStatus

enum:["active","inactive","potential"]
in RelationshipStatusType Class
active, inactive, and potential are subclasses of RelationshipStatusType

### In RelationshipType.js

enum:["member","child","supporter","customer"] 
in RelationshipTypeName Class
member, child, supplier, and customer subclasses of RelationshipTypeName

### In Agent.js

anyOf:[{ reverse : "has",},{ reverse : "is" ,}]
--> hasRelated and isRelated

### In Location.js

Location --> location property and Location Class
==> Applied to Agent

### In Group.js

member --> groupMember
allOf : [{ $ref: "Agent", } => Group is a subClass of Agent

### In Person.js

memberOf --> memberOf
relationships => Person subClass of Agent

### In Role.js

broader --> broaderRole
narrower --> narrowerRole

### In Quantity.js

id:"Quantity" --> Quantity (Class)
unit --> quantity Unit (property)

### In Unit.js

id:"Unit" --> Unit (Class)
Kind --> unitKind (property)

### In Kind.js

id:"Kind" --> Kind (Class)
Kind --> kindGeneralization (property)

### From README.md

Economic Event --> Event

Event Type --> EventType

Commitment Type --> CommitmentType

Economic Interaction --> duality

Exchange Type --> Exchange Type

Process Type --> ProcessType

Resource Type --> ResourceType

Stock_Flow => from REA model (1,2)

participation => from REA model (1,2)

[1]: McCarthy, William E., The REA Accounting Model: A Generalized Framework for Accounting Systems in a Shared Data Environment, The accounting review, Vol. LVLL, No. 3, July 1982, http://www.msu.edu/user/mccarth4/McCarthy.pdf
[2]: Gailly, Frederik et. al, Development of a formal REA-ontology Representation, Ghent University, Hoverniersberg 24, 9000 Gent, http://ceur-ws.org/Vol-160/paper22.pdf

