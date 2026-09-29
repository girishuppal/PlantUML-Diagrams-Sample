A PlantUML sprite is a small, monochrome, text-encoded graphic element used to add icons or stylized symbols (like logos or user icons) directly into text-based diagrams. Defined using hexadecimal values, they can be scaled and colorized to enhance visual communication within sequence, deployment, or C4 models. 

〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
@startuml COLORS
colors
@enduml
〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
@startuml SPRITE
listsprite
@enduml
〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️

sprite $foo2 {
FFFFFFFFFFFFFFF
F0123456789ABCF
F0123456789ABCF
F0123456789ABCF
F0123456789ABCF
F0123456789ABCF
F0123456789ABCF
F0123456789ABCF
F0123456789ABCF
FFFFFFFFFFFFFFF
}

Alice -> Bob : Testing <$foo2>

Alice -> Bob : Testing <$foo2,scale=3,color=orange}>

〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️


