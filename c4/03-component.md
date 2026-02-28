# Level 3 – Component Diagram

> **C4 guidance:** Zooms into an individual container to show its internal components and responsibilities. Create one diagram per container as needed.  
> Tooling: [C4-PlantUML](https://github.com/plantuml-stdlib/C4-PlantUML) · [Structurizr](https://structurizr.com/) · [Mermaid C4](https://mermaid.js.org/syntax/c4.html)

---

```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Component.puml

Container_Boundary(measuring, "MeasuringUnit") {
  Component(speed, "SpeedCalculator", "Core logic", "Computes speed from sensor deltas")
  Component(calibration, "CalibrationService", "GPS-based", "Auto-calibrates measurement baseline")
  Component(logger, "EventLogger", "Internal", "Logs measurement events and errors")
}

Rel(speed, calibration, "Uses calibration factor from")
Rel(speed, logger, "Sends events to")
@enduml
```

## Notes

> Add explanatory notes, decisions, or caveats about this diagram here.
