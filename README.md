# GarageGang Project Template

![Last Commit](https://img.shields.io/github/last-commit/garage-gang/garage-gang-project-template?color=yellow)

## This is Garage Gang FRC Team 11025's starting point for a new robot code projects

This project is based on [AdvantageKit's Spark Swerve template](https://docs.advantagekit.org/getting-started/template-projects/spark-swerve-template/),

This project is setup to expect swerve drive with NEO motors.

Click **"Use this template"** at the top of this repo to start a new project pre-loaded with everything below — don't use WPILib's "Create a New Project" wizard for team projects, since it doesn't use our standards.

## Setup

After creating your repository from this template and cloning it, follow the steps below:

- [ ] Install the recommended VSCode extensions when prompted (Spotless Gradle, EditorConfig).
- [ ] Set team number and current year in `.wpilib/wpilib_preferences.json` if it isn't already correct.
- [ ] Open the folder in VSCode with the WPILib extension — do **not** run "Create a New Project," this repo already is one.
- [ ] Confirm formatting works: save a `.java` file and check it reformats automatically (see [Formatting](#formatting) below).

## Formatting

All code is auto-formatted with [Spotless](https://github.com/diffplug/spotless), using the Eclipse JDT formatter configured for **tabs** and **K&R-style braces** (config lives in `config/eclipse-java-formatter.properties`).

- **On save**: VSCode reformats automatically if the recommended Spotless Gradle extension is installed (see `.vscode/settings.json`).
- **On build**: `compileJava` depends on `spotlessApply`, so a local build always fixes formatting for you.
- **`spotlessCheck`**: run manually to fail on unformatted code without modifying files, see the Gradle Tasks section below.

If your editor ever disagrees with the build, run:

```bash
./gradlew spotlessApply
```

## Gradle Tasks

Below is a list of helpful Gradle tasks for this project.

```bash
./gradlew build # Build all code and check formatting

./gradlew deploy # Deploy to the roboRIO

./gradlew simulateJava # Simulate the robot code

./gradlew spotlessApply # Auto-fix formatting
./gradlew spotlessCheck # Check formatting without modifying files
```
