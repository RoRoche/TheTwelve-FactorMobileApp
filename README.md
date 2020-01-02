# The Twelve-Factor Mobile App

My proposal of twelve factors that improve the build of modern mobile applications.
Moreover, I found the [ios-factor](https://ios-factor.com/) and here is the way I revisit it, with a focus on Android applications.

## The Twelve Factors

**1. Support the widest range of devices**

- OS version (backward API compatibility).
- Screen size.
- Device family.
- Don't assume that the user has the latest smartphone with the widest screen and the most powerful processor.

**2. Adapt the UX to the target OS standards**

- Follow editors guidelines.

**3. Maximise the use of native components**

- UI/UX widgets to build UI.
- SDK core components to build the logical layers.

**4. Build a smooth UI**

- Never block the UI and run big computation in background.
- Keep the user informed and notify him about the current status.
- Reuse cells in list.
- Deal with configurations changes and interruptions (phone call).
- Prepopulate forms as much as possible.

**5. Use local cache as single source of truth**

- So your application can work even without network (and access to the backend), cache remote data into local storage (into the embedded SQLite database).
- Build a consistent offline mode with data synchronization (compare delta to get the freshest data).

**6. Be careful of components lifecycle** 

- Dispose I/O jobs.
- Free memory.

**7. Exploit the applications ecosystem and be ready to expose yours if needed**

- Call external applications through intents or deep linking.
- If required, expose your non-sensitive data using content provider and expose logic via intent filters and deep linking.

**8. Ask permissions clearly**

- Explain why and what you have to ask it, to keep user trusting you.

**9. Minimize binary size**

- Minimize the use of 3rd-party libraries to reduce the binary size.

**10. Secure everything**

- Encrypt database.
- Store user preferences with encryption.
- Secure API communication.
- Obfuscate the source code.

**11. Be production-ready**

- Be able to deploy from any machine.
- Think to embed a verbose crash reporter, so that you can be aware of errors that occurred while using your application.
- Disable logging.
- Keep signing elements safe (certificates, keys) for later updates.

**12. Upgrade/downgrade database wisely**

- Use database version.
- Alter table to add/removes columns.
- Use logical default values.

## Also worth considering

- Take care of battery life.
- Minimize network footprint and data consumption.

## Also worth reading

- [Mobile application: the beginner guide](https://github.com/RoRoche/talks/blob/master/mobile_application_beginner_guide/mobile_application_beginner_guide.md)

## Inspirations

- <https://12factor.net/>
- <https://ios-factor.com/>
