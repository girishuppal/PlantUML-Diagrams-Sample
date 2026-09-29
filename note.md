〰️〰️〰️〰️〰️NOTE〰️〰️〰️〰️〰️〰️〰️
@startuml Note

skinparam lifelineStrategy solid

Alice -> Bob
Bob -> Jim
Jim -> John
John --> Alice
Jim -> Jim : Thinking

note over John : Hi
note over Bob, John: Bob & John
note over Alice #FFCCEE: Alice Red

note left of Alice: Lefty
note right of John: Righty

note across : Bobby

hnote over Alice : Hexa
rnote over Jim : Recta

hnote over John
- This is 
- a big note
endnote

@enduml

〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
