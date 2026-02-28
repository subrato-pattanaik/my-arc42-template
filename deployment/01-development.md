# Development Environment

> **Guidance:** Local developer machines and local infrastructure for development and unit testing.

---

## Infrastructure Overview

```plantuml
@startuml
node "<<device>>
Police Vehicle" {
  node "<<embedded>>
TPU Hardware" {
    component "MeasuringUnit" as mu
    component "VideoRecorder" as vr
    database "HDD Storage" as hdd
  }
  component "Operator UI
(Touchscreen)" as ui
}

node "<<external>>
GPS Satellite" as gps

mu --> gps : GPS signal
vr --> hdd : Write video
ui --> mu : Commands
@enduml
```

## Nodes and Components

| Node / Component | Technology | Description |
|-----------------|------------|-------------|
|                 |            |             |

## Network / Communication

| Channel | Protocol | Description |
|---------|----------|-------------|
|         |          |             |

## Configuration

> Describe environment-specific configuration, credentials management, and secrets handling.

## Notes

> Any additional remarks, constraints, or considerations for this environment.
