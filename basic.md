PLANT UML SCRIPT
------------------------
-------------------------------------------------------------------------
// Demo 1 (Basic and Loop)

@startuml ABCD
skin rose
title Girish Architecture Diagram 

actor User  
actor Customer

participant System
participant Webserver

User -> System: Initiate Process
System -> Database: **Query** Data

User -> System : Request Data
activate System
System --> User : Data Response
deactivate System


note right of System: This process handles user requests
note left of Database: Stores user information

-------------------

alt System.state isDisabled
System--> Webserver: Notify Disabled State
end alt

alt Webserver.load > 80%
Webserver --> Database: Send Load Alert
else
Webserver --> System: Normal Operation
end alt

loop for each item in list
    System -> API: Process Item
    API --> System: Return Processed Item
end loop
-------------------------------------------------------------------------
//  Demo 2 (CSS)

skinparam handwritten true
skinparam shadowing true
skinparam BackgroundColor transparent
skinparam sequenceArrowColor #ff5733ff
skinparam noteBackgroundColor #07e84aff
skinparam noteBorderColor #d50de7ff
skinparam noteFontColor #000000ff  
skinparam style strictuml
skinparam SequenceMessageAlignment center
-------------------------------------------------------------------------
// Demo 3 (Title - Header - Footer - Note)

title Sequence Diagram Alignment Example <size:40><&heart>

note left 
Click <&wifi> 
end note

note right of Girish
  Girish is thinking about the report.
end note

header Block Diagram Example
footer Generated %date("yyyy-MM-dd") by Girish Uppal

colors

listopeniconic
-------------------------------------------------------------------------

// Demo 4 (Block)

[AA] <<static lib>>
[BB] <<shared lib>>

node azure
node office365 <<shared node>>
database Production

skinparam node {
borderColor Green
backgroundColor Cyan
backgroundColor<<shared node>> Red
}
skinparam databaseBackgroundColor Yellow

abstract abstract
abstract class "abs"
annotation "anno"
circle "circ"
() oval

diamond "diam"
<> diamond_short

class "cls"
entity "ent"
exception "exc"

interface "intf"
metaclass "meta"
protocol "prot"
stereotype "stereotype"
struct struct
enum Enum
-------------------------------------------------------------------------

// Demo 5 JSON + YAML

@startjson GirishProfile
{
   "name":"Girish",
   "company":"SOCO",
   "skillset": ["Power Apps", "Power Automate", "Power BI", "Azure", "Dynamics 365" ],
   "location": {
       "city":"Brisbane",
       "country":"Australia"
   }
}
@endjson

@startyaml ccc
doe: "a deer, a female deer"
ray: "a drop of golden sun"
pi: 3.14159
xmas: true
french-hens: 3
calling-birds: 
	- huey
	- dewey
	- louie
	- fred
xmas-fifth-day: 
	calling-birds: four
	french-hens: 3
	golden-rings: 5
	partridges: 
		count: 1
		location: "a pear tree"
	turtle-doves: two
@endyaml
-------------------------------------------------------------------------
// Demo 6 - Mindmap and WBS

@startmindmap xxx
*[#Orange] Colors
**[#lightgreen] Green
**[#FFBBCC] Rose
**[#lightblue] Blue

* Debian
**[#Orange] Ubuntu
*** Linux Mint
***[#LightCoral] Kubuntu
*** Lubuntu
*** KDE Neon
** LMDE
** SolydXK
** SteamOS
** Raspbian with a very long name
*** <s>Raspmbc</s> => OSMC
*** <s>Raspyfi</s> => Volumio
@endmindmap

@startmindmap yyy
+ OS
++ Ubuntu
+++ Linux Mint
+++ Kubuntu
+++ Lubuntu
+++ KDE Neon
++ LMDE
++ SolydXK
++ SteamOS
++ Raspbian
-- Windows 95
-- Windows 98
-- Windows NT
--- Windows 8
--- Windows 10
@endmindmap

@startwbs wwww
+ New Job
++ Decide on Job Requirements
+++ Identity gaps
+++ Review JDs
++++ Sign-Up for courses
++++ Volunteer
++++ Reading
++- Checklist
+++- Responsibilities
+++- Location
++ CV Upload Done
+++ CV Updated
++++ Spelling & Grammar
++++ Check dates
---- Skills
+++ Recruitment sites chosen
@endwbs
-------------------------------------------------------------------------
// Demo 7 - Controls 
@startsalt cc
{
  Just plain text
  [This is my button]
  ()  Unchecked radio
  (X) Checked radio
  []  Unchecked box
  [X] Checked box
  "Enter text here   "
  ^This is a droplist^
}
@endsalt

-------------------------------------------------------------------------
// Demo 8 - GANTT
@startgantt rtrtr
title Project Schedule
caption Some Project Gantt Chart
Project Starts 2025-07-01
printscale daily
[Task 1] starts at 2025-07-01 and lasts 5 days
[SameTaskName] as [T1] lasts 27 days and is colored in pink
[SameTaskName2] as [T2] lasts 13 days and is colored in orange
[T1] -> [T2]
[T3] lasts 10 days
[T5] lasts 5 days and is colored in green
[T3] -> [T5]
[T3] is colored in orange

[Prototype design] requires 15 days
[Test prototype] requires 10 days
[Project Complete] happens 2025-07-11
[Project Complete] is colored in green

-- Testing Phase --
[Task A] lasts 10 days
[Task B] lasts 5 days
[Task C] lasts 7 days

[Task B] starts after [Task A]'s start
[Task C] starts after [Task A]'s end

!$SHORT_DURATION = 15
[$PLANNING_TASK] lasts $SHORT_DURATION days
[$PLANNING_TASK] -> [SameTaskName2]



@endgantt
