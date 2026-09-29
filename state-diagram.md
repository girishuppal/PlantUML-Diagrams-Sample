State diagrams provide a visual representation of the various states a system or an object can be in, as well as the transitions between those states. They are essential in modeling the dynamic behavior of systems, capturing how they respond to different events over time. State diagrams depict the system's life cycle, making it easier to understand, design, and optimize its behavior.

〰️〰️〰️〰️STATE DIAGRAM〰️〰️〰️〰️〰️〰️〰️〰️
@startuml AAA State Diagram

title "AAA State Diagram"
skin rose

footer "Created by Girish Uppal"


state st <<start>>
state en <<end>>

state "Agent Management" as Agent
st -> Agent
Agent -> en
state Agent{
    state conc as "Agent Created"
    state coni as "Invited"
    state conp as "Portal Ready"
}
conc -> coni
coni -> conp
conp -[dotted]----> conc : "If Agent access disabled"


state "Document Management" as RM
state RM{

    state rg as "Document Generated"
    state rv as "Document Validated"
    state ro as "Document Orgnanised"
    state rp as "Document Permission set"
    state ru as "Document Uploaded"
    state rd as "Document Downloaded"
}



rg -> rv
rv -> ro
ro -> rp
rp -> ru
ru -> rd

@enduml

〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
