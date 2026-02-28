# Android Studio Integration

## Overview

Google Antigravity can be used alongside Android Studio for AI-powered Android development. While Antigravity runs as a standalone IDE, it integrates with your Android project structure and tooling for a seamless development experience.

## Setup

### Prerequisites

- Android Studio installed (Arctic Fox or later)
- Android SDK configured
- Google Antigravity installed
- A valid Google account

### Open Your Android Project

1. Launch Antigravity
2. Open your existing Android project directory
3. Antigravity detects the project structure (`build.gradle`, `AndroidManifest.xml`, etc.)
4. The agent gains access to Gradle, ADB, and Android-specific tooling

## Workflow

### Feature Development

```
"Add a RecyclerView with a custom adapter to the MainActivity 
 that displays a list of items from the Room database"
```

The agent will:
1. Create the RecyclerView layout XML
2. Implement the adapter class
3. Set up the Room entity and DAO
4. Wire everything in the Activity
5. Run the build to verify compilation

### UI with Jetpack Compose

```
"Create a settings screen using Jetpack Compose with 
 Material 3 theme, including dark mode toggle"
```

The agent understands Compose conventions and generates idiomatic `@Composable` functions.

### Gradle Configuration

```
"Add the Hilt dependency injection library and set up 
 the application module"
```

The agent modifies `build.gradle.kts`, adds annotations, and creates the Hilt module.

## Testing

### Unit Tests

Agents can generate JUnit and Mockito tests:

```
"Write unit tests for the UserRepository class, 
 mocking the network layer"
```

### Instrumented Tests

For UI tests, the agent can generate Espresso or Compose test code:

```
"Write an Espresso test that verifies the login flow"
```

> [!NOTE]
> Running instrumented tests requires an Android emulator or connected device. The agent can invoke `adb` commands but cannot interact with the emulator UI directly.

## Common Tasks

| Task | Agent Capability |
|---|---|
| Create Activities/Fragments | ✅ Full support |
| Jetpack Compose UI | ✅ Full support |
| Room database setup | ✅ Full support |
| Gradle dependency management | ✅ Full support |
| XML layouts | ✅ Full support |
| Unit test generation | ✅ Full support |
| Build & compile | ✅ Via Gradle CLI |
| Run on emulator | ⚠️ CLI only (`adb install`) |
| Visual UI testing | ❌ Requires emulator GUI |

## Tips

1. **Keep Android Studio open** for visual tasks — use Antigravity for code generation
2. **Use the terminal** — Agents can run `./gradlew build`, `adb install`, etc.
3. **Compose over XML** — Agents produce better results with Compose (pure Kotlin)
4. **Provide context** — Mention your architecture pattern (MVVM, MVI, etc.)

## See Also

- [Getting Started](./getting-started.md) — General Antigravity setup
- [Features](./features.md) — Core platform capabilities
- [Skills Guide](./skills-guide.md) — Create Android-specific skills
