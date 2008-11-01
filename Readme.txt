Brain Workshop: a Dual N-Back game in Python

Thank you for downloading Brain Workshop.
Please visit the Brain Workshop web site for help & instructions!

From the main screen, press W to open the web site.
Pressing H will open the Help & Tutorial page.

Or visit:
   http://brainworkshop.sourceforge.net

Configuration options are available in the file 'config.ini'
in the data folder. This file is created the when the program is
first launched. Windows users can access this file via the
'Configuration' item in the Brain Workshop group in the Start Menu.

Let me know if you have any comments or suggestions:

   plhosk@gmail.com

Enjoy!

----------------------------------------------------------------------
*** NOTE TO MAC OS X, LINUX AND WIN32 SOURCE USERS: ***

Python 2.5 or 2.6 is required to run Brain Workshop on Mac OS X
and Linux. Python 2.4 may also work as long as the python-ctypes
package is installed.
[Note: Windows versions have python included.]

Python 2.6 can be downloaded here:
      http://www.python.org/download/releases/2.6/

Music support requires AVBin (highly recommended!)
Download AVBin here:
      http://code.google.com/p/avbin/

Detailed instructions and links for Mac OS X, Linux and win32 source
installation are available on the Brain Workshop web site:

    http://brainworkshop.sourceforge.net

----------------------------------------------------------------------
Change Log:

4.2:
* Added new mode to stretch working memory: Dual Variable N-Back.
      The n-back level is displayed in the center and changes
      randomly every 3 seconds.
* Added single-task n-back modes: Position N-Back and Audio N-Back.
* Default config file is no longer packaged with the download
      so upgrading to this version won't overwrite existing
      configuration settings. The config file config.ini will be
      created if necessary when BW is launched for the first time.
* OpenAL is now the default sound driver in Linux if available.
      If you're having sound problems, it may help to install the
      python-openal package.
* There's no longer any need to install pyglet on Mac OS X or Linux.
      It's now included with the source distribution.

4.12:
* Fixed level increase threshold in Novice mode
* Novice mode now generates 4 visual matches, 4 audio matches
      and 2 simultaneous matches, matching the formula used in the
      original study.

4.11:
* Fixed level decrease threshold in Novice mode
* Added a configuration option to use the pre-4.1 flat squares
* Two changes to Novice Mode to eliminate the last of the differences
  compared to the original study protocol:
     1. Exactly 6 position and 6 audio matches are now generated each
           session
     2. The score for the session is set as the lowest of the two
           individual modality scores (visual & audio).

4.1:
* The squares in Dual & Triple N-Back have a new look.
* Individual scores for each input category (position, sound, etc)
     are shown in the graph screen.
* The number of sessions below 50% required to trigger a
     level decrease has been changed from 1 to 3.
* New piano sounds are available in the config file to test your
     tonal memory. 
* Pressing the ESC key during a session will return you to the
     main screen instead of quitting the program.

4.04:
- Added the division operation to the Arithmetic N-Back modes.
     Use the period key '.' to insert a decimal point.
     Each of the operations (add, subtract, multiply, divide)
     can be turned off or on in any combination in the config file.
- Fixed a bug where if you had just advanced to a new level and
     quit BW, the next time you restarted you would be back at
     the previous level.
- Added config option to play music in Manual mode.

4.03:
- Added new number sounds (0-13). Either the letters or the numbers
     will be chosen randomly at the start of each session.
- The female voice sounds are now selected by default.
- Added two new game modes, Dual Arithmetic N-Back and Triple
     Arithmetic N-Back. Press N from the main screen to access
     the extra game modes.

4.02:
- Fixed sound driver selection in Linux.
- A few minor changes related to Arithmetic N-Back mode.

4.0:
- New game mode: Arithmetic N-Back (see tutorial for details)
- Optional Novice mode (aka BT mode) emulates the original study
  protocol.
- New NATO Phonetic Alphabet sounds (alpha, bravo, charlie, etc).
     The old sounds are still available as an option.
- Keep track of your daily progress with the new graphing feature.
- Export your history of daily n-back averages to a text file
  for easy pasting into a spreadsheet.
- Adaptive level-changing model ensures you're always playing
     at the right level.
- Keyboard keys can now be redefined.
- Feedback for missed cues is displayed.
- Feedback can be turned off in the config file if desired.
- Text can be hidden during gameplay to reduce distractions.
- Optional full-screen mode for a larger, distraction-free
     playing field.
