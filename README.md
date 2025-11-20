This repo only contains release binaries.

# Status and Progress

Below is a detailed list of features that are either completed, or in progress.
All features are required to satisfy an MVP for this app.

# Software Development

- [x] App distribution
  The ability to download the app.
- [x] Automatic update downloads  
  Identify and download updates for the app when they become available.
- [x] Automatic update installs
  Automatically install the update if the user decides to update.
- [x] Remote database integration
  Have a remote database to hold all user and application data, such
  as reports, user preferences, room session configurations, etc.
- [x] Logging
  Have a detailed and robust logging mechanism, which is used to
  collect logging and tracing data to aid in discovering and fixing
  bugs, performance issues, or anything else where we might need to
  peek inside of the app while it's running.
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
  Record each person's individual video performance
- [ ] Video recording
  Record each person's individual video performance


# UI Design

- [-] Logo
- [-] Color palette
- [ ] Sign-in screen
- [-] Welcome screen
- [-] Feedback test
  A test that is performed every time before joining a session room
  to avoid potentially ear-damaging audio feedback.
- [-] Session rooms
- [-] Settings
  This includes volume, panning, input and output device selection, etc.
- [ ] Metronome
- [ ] Recording