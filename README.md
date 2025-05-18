# HakiSense

**HakiSense** is a cross-platform embedded application developed in C++ for real-time object detection, measurement, and 3D reconstruction. It is designed for deployment on platforms such as Raspberry Pi, macOS, and Linux, with a focus on maintainability, scalability, and portability through a clean architecture approach.

---

## 🚀 Project Overview

- Perform real-time detection and 3D modeling of physical objects using camera inputs
- Fully implemented in C++ following clean architecture principles
- Supports multiple hardware platforms via hardware abstraction layers
- Provides a minimal presentation layer for embedded environments through CLI and lightweight API interfaces
- Designed to be extensible and integrable with external systems via well-defined APIs

---

## 🏗 Architecture

The project follows a clean architecture pattern composed of the following layers:

### Domain Layer

- Core business logic including entities, use cases, and repository interfaces
- Platform and UI independent to ensure reusability and testability

### Data Layer

- Concrete implementations of repositories and data models
- Datasources responsible for interfacing with hardware and system resources:
  - Camera providers for Raspberry Pi, macOS, Linux
  - Vision processing components
  - Networking modules for API exposure

### Presentation Layer

- Controllers / Managers handling state management and interaction logic
- Interfaces such as CLI and lightweight API server to manage input/output operations within the embedded environment
- No direct UI elements; presentation is focused on embedded interaction

### Application Layer

- Application entry point, initialization, and dependency injection
- Platform detection and setup of appropriate hardware adapters

---

## 📁 Directory Structure

- src/
  - domain/
    - entities/
    - usecases/
    - repositories/
  - data/
    - models/
    - repositories/
    - datasources/
  - presentation/
    - controllers/
    - cli/
    - api/
  - app/
    - main.cpp
- tests/

---

## ⚙️ Platform Support

- Raspberry Pi: native camera and hardware access
- macOS and Linux: webcam access through OpenCV or equivalent libraries
- Hardware access abstracted to ensure platform independence and ease of extension

---

## 📄 License

Licensed under **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**.

You may:

- Share and adapt with attribution
- Use for non-commercial purposes only

Full license text available at: <https://creativecommons.org/licenses/by-nc/4.0/>

© Linhares David 2025
