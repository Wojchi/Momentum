# Momentum

> Build better habits. Track your progress. Keep moving forward.

**Momentum** is an open-source self-improvement app for Android that brings habit tracking, workouts, nutrition tracking, and daily planning together in one place.

The goal of Momentum is simple: provide the essential tools for working on yourself without making the experience unnecessarily complicated.

> [!NOTE]
> Momentum is currently under active development. Features and UI may change as the project evolves.

---

## Features

Momentum is built around a few core areas of self-improvement.

### Dashboard

The Dashboard provides an overview of your day and recent progress.

Planned features include:

- Daily motivational quote
- Habit activity heatmap
- Daily to-do list
- Overview of your daily progress
- Historical activity tracking

The activity heatmap is inspired by GitHub's contribution graph and provides a visual representation of how consistently habits have been completed over time.

---

### Habits

Create habits and track them individually for each day.

Features include:

- Create custom habits
- Daily habit checklist
- Navigate between days
- Track completion separately for every date
- View historical habit activity
- Long-term activity visualization

Completing a habit today does not automatically mark it as completed yesterday or tomorrow. Every completion is stored for its respective calendar day.

---

### Workouts

Create and manage your own workout routines.

Features include:

- Create workout templates
- Add exercises to workouts
- Choose from existing exercises
- Create custom exercises
- Track completed workout sessions
- View recent workout history

A workout can contain any number of exercises, allowing routines such as:

- Push
- Pull
- Legs
- Calisthenics
- Custom training plans

---

### Fuel

Track your daily calorie intake through a simple nutrition overview.

Features include:

- Set a daily calorie goal
- Track consumed calories
- See remaining calories
- Add calories directly
- Create reusable custom meals
- Store calorie history by date

For example:

```text
Daily Goal: 2500 kcal
Consumed:   1700 kcal
Remaining:   800 kcal
```

Custom meals can be saved and reused later instead of entering the same information repeatedly.

---

### Daily To-do

Momentum also includes a lightweight daily task list.

You can:

- Add tasks
- Complete tasks
- Delete tasks

Tasks belong to a specific calendar day. Starting a new day gives you a fresh daily list while previous entries can remain stored as historical data.

---

## Screenshots

> Screenshots will be added as development progresses.

<!--
Example layout:

| Dashboard | Habits | Workouts | Fuel |
|-----------|--------|----------|------|
| ![](docs/screenshots/dashboard.png) | ![](docs/screenshots/habits.png) | ![](docs/screenshots/workouts.png) | ![](docs/screenshots/fuel.png) |
-->

---

## Tech Stack

Momentum is developed as a native Android application.

### Core

- **Kotlin**
- **Jetpack Compose**
- **Material 3**

### Architecture

The project is structured with a separation between UI and business logic and is designed to remain maintainable as new features are added.

The architecture makes use of concepts such as:

- Compose UI
- ViewModels
- Repositories
- Data models
- Reusable UI components
- Centralized navigation

Existing project structures and components are preferred over introducing unnecessary abstractions or dependencies.

### Persistence

Momentum is designed around local, persistent data.

Where appropriate, the project uses:

- **Room** for structured local application data
- **DataStore** for application preferences and settings

Persistent data may include:

- Habits
- Habit completion history
- Daily to-do items
- Workout templates
- Exercises
- Custom exercises
- Workout sessions
- Meals
- Daily calorie entries
- App settings

---

## Date-Aware Tracking

A major part of Momentum is that data is associated with actual calendar dates.

The application does not treat a new day as simply "24 hours since the last session."

Instead, daily information is associated with the user's local calendar day.

This applies to:

- Habit completions
- Daily to-do items
- Calorie tracking
- Daily quotes
- Activity history

For example:

```text
23:59 — September 1
Data belongs to September 1

00:01 — September 2
A new calendar day begins
```

Historical information remains stored so progress can be viewed over time.

---

## Project Structure

Momentum aims to keep responsibilities separated and features easy to extend.

A simplified representation of the architecture looks like:

```text
UI
│
├── Screens
├── Components
├── Navigation
└── Theme
     │
     ▼
ViewModels
     │
     ▼
Repositories
     │
     ▼
Data Layer
├── Models
├── Local Database
└── Preferences
```

