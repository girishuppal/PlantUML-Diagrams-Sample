〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
@startgantt GANTT
title XXX Schedule
footer "Created by Girish Uppal"

<style>

ganttDiagram{
    task{
        FontName Verdana
        FontSize 14        
    }
    arrow{
        LineColor brown
    }
    timeline {
        FontName Verdana
        BackgroundColor lightblue
        FontSize 7    
    }
    Separator{
        LineColor grey
        Margin 5
        Padding 20
    }
}


</style>

skin rose
hide footbox
' hide topbox

' Scaling
' printscale weekly
'ganttscale weekly
projectscale daily


' Holidays
saturday are closed
sunday are closed
2026-1-26 is colored in LightSeaGreen
2026-4-3 is  colored in LightSeaGreen
2026-4-6 is  colored in LightSeaGreen
2026-4-25 is  colored in LightSeaGreen



'Estimates
Project starts 2026-1-5
--

[POC] as [P] requires 8 days 
note bottom
# Evaluate ABC option
# Evaluate Data Storage
# Evaluate Data processing
endnote
[Discovery] as [Dis] requires 5 days

-- PRE SALES --
[Solution Design] as [SD] requires 7 days
[Design-Endorse] as [E] requires 1 week

-- IMPLEMENTATION --
[Development] as [Dev] requires 8 weeks

note bottom
# Require design to be signed off
# YYY to provide details
endnote

[Contact Setup] as [CM] requires 2 days
[Users Invited to App] as [U] requires 7 days
[EDR Report Ready] as [PMS] requires 4 days
[UAT environment Setup] as [UATE] requires 5 days
[UAT by XYZ] as [UAT] requires 5 days
[Production environment Setup] as [PRODE] requires 5 days
[Bug Fixes] as [BF] requires 5 days

' Separator just at [SD]'s end
'[Dev] on {Girish:50%} requires 4 weeks

' Dependency
[POC] -> [SD]
[Dis] -> [SD]
[SD] -> [Dev]
[Dev] --> [UATE]
[UATE] --> [UAT]
[UAT] --> [PRODE]
[PRODE] --> [BF]
[BF] --> [PMS]

' % Completion
[P] is 30% completed
[Dis] is 40% completed
[SD] is 0% completed
[Dev] is 0% completed
[UATE] is 0% completed
[UAT] is 0% completed
[PRODE] is 0% completed
[PMS] is 0% completed
[BF] is 0% completed

' Start Date
[POC] starts at 2026-1-12
[SD] starts at 2026-1-22
[E] starts at 2026-2-5
[CM] starts at 2026-4-9
[PMS] starts at 2026-4-24
[Dev] starts at 2026-2-3
[Dis] starts at 2026-1-13

' Colors
[P] is colored in OrangeRed
[Dis] is colored in Gold
[SD] is colored in YellowGreen
[E] is colored in DarkSalmon
[Dev] is colored in Darkorange
[UAT] is colored in Darkorange
[UATE] is colored in Darkorange
[PRODE] is colored in Darkorange
[BF] is colored in Darkorange
[Dev] is colored in Darkorange
[CM] is colored in DarkGoldenRod
[Go Live] is colored in Green
[U] is colored in DarkOrchid
[PMS] is colored in SpringGreen

' Milestones
[Go Live] happens at 2026-4-30
[U] happens at 2026-4-23
[E] happens at 2026-2-5
[CM] happens at 2026-4-9
[XDE: Test Data Receive] happens at 2026-3-17
[YDE: Clean Data Receive] happens at 2026-4-8
[Process Onboarding] happens at 2026-5-18
[Setup Podcast] happens at 2026-6-1


--SUPPORT--

' caption Project Schedule
' legend
' Legend goes here
' end legend

@endgantt

〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
