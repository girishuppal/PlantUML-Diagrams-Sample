You can change colors and font of the drawing using the skinparam command.
skinparam is now deprecated and is being phased out.
Although it is still supported for simple cases and for backward compatibility, users should migrate to CSS style, which supports more complex styling scenarios.
〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
@startuml SKINPARAM
skinparameters
@enduml

〰️〰️〰️〰️SKINPARAM〰️〰️〰️〰️〰️〰️〰️〰️

@startuml THEME

skinparam backgroundColor transparent
'skinparam monochrome true
'skinparam monochrome reverse
skinparam defaultFontName Impact
skinparam Handwritten true


skinparam lifelineStrategy dotted

skinparam ArrowMessageAlignment centre
'skinparam ArrowFontName Verdana
skinparam ArrowFontSize 32
skinparam ArrowFontStyle bold
skinparam ArrowColor green
skinparam ArrowThickness 5

skinparam SequenceMessageAlignment right


Alice -> Bob : Hello
Bob --> Alice : Hi there
Alice -> Bob : Without color: <#0:sunglasses:>
Alice -> Bob : Change color: <#green:sunny:>
Bob -> Alice : Change color: <#red:sunny:>
Bob -[#red]> Alice : hello
@enduml


〰️〰️〰️〰️SKINPARAM〰️〰️〰️〰️〰️〰️〰️〰️
@startuml Note

skinparam lifelineStrategy solid
skinparam style strictuml

participant Glenn
hide unlinked

Girish -> George
George -> Gail
Gail --> Girish
Gail --> Girish++
George --> Gail--

Girish ->(120) Gail: This is slanted

@enduml

〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