The exact structure may evolve alongside the application.

---

## Getting Started

### Prerequisites

To work on Momentum, you will need:

- Android Studio
- Android SDK
- JDK compatible with the project's Android Gradle Plugin
- Git

---

### Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Momentum.git
```

Then navigate into the project:

```bash
cd Momentum
```

---

### Open the Project

1. Open **Android Studio**.
2. Select **Open**.
3. Choose the cloned Momentum directory.
4. Allow Gradle to synchronize the project.
5. Select an Android emulator or connected device.
6. Run the application.

---

## Roadmap

Momentum is being developed feature by feature.

### Foundation

- [ ] Core navigation
- [ ] Data models
- [ ] Local persistence
- [ ] App settings

### Habits

- [ ] Create habits
- [ ] Daily habit tracking
- [ ] Date-based habit completion
- [ ] Habit history
- [ ] Activity heatmap

### Dashboard

- [ ] Daily overview
- [ ] Daily quotes
- [ ] Daily to-do list
- [ ] Habit activity visualization

### Workouts

- [ ] Workout templates
- [ ] Exercise library
- [ ] Custom exercises
- [ ] Workout sessions
- [ ] Workout history

### Fuel

- [ ] Daily calorie goal
- [ ] Calorie tracking
- [ ] Direct calorie entry
- [ ] Custom meals
- [ ] Meal library
- [ ] Daily calorie history

### Future Ideas

Momentum is intended to continue growing over time. Possible future additions include:

- Habit reminders
- Habit scheduling
- Habit icons and colors
- More detailed workout statistics
- Exercise muscle groups
- Exercise equipment tracking
- Macronutrient tracking
- Meal ingredients
- Calendar view
- More progress statistics
- Additional customization options

---

## Contributing

Momentum is open source, and contributions are welcome.

If you find a bug, have an idea for a feature, or want to improve an existing part of the application, feel free to contribute.

### How to Contribute

1. Fork the repository.

2. Create a new branch:

```bash
git checkout -b feature/your-feature-name
```

3. Make your changes.

4. Commit your changes:

```bash
git commit -m "Add: description of your change"
```

5. Push your branch:

```bash
git push origin feature/your-feature-name
```

6. Open a Pull Request.

Please keep changes focused and avoid unrelated refactoring in the same Pull Request.

---

## Development Guidelines

When contributing to Momentum:

- Use Kotlin.
- Follow the existing project architecture.
- Use Jetpack Compose for Compose-based UI.
- Use Material 3 components where appropriate.
- Reuse existing components before creating new ones.
- Keep UI and business logic separated.
- Avoid unnecessary dependencies.
- Avoid unnecessary large refactors.
- Do not remove existing functionality without discussion.
- Make sure persistent data survives application restarts.
- Ensure date-dependent functionality works correctly across calendar days.
- Keep new functionality maintainable and extensible.

Before opening a Pull Request, make sure the project builds successfully and relevant tests still pass.

---

## Feature Requests

Have an idea that would make Momentum better?

Open a GitHub Issue and describe:

- The problem you want to solve
- Your proposed feature
- Why it would be useful
- Any UI or implementation ideas you may have

Suggestions and discussions are welcome.

---

## Bug Reports

If you encounter a bug, please open an Issue and include as much information as possible.

Useful information includes:

- What happened
- What you expected to happen
- Steps to reproduce the problem
- Android version
- Device or emulator
- Screenshots or screen recordings
- Relevant logs, if available

---

## Open Source

Momentum is developed openly so that anyone interested in Android development, fitness, productivity, or self-improvement can contribute.

Contributions can range from small improvements and bug fixes to entirely new features.

You do not need to implement a large feature to contribute.

---

## License

<!-- Replace this section once you have selected a license. -->

A license for this project has not yet been specified.

See the `LICENSE` file for details once a license has been added.

---

## Support

If you like the project, consider giving the repository a ⭐.

It helps others discover Momentum and supports the continued development of the project.

---

<p align="center">
  <b>Momentum</b><br>
  Build better habits. One day at a time.
</p>
