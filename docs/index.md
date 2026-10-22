---
title: Overview
description: "Summary of in-progress or completed project."
order: 0
---

{% include ddc-abbreviations.md %}

## Page contents


## Summary

### P.A.U.L.A. (Plan, Act, Uplift: Life Achieved) 

Is a personalized, offline-first Android task manager, daily routine tracker, and encouraging lifestyle companion. Developed in loving memory of Paula Elizabeth
Kleczka—who championed an organized living space, folded blankets, and caring for family. The application bridges structured productivity with uplifting personal connection. The app streamlines everyday responsibilities by combining customizable to-do lists and recurring habit checklists with an interactive 2D companion avatar that provides real voice encouragement. Users can organize daily household chores, manage family responsibilities, and track long-term habits while receiving audio affirmations and visual milestone rewards as items are completed.

## Intended users and user stories

- The Busy Household Manager 

    An individual or parent managing multiple domestic responsibilities, cleaning
    routines, and family to-dos who needs an organized, frictionless way to keep track of recurring chores.


- The Routine & Habit Builder

    A student or working professional striving to build structured daily habits (such 
    as tidying up a workspace, studying, or morning routines) through positive reinforcement.


- The Encouragement Seeker

    A user who experiences task fatigue or executive dysfunction and benefits from warm auditory 
    feedback, visual companion check-ins,and celebrated micro-wins rather than cold, corporate checklists.

## Functionality



- To-Do Lists & Daily Habits

    Create, edit, and check off one-time tasks or repeating routines (like folding blankets or tidying a room). 
Each item can have notes, due dates, priority stars, and category tags.


- Paula's 2D Companion Avatar

    A friendly illustrated character on the main screen that reacts to your day. She greets you when you open the app, 
rests during quiet hours, and celebrates when you finish your chores.


- Real Spoken Voice Encouragement

    Plays short audio clips of Paula’s actual voice. You hear warm greetings, gentle task reminders, 
and encouraging words when you clear your daily list or reach a milestone.


- Simple Swipe Lists (RecyclerView)

    Displays your tasks in clean, easy-to-read cards. You can swipe a task to check it off, 
sort by urgency, or filter by categories like Household and Family.


- Custom Settings & Quiet Hours

    A straightforward settings menu to adjust volume, toggle between voice clips and gentle chimes,
    turn on subtitles, and set nighttime "quiet hours" so alerts never disturb your rest.


- 100% Offline Storage

    Saves all tasks, habits, and streaks directly on your phone. The app never needs an internet 
connection or cloud account,
so your data stays private and loads instantly.


## Persistent data

Because P.A.U.L.A. is an offline-first app, all data is
stored locally on the device using Google Room and SQLite.
No external server is required, ensuring instant access
and complete privacy:

* **Task Items:** Stores task titles, descriptions, due
  dates, priority levels, category tags (e.g., Household,
  Family), and completion status across sessions.
* **Daily Routines & Habits:** Tracks recurring checklists
  (such as making the bed and folding blankets), target
  frequencies, and daily streak counts.
* **Voice Prompt Mappings:** Saves trigger conditions,
  audio clip references, and text transcripts for Paula's
  voice affirmations.
* **Photo Attachments:** Stores local file references and
  timestamps for photos taken of tidy spaces and completed
  projects.
* **User Preferences:** Preserves quiet-hour windows, audio
  volume levels, caption toggles, and notification
  settings using Android preferences.

## Device/external services

### Client Device Services
* **Audio Playback (`MediaPlayer` / `SoundPool`):** Plays
  recorded audio clips of Paula's voice for greetings,
  reminders, and celebration milestones.
* **Device Camera (`Camera API`):** Allows users to snap
  photos of clean spaces, family moments, or finished
  chores to attach to tasks.
* **Reminders & Alerts (`AlarmManager` & `NotificationManager`):**
  Schedules daily routine reminders and respects quiet
  hours.
* **Tactile Feedback (`Vibrator API`):** Provides gentle
  haptic vibrations when checking off tasks or completing
  habits.

### External Services
* **YouTube Video Service:** Provides quick access to
  helpful instructional video tutorials (such as blanket-folding
  techniques, laundry tips, and kitchen tidying guides)
  linked directly to relevant household tasks and routines.

## Stretch goals and possible enhancements 

1. **Custom Color Themes (Least Complex):**
   Add quick theme toggles featuring Paula's favorite
   colors—pink, purple, and black—for app accents and
   cards.

2. **Visual Streak Calendar & Heatmap (Moderate Complexity):**
   A monthly calendar grid that highlights consistency
   and habit streaks with visual color intensity.

3. **In-App Voice Clip Import (Moderate Complexity):**
   A simple tool inside settings allowing users to record
   or import new audio clips directly onto the device.

4. **Animated 2D Avatar Reactions (High Complexity):**
   Upgrade the static avatar illustrations to smooth 2D
   vector animations (such as waving arms or smiling)
   when tasks are cleared.

5. **Encrypted Local Backup & Restore (Most Complex):**
   Allow users to export and import an encrypted backup
   file of their tasks, streaks, and photos to phone
   storage for safekeeping.


