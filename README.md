This repo only contains release binaries.

# Status and Progress

Below is a detailed list of features that are either completed, or in progress.
All features are required to satisfy an MVP for this app.

## Software Development

These are the list of features related specifically to the software implementation
of the app.

- [x] App distribution
      The ability to download the app.
- [x] Automatic update downloads  
       Identify and download updates for the app when they become available.
- [x] Automatic update installs
      Automatically install the update if the user decides to update.
- [x] Remote database integration
      Have a remote database to hold all user and application data, such
      as reports, user preferences, room session configurations, etc.
- [ ] Find and host a production-ready server
      Currently, the database is hosted on a Raspberry Pi 4. This is fine during
      the testing phase, but will be unsuitable for the production release. Therefore,
      we need to find a production-ready server, or host in the cloud.
- [x] Logging
      Have a detailed and robust logging mechanism, which is used to
      collect logging and tracing data to aid in discovering and fixing
      bugs, performance issues, or anything else where we might need to
      peek inside of the app while it's running.
- [ ] Local log file
      Save logs to a rolling log file locally on the user's system.
- [ ] Remote error reporting
      Collect logging data, such as errors and crashes, and send them to the
      remote database.
- [x] ASIO support
      Setup and successfully compile the app with the ASIO SDK.
- [x] Enumerating audio devices
      Discover and list all connected audio input and output devices on
      every supported platform and host, including ASIO-capable devices.
- [ ] Virtual audio bridging
      Provide a mechanism for routing audio from other applications, such as
      screen readers and the browser, into our app while running in exclusive
      mode.
- [x] Signing in
      Provide a secure way to sign-in to the app.
- [ ] Audio recording
      Record audio during sessions.
- [ ] Metronome
      Provide a latency-compensated metronome.
- [ ] Video streaming
      Stream a high-latency video feed of performances.
- [ ] Audio recording
      Record each individual audio channel stream during sessions.
- [ ] Video recording
      Record each person's individual video performance

# UI Design

These are the list of tasks related to the Figma design file for the UI of the app.

- [-] Logo
- [-] Color palette
- [ ] Sign-in screen
- [-] Welcome screen
- [-] Feedback test
  A test that is performed every time before joining a session room
  to avoid potentially ear-damaging audio feedback.
- [-] Session rooms
  This is the main interface where the users will be in for the majority of their use
  with the app. It's equivalent to a virtual call like with Zoom.
- [-] Settings

  - [x] Volume
  - [x] Panning
  - [x] input and output device selection
  - [ ] Joining rules and permissions for spectators
  - [ ] Screen reader-specific adjustments, like the announcing of live-regions.
  - [ ] Spectator audio mix.
  - [ ] Descriptive tooltips for all settings and keyboard shortcuts

- [ ] Metronome
- [ ] Recording
- [ ] Spectators
      Ability to see who and how many people are spectating.
- [ ] Break-out rooms
      These are smaller rooms intended to allow larger groups of musicians to
      practice their parts in small independent rooms.
- [ ] Global volume
- [ ] Performance metrics and stats for nerds
      This includes metrics such as round-trip latency, CPU and memory histograms.
- [ ] Chat
      Allows communication between members who do not have a dedicated whisper mic.
