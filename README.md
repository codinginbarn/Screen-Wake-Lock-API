In the demo.html:

- There is a "Toggle wake lock" button and a paragraph to display the wake lock status.

- When you click the "Toggle wake lock" button, if the wakeLock variable is not null, it will release the wake lock and null out the wakeLock variable. If wakeLock is null, it will attempt to request a wake lock.

- Note that before requesting a wake lock, you should confirm that the navigator.wakeLock API is available (not shown in this example).

- The requestWakeLock function tries to request a 'screen' wake lock, adds an event listener for the 'release' event, and logs the wakeLock.released status.

- The wakeLock.released property returns a boolean indicating whether this WakeLockSentinel's wake lock has been released. True if it was released, and false otherwise.

- The wakeLock.release method releases this WakeLockSentinel's wake lock.

Add this HTML to a file and open that file in a browser to see a working example. Please, remember that some browsers may need user activation before they allow the WakeLock API. So, the function should be called from an event handler (like onClick).
