# Level 1 – System Context Diagram

> **C4 guidance:** Shows the system in the context of its users and external systems. Answers: What are we building? Who uses it? What does it interact with?  
> Tooling: [C4-PlantUML](https://github.com/plantuml-stdlib/C4-PlantUML) · [Structurizr](https://structurizr.com/) · [Mermaid C4](https://mermaid.js.org/syntax/c4.html)

---

```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Context.puml

Person(user, "Police Officer", "Operates the TPU device")
System(tpu, "Traffic Pursuit Unit", "Measures and records vehicle speeds")
System_Ext(gps, "GPS Satellite", "Provides positioning data")

Rel(user, tpu, "Uses")
Rel(tpu, gps, "Receives location data from")
@enduml
```

## Notes

> Add explanatory notes, decisions, or caveats about this diagram here.
