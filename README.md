# Clean Architecture in iOS

![Swift](https://img.shields.io/badge/Swift-5.0-FA7343?style=flat-square&logo=swift&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-iOS-000000?style=flat-square&logo=apple&logoColor=white)
![Architecture](https://img.shields.io/badge/Architecture-Clean%20Architecture-2563EB?style=flat-square)
![Pattern](https://img.shields.io/badge/Pattern-MVVM-7C3AED?style=flat-square)
![Xcode](https://img.shields.io/badge/Xcode-15%2B-147EFB?style=flat-square&logo=xcode&logoColor=white)

A practical iOS application demonstrating **Clean Architecture** principles combined with the **MVVM** pattern in Swift. Built as a real-world assignment to showcase scalable, maintainable, and testable iOS code structure.

---

## Architecture Overview

This project follows **Clean Architecture** — separating the codebase into distinct layers with clear responsibilities and dependencies flowing inward only.

```
┌─────────────────────────────────────┐
│         Presentation Layer          │
│     (ViewControllers / ViewModels)  │
├─────────────────────────────────────┤
│           Domain Layer              │
│      (Use Cases / Entities)         │
├─────────────────────────────────────┤
│            Data Layer               │
│   (Repositories / API / Storage)    │
└─────────────────────────────────────┘
```

### Layer responsibilities

| Layer | Contents | Responsibility |
|---|---|---|
| **Presentation** | ViewControllers, ViewModels | UI logic, user interaction, data binding |
| **Domain** | Use Cases, Entities, Repository Protocols | Business logic, fully independent of frameworks |
| **Data** | Repository Implementations, API Client, Models | Data fetching, mapping, caching |

---

## Key Concepts Demonstrated

- **Clean Architecture** — strict layer separation, dependency inversion
- **MVVM** — ViewModels drive UI state, no business logic in ViewControllers
- **Repository Pattern** — abstracts data sources behind protocols
- **Use Cases** — each user action is a single-responsibility use case class
- **Protocol-oriented design** — every layer communicates via protocols, making units independently testable
- **Dependency Injection** — dependencies passed in, never created internally

---

## Tech Stack

| Technology | Usage |
|---|---|
| Swift 5 | Primary language |
| UIKit | UI layer |
| URLSession | Networking |
| Core Data / UserDefaults | Local persistence |
| XCTest | Unit testing |

---

## Project Structure

```
LineManAssignment/
├── Presentation/
│   ├── ViewControllers/
│   └── ViewModels/
├── Domain/
│   ├── Entities/
│   ├── UseCases/
│   └── Repositories/ (protocols)
├── Data/
│   ├── Repositories/ (implementations)
│   ├── Network/
│   └── Models/
└── Resources/
```

---

## Getting Started

### Requirements
- Xcode 15+
- iOS 15+
- Swift 5.0+

### Installation

```bash
git clone https://github.com/Ron-gahlot/Clean-Architecture-iOS.git
cd Clean-Architecture-iOS
open LineManAssignment/LineManAssignment.xcodeproj
```

Then build and run on a simulator or device using `Cmd + R`.

---

## Why Clean Architecture?

In large-scale iOS apps (like those I've worked on with 90M+ users at ZEE5), maintaining code without clear boundaries becomes a bottleneck. Clean Architecture solves this by:

- Making each layer independently **testable**
- Allowing **data sources** (API, CoreData, mock) to be swapped without touching business logic
- Enabling **parallel development** — UI and backend logic can be built simultaneously
- Reducing **coupling** — changes in one layer don't cascade through the whole app

---

## Author

**Rahul Kumar Gahlot** — Senior iOS Engineer

[![GitHub](https://img.shields.io/badge/GitHub-Ron--gahlot-181717?style=flat-square&logo=github)](https://github.com/Ron-gahlot)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Rahul%20Gahlot-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rahul-gahlot)
