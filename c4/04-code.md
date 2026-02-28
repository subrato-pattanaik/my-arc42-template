# Level 4 – Code / Class Diagram

> **C4 guidance:** Optional deepest level. Shows how components are implemented — class diagrams, ER diagrams, etc. Usually auto-generated from source code.  
> Tooling: [C4-PlantUML](https://github.com/plantuml-stdlib/C4-PlantUML) · [Structurizr](https://structurizr.com/) · [Mermaid C4](https://mermaid.js.org/syntax/c4.html)

---

```plantuml
@startuml
class SpeedCalculator {
  -calibrationFactor: double
  +calculateSpeed(sensorDelta: double): double
  +applyCalibrationFactor(factor: double): void
}

class CalibrationService {
  +calibrateWithGPS(gpsData: GPSFrame): CalibrationResult
}

class EventLogger {
  +log(event: MeasurementEvent): void
}

SpeedCalculator --> CalibrationService : uses
SpeedCalculator --> EventLogger : uses
@enduml
```

## Notes

> Add explanatory notes, decisions, or caveats about this diagram here.