- Optional black background reduces eye strain.
- Easy config file provides access to configuration options.

3.1:
- Enabled high performance VBO (vertex buffer object). If you get a
  MissingFunctionException, use the --novbo command line parameter
  to launch Brain Workshop.
- Changed preferred sound driver to ALSA on Linux.
- Converted letter sounds to 44.1 KHz to alleviate crackling problem
  on certain sound hardware.

3.01:
- When first loading, if the last session completed was in Standard
  mode, Brain Workshop will start at the same n-back level.
- Only today's sessions are loaded in the history chart.

3.0:
- Three consecutive scores of >=80% are now required to advance levels,
  as indicated by the grey/green squares in the top left corner.
  A grey square will turn green if a >=80% score is achieved and a
  green square (if any) will turn grey if the score is below 80%.
  Once both squares are green and another 80% is achieved, the level
  increases. A 100% score will cause an instant advancing.
- The entries on the session history chart will turn green if
  the session is >= 80%. The chart now displays in a variable-width
  font.
- Added the time.sleep() workaround to reduce CPU usage on OS X.
  Disabled Vsync to eliminate an error message on certain machines.
- New columns have been added to the stats.txt file, including
  individual percentage scores for the six input types. Please see
  Readme-stats.txt in the data directory for details.

2.7:
- Added a new column in the stats file:
	0 = Standard mode, 1 = Training mode
- one new music clip added
- Added an encouraging message if you get below 40%

2.64:
- Lowered level advance threshold to 80%.
- Added a workaround for pyglet.gl.lib.MissingFunctionException
  which occurs on certain video cards.

2.63:
- Fixed a bug causing 100% CPU utilization.
- Fixed a crash caused by the music clip feature.
- Reduced startup time and memory footprint.

2.62:
- Contribution to the n-back average is now calculated like so:
      (nback - 1) + percentage / 100
  This means the average n-back level for a single 4-back session
  with a score of 50 percent will now be 3.5 instead of 2.

- Fixed a bug in the input feedback that would show correct responses
  as incorrect (this did not affect stats). 
- Added more music clips and adjusted the length and volumes of the
  existing ones.

2.6:
- Added color feedback on input. The input labels ('A: position' etc)
  will turn red for incorrect, green for correct and blue if
  there haven't been enough trials yet.

2.5:
- Fixed bug where a bogus stats entry would be created under
  certain conditions when switching from Standard to Training mode.
- Removed the need for Tkinter on Linux and OS X.

2.4:
Added music clips which play when certain scores are achieved.

2.3:
- Added a Sessions Today indicator which shows the total number of
  sessions completed this calendar day. Useful for tracking progress
  on your 20 session per day training quota.
- Added possibility of different stats files on the command line.
     Give each person in your family a separate desktop icon!
        example: brainworkshop.exe --statsfile fred.txt
                 brainworkshop.exe --statsfile mary.txt
- Brain Workshop now starts in Standard mode. This enforces
  certain settings for number of trials and time per trial,
  making it easier to compare scores. Currently these are
  specified as follows:
	All modes are 20 trials per session.
            Dual N-Back: starts with 2-back, 3 seconds
          Triple N-Back: starts with 2-back, 3 seconds
     Dual Letter N-Back: starts with 1-back, 3 seconds
      Tri Letter N-Back: starts with 1-back, 4 seconds
     Quad Letter N-Back: starts with 1-back, 4 seconds
- Fixed a bug in the average n-back calculation
- Changed stats file format from tab-separated to comma-separated.
  Old stats files will still load successfully.

2.2:
   - Session stats are now output to the file data\stats.txt
   - Previous stats are loaded upon launch.
   - Added an option to clear stats (this does not affect stats.txt)
   - Average N-Back level is calculated for the last 20 sessions.
        The contribution of a particular session is calculated:
           Contribution = (N-back level) * (Percentage score) / 100
        Average is calculated as:
           Average = (sum of contributions) / (number of sessions)

2.1:
   - Added three new challenging game modes:
        Dual Letter N-Back, Tri Letter N-Back, Quad Letter N-Back
   - Adjusted level advance threshold from 100% to 90%
   - Adjusted "applause" threshold from 80% to 70%

2.0:
   - Applause sound now plays when a score of 80% is achieved
   - Version check is now performed on launch
   - Added a workaround for the pyglet.gl.ContextException error
        which occurs on certain video cards
   - Added a more descriptive error message in case an old version
        of pyglet is installed
   - Fixed cosmetic issue with the session history label on Linux
