# Level 2 – Container Diagram

> **C4 guidance:** Zooms into the system boundary, showing high-level technical building blocks (containers) and how they communicate.  
> Tooling: [C4-PlantUML](https://github.com/plantuml-stdlib/C4-PlantUML) · [Structurizr](https://structurizr.com/) · [Mermaid C4](https://mermaid.js.org/syntax/c4.html)

---

```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

Person(user, "Police Officer")

System_Boundary(tpu, "Traffic Pursuit Unit") {
  Container(ui, "Operator UI", "Touchscreen / Display", "Controls and status display")
  Container(measuring, "MeasuringUnit", "Embedded C / RTOS", "Speed measurement and calibration")
  Container(recorder, "VideoRecorder", "H.264 / HD", "Records video clips of pursuits")
  ContainerDb(storage, "HDD Storage", "Filesystem", "Stores video clips and pursuit logs")
}

Rel(user, ui, "Interacts with")
Rel(ui, measuring, "Triggers measurement")
Rel(measuring, recorder, "Signals pursuit start/end")
Rel(recorder, storage, "Writes video clips")
@enduml
```

## Notes

> Add explanatory notes, decisions, or caveats about this diagram here.
