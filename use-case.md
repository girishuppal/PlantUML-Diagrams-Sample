〰️〰️〰️〰️USE CASE〰️〰️〰️〰️〰️〰️〰️〰️
@startuml Use Case
footer "Created by Girish Uppal"
skin rose

'!theme blueprint

skinparam actorStyle awesome
'skinparam style strictuml

left to right direction
'top to bottom direction


' All actors
actor "M365 Admin" as VA
'actor "CEO" as CE
actor "Reliability Engineer" as SC
actor "Document Notifier" as DR
actor "Data Custodian" as DN
actor "Google" as IP #line:blue;line.dotted
actor "Microsoft User" as QU #line:green;line.dotted


(Qualtrics Dashboard) #line:green;line.dotted
QU -> (Qualtrics Dashboard) #line:green;line.dotted


rectangle "Contact Management"{
(Create User) as CRU
(Invite SAP User) as INU
(Assign SalesForce Report access \n Roles to User) as APR
}
VA -up-> CRU
VA -up-> INU
VA -up-> APR

rectangle UsageAnalytics{
    (View Usage Analytics raw data) as VUR
}

VA -down-> VUR
rectangle Archiving{
(Disable SXA exclusive Users) as DPE

(Archive Some Reports) as ATR
}

VA -down-> DPE
VA -down-> ATR

rectangle "Infrastructure Setup"{
    (Create Key container) as CBC
    (Create Security record for report) as CSR
}

VA -up-> CBC
VA -up-> CSR

rectangle "Site Validation"{
    (Validate Site) as VAR
}
VA -down-> VAR

rectangle "Fabric Setup"{
    (Trigger Data Factory) as TFP
    (Upload Metadata file to Kafka) as UMF
}

VA -up-> TFP
VA -up-> UMF


rectangle "SharePoint Management"{
(Upload docs) as UPR
(Verify docs) as VER
(Create Custom docs) as CCR
}

VA -down-> UPR
VA -down-> VER
VA -down-> CCR

rectangle "Notebook Creation"{
    (Generate Loop Component) as CRR
    (Upload onnx to temp storage) as URT
}
IP --> CRR
IP --> URT

rectangle "IT Files"{
    (Download IT Files) as DSF
}

DR -> DSF


rectangle "Site Access"{
    (Download Page) as DOR
}
SC -up-> DOR
'CE -down-> DOR
DN -up-> DOR


@enduml

〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
