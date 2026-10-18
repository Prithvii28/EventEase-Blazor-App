# EventEase — Blazor Event Management App

EventEase is a beginner-friendly ASP.NET Core Blazor project created for a learning assignment. It demonstrates reusable components, routing, form validation, simple session state, and an attendance tracker.

## Features

- **Event Card component:** Edit event name, description, location, date, and capacity with Blazor input components and two-way binding.
- **Routing:** Home, Events, Register, and Attendance pages, with a not-found view.
- **Registration form:** Uses `EditForm`, data annotations, and validation messages for name, email, and event selection.
- **Session state:** A scoped `SessionState` service keeps the current user's name and demo attendee list while the app session is active.
- **Attendance tracker:** Toggle a registered attendee's status between present and not checked in.
- **Responsive layout:** Basic responsive CSS for desktop and mobile screens.

## Requirements

- .NET 8 SDK or a compatible later SDK
- Visual Studio 2022 with the ASP.NET and web development workload, or Visual Studio Code with C# Dev Kit

## Run locally

1. Install the .NET SDK.
2. Open a terminal in the folder containing `EventEase.csproj`.
3. Run:

   ```bash
   dotnet restore
   dotnet run
   ```

4. Open the local URL shown in the terminal.

## Pages

- `/` — Home
- `/events` — Edit and preview the event card
- `/register` — Register an attendee
- `/attendance` — Track attendance for registered emails

## Copilot assistance summary

Microsoft Copilot can be used as a coding assistant to draft and explain Blazor components, suggest routing patterns, help troubleshoot build or runtime errors, and recommend validation and state-management improvements. During development, review each suggestion, test the result, and adapt the code to the project's requirements. This repository's implementation should be described accurately in the final assignment: only claim Copilot assistance for steps where Copilot was actually used.

## Notes and limitations

- This is a learning/demo application, not a production event system.
- Attendee and attendance data are stored in an in-memory scoped service; they are not saved to a database and may be lost when the app session ends.
- The Event Card uses a shared event object. It is suitable for demonstrating two-way binding; a larger app could use explicit `EventCallback` handling for component-to-parent updates.
- No authentication, database, email sending, or deployment pipeline is configured.

## Suggested checks before submission

- Build and run the app locally.
- Test each navigation link.
- Try submitting the registration form with empty or invalid fields.
- Register an attendee and test the attendance toggle.
- Replace this README's notes with any changes you make.
