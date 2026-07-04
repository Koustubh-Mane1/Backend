# JVM Learning — Multi-Module Gradle Project

A structured multi-module Gradle monorepo for learning Java/JVM backend concepts:
Spring Boot, Micronaut, concurrency, web, and data access.

## Module Structure

| Path | Topic | Status |
|------|-------|--------|
| `module-0-jvm/hello-world` | JVM basics, plain Java entry point | Ready |
| `module-1-concurrency/threads-lifecycle` | Thread states and lifecycle | Placeholder |
| `module-2-di/spring-boot-basics` | Dependency injection with Spring Boot | Ready |
| `module-3-web/` | Web layer (to be added) | — |
| `module-4-data/` | Data access patterns (to be added) | — |

## Prerequisites

- JDK 21
- No Gradle installation required — uses the Gradle wrapper (`./gradlew`)

## Build Everything

```bash
./gradlew build
```

## Run Tests for a Module

```bash
./gradlew :module-0-jvm:hello-world:test
./gradlew :module-1-concurrency:threads-lifecycle:test
./gradlew :module-2-di:spring-boot-basics:test
```

## Run the Spring Boot Application

```bash
./gradlew :module-2-di:spring-boot-basics:bootRun
```

## Run the Hello-World Main Class

```bash
./gradlew :module-0-jvm:hello-world:run
```

## Compile Only (Skip Tests)

```bash
./gradlew classes
```

## List All Projects

```bash
./gradlew projects
```

## Adding a New Module

1. Create the directory: `module-X-topic/my-subtopic/`
2. Add a `build.gradle` inside it (copy the minimal template from an existing module)
3. Add `include 'module-X-topic:my-subtopic'` to `settings.gradle`
