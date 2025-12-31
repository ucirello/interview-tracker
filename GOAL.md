# Bugs
- [x] the clock emoji/icon makes reading the seconds impossible (overlaps)
      did you use Playwright Snapshots to validate the layout?
      save the screenshots at the root of this project.

# Feature
I need an interview note tracking web application in HTML, inlined JS, and PicoCSS.

The idea is that this application will allow me to track interview notes with a particular candidate, and tag each note with a timestamp.

The basic interface is
```
┌──────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│                ┌─────────────────────────────────────────────┐               │
│                │               Candidate Name                │               │
│                └─────────────────────────────────────────────┘               │
│                                                                              │
│         HH:MM:SS │┌────────────────────────────────────────┐                 │
│                  ││                                        │                 │
│                  ││                                        │                 │
│                  ││                                        │                 │
│                  ││Note: this window resizes as I type the │                 │
│                  ││                  note                  │                 │
│                  ││                                        │                 │
│                  ││                                        │                 │
│                  ││                                        │                 │
│                  ││                                        │                 │
│                  │└────────────────────────────────────────┘                 │
│                  │                                                           │
│                  │┌────────────────────────────────────────┐                 │
│          HH:MM:SS││                                        │                 │
│                  ││                                        │                 │
│                  ││                                        │                 │
│                  ││Note: this window resizes as I type the │                 │
│                  ││                  note                  │                 │
│                  ││                                        │                 │
│                  ││                                        │                 │
│                  ││                                        │                 │
│                  ││                                        │                 │
│                  │└────────────────────────────────────────┘                 │
│                  │                 ┌───┐                                     │
│                  │                 │ + │                                     │
│                  │                 └───┘                                     │
│                                                                              │
│                                                                              │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘
```
Candidate Name is a text input field where I can type the candidate's name.
Each note is a text area that automatically resizes as I type the note.
Next to each note is a timestamp in HH:MM:SS format indicating when the note was created.
There is a "+" button below the notes that allows me to add a new note with the current timestamp.
I should be able to edit the timestamps too if necessary.
When I press the save button (not in the design) - it then pops out a Markdown version of my notes.

- [x] The application is a simple SPA (Single Page Application) that runs entirely in the browser.
- [x] It uses only pure HTML, inlined JavaScript, and PicoCSS for styling.
      PicoCSS: <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@picocss/pico@2/css/pico.lime.min.css" >
- [x] Export to Markdown format when I press the save button.
- [x] The application should be responsive and work well on both desktop and mobile browsers.
- [x] The application should have a clean and user-friendly interface.

CRITICAL: it must be a pure HTML and inlines JS and PicoCSS implementation, some light touch CSS to make looks be good is OK;
CRITICAL: use playwright screenshots (and the skill to operate playwright) to verify the application is working correctly.
