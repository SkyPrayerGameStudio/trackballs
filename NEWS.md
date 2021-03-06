v0.00 Nov 2002; Mathias Broxvall <matbr@home.se>, Initial release:

29 Nov 2002; Väinö Järvelä <vaino.jarvela@pp.inet.fi> various files:

- Made compatible with GCC3.1.
- Added new argument/options handling.
- Added mute and windowed modes.

12 Dec 2002; Mathias Broxvall <matbr@home.se>, various files:

- Cleaned up guile interface
- Added "baby" balls
        
06 Jan 2003; Väinö Järvelä <vaino.jarvela@pp.inet.fi>, enterHighScoreMode.cc:

- Default name for highscore entry equals to the user running the game.
          Fetched from environment variable "USER"
- Change the "Name:" text to "Enter your name:"        for better clarity.

06 Jan 2003; Mathias Broxvall <matbr@home.se>, various files:

- New ball modifications and effects
- More guile functions
- Extra levels
- Added "acid" flag to floors and editor
- Updated configure scripts, works better but requires autoconf > 2.53
          when rebuilding ./configure
- Commandline arguments for graphics resolution
- In editor: picking up colors, manipulating flags in large regions, etc.
- Added "sand" flag to floors and editor
- Left mousebutton makes the ball jump
- ???
        
13 Jan 2003; Frank Gevaerts <frank@gevaerts.be>, map.cc:

- Replaced "system / gzip" hack with calls to zlib functions

13 Jan 2003; Mathias Broxvall <matbr@home.se>, map.cc:

- Changed fileformat to be platform independent
- Release trackballs as v0.3.0

19 Jan 2003; Mathias Broxvall <matbr@home.se>, various files:

- Added bonuses at end of level
- Replaced player info (time,score,lives,mods) with graphical "panel"
- Fixed some graphic glitches
- Added forcefields, switches to turn objects on/off
- New levels
- Released as trackballs v0.4.0

31 Jan 2003; Mathias Broxvall <matbr@home.se>, various files:

- Replaced all sound effects.
- Made a "Hall of Fame"
- Fixed button clicks on the main screen
- Added "buy continue" when dead        
- Splashscreen.
- Editor save button and filepermission check
- Added "using namespace std" in every source file.
- Released as trackballs v0.4.1        

04 Feb 2003; Mathias Broxvall <matbr@home.se>, various files:

- More soundeffects
- Added fog
- Settingsscreen
- Keyboard controlls
- Replaced fonts for a GPL'ed one
- Added player setup screen, choose starting level from
          already visited ones.
- Added install script for icons under KDE
- alternative colors and textures for player
- Released as trackballs v0.5.0

08 Feb 2003; Mathias Broxvall <matbr@home.se>, various files:

- Replaced fonts, *again*, since some fontservers didn't handle
          the old ones correctly.
- Fixed bug in the physics engine
- Added extra call to SDL_Quit at exit
- Fixed crash when entering player name
- Ball textures are not drawn if gfx_details == NONE
- Released as trackballs v0.5.1        

15 Feb 2003; Mathias Broxvall <matbr@home.se>, various files:

- Added "health bar" for player
- Created "pipes" and "pipe connectors"
- Diamonds acting as "save points"
- Small fixes in the default levels
- Created the notion of levelsets, highscores for them etc.
- Added Help screen
- Fixed some "popups" in map drawing
- Trackballs is now hosted at sourceforge!
- Released as trackballs v0.6.0
        
21 Feb 2003; Mathias Broxvall <matbr@home.se>, various files:

- Fixed mouseclicks in menus
- Added music and effects volume in settings        
- Added editable wall colors 
- Bug when fps>100 fixed. Also alternative keys for diagonal movement
- AA for mapgrid
- Rolling with spikes generates debris and is unstalbe
- Editor now uses F1-F5 to select function and arrows more around.
- Fixed problem with too large textures by rescaling images if neccessary.
- Redone helpscreen
- Polished some levels and added a new "pipe" level
- Not released as trackballs v0.6.99 (PRERELEASE)

22 Feb 2003; Mathias Broxvall <matbr@home.se>, various files:

- Added configure options for highscores location and default resolution
- Option to turn on/off grid lines
- Released as trackballs v0.7.0

25 Feb 2003; Mathias Broxvall <matbr@home.se>, various files:

- Fixed bug with modulus of negative numbers
- Fixed fatal bug crashing the editor
- Map is now drawn in back-to-front order.
- Added level option to scale maximum jump height
- Fixes in configure.ac and Makefile.am (thanks Bernhard)
- Released as trackballs v0.7.1

28 Feb 2003; Mathias Broxvall <matbr@home.se>, various files:

- Translation of whole map in editor
- Possibility to automatically make hills, mountains in editor.
- Support from semitransparent walls/ground.        
- Added API to alter spike/platform speeds after creation.        
        
28 Feb 2003; YP, ball.cc, glHelp.cc, glHelp.h

- Optimised drawing of spikes
        
06 Mars 2003; Mathias Broxvall <matbr@home.se>, various files:

- nogrid flag
- support for editing all corners in a region
- Questions for saving/quiting in editor
- Saving/loading settings
- Made sure correct timedelta (instead of 1/fps) is used everywhere
- guile function (play-effect "name.wav")
- guile functions to alter cells (flag, height, velocity)
- added animator objects (animator, animator-value)
- ctrl-j in editmode makes flattens cell
- Made sure keyboard works in all menus
- Fixed a bug with the starting viewpoint
- Alternative path (~/.trackballs/levels) to .set, .map and .scm's
- Some optimisations in Ball::physics
- scriptable camera angle
- API function (set-texture anim texture-name)
- Added path to bonuslevel in lv3
- Added "extra life" modpill
- Moved translucent effects from ball::draw to stage 2.
- Holding down mouse no longer works for jump
- Released as trackballs v0.8.0

08 Mars 2003; Sam Listopad <samlii@users.sourceforge.net>, various files:

- Changes to compile on win32's mingw toolchain. (GCC)
- Moved directory finding logic to main to allow for .scm's in the 
          share/ice-9 directory.
- Added ./share to the list of checked directories
- Make current directory . if no directory breaks found in arg[0].

09 Mars 2003; Mathias Broxvall <matbr@home.se>, various files:

- In editor: ctrl-shift-{u,h,m,k,j} flattens a [region of] cells
- Added parameters and smooth transitions to fog.
- Replaced old slalom map with a new better one
- Changed default color of sign's depending on light and fog settings.

10 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added "pause" mode during game. Mapped to 'p' or 'P' key.
          A new statusGame -> statusPaused. Just draw the string 'Paused'.
- Added cactus object (cactus.{cc|h} + the definition in guile)
- Added a new level for my tests (hxtst) in share/levels/ (with the
            cactus at the place of Mr Black)
          TODO: the cactus is hugly! It's not what it was supposed to be!

11 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added a "darken" effect in pause-mode
- Added flags for allowing to draw cell's lines one by one
          (like the CELL_NOGRID, but specific for each side)
- Added edition for line drawing (UP, DOWN, LEFT and RIGHT with
          CTRL and SHIFT for NORTH, SOUTH, EAST and WEST).
          TODO: keys are bad mapped (north is not the intuitive one)

11 Mars 2003; Mathias Broxvall <matbr@home.se>, various files:

- New "splash" effect when going into acid
- Fixed compilation problem with wrong path to SDL/SDL_image
- Changed behaviour when dying within acid
- Applied patch for highscores from Bernhard Kaindl
- New calculations for which cells to draw in map::draw
- Renamed levels/con.set to levels/contrib.set
        
11 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added support for textures for cells without flags.
- Added texture edition through a new menu "textures"
- Corrected menu area to take in count the new menu "textures"
- Added teleport object (src/teleport.*), and it's definition
          in guile (add-teleport pos_x pos_y dest_x dest_y radius).
- Added a test teleport in level 'hxtst'.
- Changed the keys for texture selection for cells. Now it is
          CTRL+arrow-keys instead of arrow-key. It allow to move in the
          map in "Textures" mode.
        
11 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Corrected a bug in texture-loading in cell::load
- Improved cactus appearence (spikes)
- Cactus can now be killed if spikes activated.
          TODO: remove the cactus object from available entities.

11 Mar 2003; Ari Pollak <ari@debian.org>:

- Cleaned up bufferoverflow patch, no need for memset() since
          snprintf() always leaves a trailing \0 even if string is truncated

13 Mars 2003; Mathias Broxvall <matbr@home.se>, various files:

- Applied a bufferoverflow patch (plus some own buffer overflow checks)
- Changed SettingsMode so that mouseSensitivity can be 0.0
- Use float instead of real in cells to reduce footprint by 2megs.
- Created new "water" feature.         
- Changed viewed cell info in editor to be dependend on current 
          Menu choise (height,waterheight,velocity etc)
- Added fountain objects
- Modified water alpha to be dependent on depth
        
13 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added birds in the game (bird.*). Also added in guile. No animation
          nor nice shape for the moment.
- Allowed cactus to kill Mr Black. Updating level 'hxtst'.
- Killing cactus now gives points
- Birds now kill balls, and can be killed by balls with spikes.
- Introduced a delay before bird restart
- Killing a bird gives a small amount of points

14 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Included patch from Samuel Listopad (time management through SDL)
- Corrected a bug that allows to kill a cactus multiple times
- Added sound definition/play for catcus and bird die
- Corrected an uninitialized variable in sound.cc
- Added sound for spikes rising. If near enough, spikes now
          generate a sound at rising time.
- Added new functions in 'sound.*' which allow to control the
          volume of effects played.
- Changed the sound of spikes in order to make a progressive
          volume regards to the distance to the ball.
- Added sideSpike. Same than 'spike', but coming from the side.
          Same guile definition, with an additionnal 'int' for the side.
          1:X+, 2:X-, 3:Y+, 4:Y-.
          Still some troubles with collisions with balls...
- Added object colorModifier. Allow to alter the color of a cell.
          You can select RED (1), GREEN (2) or BLUE (3) component, or all (0).
          Color changes between a min and max value, with a given frequency
          and a phase. See level 'hxtst' for an example.

14 Mar 2003; Ari Pollak <ari@debian.org>:

- share/Makefile.am, share/trackballs.6:
    - Move man page to section 6, since trackballs is a game
- configure.ac:
    - Check for libGLU seperately, since certain distributions package
         libGL and libGLU seperately.

17 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added snapshots during game (only). Press "Print" key to generate
          a snapshot_xxx.ppm in the current directory. TODO: create an other
          format than PPM (big!), put snapshots elsewhere ? Allow snapshots
          everywhere (not only during game, i.e. to make nice documentation
          with pictures...)

17 Mars 2003;  Mathias Broxvall <matbr@home.se>, bird.cc birh.h wings.png

- New textured graphics for birds
- Moved bird drawing to stage 2 so that their transparent parts will not 
          other objects.

18 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Changed 'bindTexture' in 'glHelp.cc'. If the texture is not
            found in the pre-loaded list, the texture is loaded and inserted
            in the list. Also added a test if too much textures are loaded
            (as it is a static array).
- Added a name to the window of trackball (in mmad.cc). TODO: correct
            the 'configure' in order to generate variables PACKAGE and VERSION
            in the config.h, which can be use to refer to ourself.

18 Mars 2003;  Mathias Broxvall <matbr@home.se>:

- Made player sensititive to being under water (runs out of oxygen)
- Added new ball modification "float" together with modpills for it
- Fixed define of PACKAGE and VERSION to trackballs
- Added version commandline option (--version) and display version in
          the menuMode

18 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Changed name of the SDL window in order to use PACKAGE and VERSION
- Added a '#include "../config.h" in 'general.h' (only if the
          tag 'HAVE_CONFIG_H' is set) in order to exploit configuration
          given by the 'configure' inside the code (no use for the moment,
          but it may be usefull if we plan to make a robust game. In
          particular I coded a soft and for Solaris _many_ things are
          a little different... Using the config.h allow to switch parts
          of the code to handle particular cases...)

20 Mars 2003;  Mathias Broxvall <matbr@home.se>:

- Added texture coordinates to cells, drawing of textures.
- Rewrote manipulation of textures in editor. 
- Automatic translation of texture indices in map
- Corrected all references of textures to be relative to loaded textures
- New "rotational friction" to limit rotation speed when on ice, water etc. Might
          reduce the top speed slightly on other surfaces. Check that all maps still work.
- Added new splashes caused by rotation in water. Eg. "swimming"
- Note. now only saving texture coords if texture is set or flags nonzero.
- New commandline option "--touch" which can be used to update maps
- Added a "stargate" like appearance to teleporters        

21 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Changed secondary color for teleport. Nicer effect.
- Added map-is-transparent in my test level 'hxtst'.
- Added a vertical push for the fountain. If player comes
          just above the fountain, he is propulsed like a jump.
          Vertical force is proportionnal to fountain's strength.
- Corrected '--touch' option: the map name to touch was not
          converted in BASEDIR/name format, so touching a map without
          being in the map dir (or given the full path) was not possible
- Corrected sound volume for spikes. Max is now 2/3 of the real
          max volume.
- Updated the README.html to include my objects.

21 Mars 2003;  Mathias Broxvall <matbr@home.se>:

- Correct rotation for birds. Also added flag *bird-constant-height*
- Corrected '--touch' so that it *also* works with absolute filename
- Fixed bug with texture coordinates of compressed maps (not all coords are saved
          to make compression more efficient)

21 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added a help1_*.png in share/image, preparation more more
          help screens.
- Added support for help0, help1 and text in helpMode.{cc|h}
- Added pictures of cactus, teleport and bird in help1.
          Mathias: please edit help1_*.png because I don't have your
          font to draw corresp. text.
- Corrected collisions for sideSpike. Seems to work fine.
          To be more tested.

22 Mars 2003;  Mathias Broxvall <matbr@home.se>:

- Fixed bug with floating in shallow water
- Changed push of fountain to take velocity (direction) of fountain into effect.        
        
25 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added a new feature in edit mode: using TAB key with a selection
          in 'Edit heights' mode "smooth" all the cells in the selection.
          Each corner of each cell is modified in order to create a smooth
          continuity. Usefull when building large smooth areas.
- Pressing TAB without selection adjust the center height to the
          average value of corners.
- Corrected a bug in editMode.cc: 'hill' variable was not initialized
          generating 'core dump' in some situations.
- Added CTRL+TAB key. Flatten the current cell (height is the average
          value of the 4 corners). Useful for putting objects in complex
          levels on a flat cell.
- Added level 'snowbord'. Not finished, but playable.
- Updated a little bit the 'help1' screen.
- Added some new features in levels (lv1, lv2 and lv5) (resp.
          sidespikes, cactus and birds).
- Removed an old 'debug' display in sidespike.

26 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added heightModifier.{cc|h}. Allow to modify the height
          of a corner of a cell, and the corresponding heights of the
          cells's corner which touch this corner (not very clear...).
          Allow to make "waving" ground. See 'hxtst' for an example.

27 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Improved heightModifier behavior. More flexible.
- Added a "wave" at end of level 'lv4' to reach goal (heightModifier
          feature)
- Improved 'Pause' mode behavior and look.
- The mouse pointer in 'menuMode' now "blinks" a little.
- Corrected a bug in *constant-height* for birds.

28 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added sparkle2d.{cc|h}. Generates sparkles in 2D mode.
- Added sparkles on the mouse pointer. Not sure it is very nice...

30 Mars 2003;  Mathias Broxvall <matbr@home.se>:

- Finished the "waterworld" level.
- Use constant value for water alpha (looks strange otherwise)

31 Mars 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Corrected a little bit the 'snowbord' level. It is now a little
          bit simpler (but a little only). PS: I finish this level loosing
          at most one life.
- Added the missing file 'share/image/glitter.png'.

31 Mars 2003;  Mathias Broxvall <matbr@home.se>:

- Some fixes to the snowbord level for different diffuculty levels
- Changed the sparkles in the main menu
- Trimmed some physics parameters
- Fixed a bug with overlapping translucent objects
- Releasing as trackballs v0.9.0
        
01 April 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added src/image.{cc|h} to handle RGBA image loading (used
          by font system).
- Added src/font.{cc|h}. Crash.

02 April 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Code no more generates crash. Font system still not available.
- First test of the font system. Just run the game and have
          a look at the first menu. Nothing else available for the moment.
- Font system is now functionnal, but minimalist. Have a look
          to the starting menu for some tests with the different modes
          available for drawing text. I'm working on text selection with
          the mouse, but still don't know how I will highlight selected
          text.

03 April 2003; Sam Listopad <samlii@users.sourceforge.net>:

        * src/Makefile.am, configure.ac:
        - Added checks for windows, and stuff to make Icons for windows
                  platform.
        * trackballsIcon.rc:
        - Added resource file to compile in Icons on windows platform.
        * src/sound.cc:
        - Made the playEffect respect the sfxVolume from settings in 
                  all cases.
        * src/mmad.cc
        - Set the window caption and icon before opening the window.

04 April 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Changed the Font:: api to make a more generic system.
- Added a second font object.
- Added generic functions to select the font to use and to
          access the font objects (hidden from user point).
- Changed tests exemples in first menu to use new API and
          the two available fonts.
- Added a third font for test purpose. Still some changes to
          be done for genericity purpose, and some functions to add.
- Added 'right' aligned texts
- Added 'set_color' functions to allow to modify base color
          and transparency for drawn texts (for each font).
- Selection of text with mouse is ok. Working on a way to
          highlight selected texts.
- Text modification mechanism ok.

05 April 2003;  Mathias Broxvall <matbr@home.se>:

- Changed some glPushX,glPushY followed by glPopX,glPopY to glPopY,glPopX 
        (where X,Y is Matrix or Attrib)
- Added a commandline option "--low-memory" which reduced memory usaged with ~15 megs

07 April 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Changed names for Font:: functions (more proper now).
- Corrected small bugs
- Added draw*SimpleText familly. Simple text management: the
          text is directly drawn, not stored, not animated... used for
          simple informative texts.
- Changed the framerate display in order to use drawSimpleText.
- Changed the version number in order to use drawSimpleText.
- Added stuff from 'font' in the help part (not finished)

08 April 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- First valid "pulse mode". Starting to replace some part of the
          texts with font system.
- Added some features to pulse mode (a redish glow behind selected
          texts [only on font0 at this time]).
- Changed font images from 1024x512 to 1024x256. Corrected font.cc
          to handle this. Font images are now 2x smaller on disk and in memory.

15 April 2003; Yannick Perret <yperret@bat710.univ-lyon1.fr>:

- Added 'delAllText()' in menuMode when leaving first menu screen
          (to prevent texts to stay displayed).
- First tests for 3D text drawing (ugly!)

21 April 2003; Ari Pollak <ari@debian.org>:

- Don't install the highScores file mode 666 if it is already owned
          by the games group

28 July 2003; Mathias Broxvall

- Added stdint to files included by general.h
- Fixed initial velocity bug after debugging help from Christophe Mermoud.
- Changed font texture to 512x256 since many gfx cards can't handle too 
          large textures. (TODO - fix other fonts)
        
08 August 2003; Mathias Broxvall

- Moved around enter2d/leave2d calls so that we only push/pop one level deep.
- Fixed bug with missing cursor in setupMode.cc by pushing GL_CURRENT_BIT
- Fixed random crashes on mga_dri accelerated displays caused by mga_dri referencing
        deleted textures when poping the ModelView matrix.
- Fixed potential bug with position of ball when jumping        

11 September 2003; Mathias Broxvall

- Turn off fog when gfx_details is 0

24 September 2003; Mathias Broxvall

- Releasing as trackballs v0.9.1

        
03 October 2003; Mathias Broxvall

- Adding some sound effects from Joshua Harding        

10 October 2003; Mathias Broxvall

- Added setting for 32bit colordepth
- Tuned fonts slightly
- Fixed bug/feature when entering player name containing whitespace
- Substituted old-style texts to new fonts in setupMode.cc, mainMode.cc, hofMode.cc, settingsMode.cc
- Got patch for settingsMode.cc/.h from Klaasvan Gend and added
        settings8.png from Dietrich.

26 October 2003; Mathias Broxvall

- Added joystick support (settings, settingsMode, calibrateJoystickMode, player, etc.)
- Replaced some more SDL_TTF calls with calls to textured font
- Generalised calls to draw mousepointer (sparkles, rotation etc. in all modes with mousepointer)
- Warping mouse after changing resolution
- Fixed glitch in colors of settings menu

21 November 2003; Mathias Broxvall

- Releasing as trackballs v0.9.2

24 November 2003; Mathias Broxvall

- Applying 0.9.2-sparkle.patch and 0.9.2-destdir-icons.patch from Gentoo

31 January 2004; Mathias Broxvall

- Implemented a new menusystem
- Option to modify steering in multiples of 45 degrees.
- Added a return button to the help screen
- New modpills "large" and "small"
- Fixed nicer phase in/out of ball mods
- Made debris inherit texture
- Added simple check for zlib in configure.ac
- New weather engine which can do snow or rain. (Purely decorative effect)

1 February 2004; Mathias Broxvall        

- Fixed bug in editmode with menu background
- Changed behaviour of pipes so that player can't enter too small pipes
- Started on a new levelset "the four seasons", two levels done.
        
7 February 2004; Mathias Broxvall        

- Made point size of Splash dependent on screen resolution
- Made resolution of Debris dependent on graphic settings
- Increased maximum number of fountain particles
- Fixed bug in editor.

9 February 2004; Mathias Broxvall

- Added Francek's levels (dn* aka "Strange")        
- Releasing as trackballs 1.0.0

24 Mars 2004; Mathias Broxvall

- Corrected small bug in fourSeasons_3.scm

2 April 2004; Samuel Listopad II

- Modified configure.ac to check for different OpenGL libs
        if making for a win32 host.
- Changed all "static" textures to go through glHelp.cc
        These include fonts, the dizzy texture, and any of the 
        others already using it.
- Added a resetTextures function to glHelp to reload all
        "static" textures on resolution change.  Win32 needed this
        to be able to change resolution.  Don't know if other
        platforms need it
- A couple of minor changes for win32 asthetics, and MS
        stupidities.

6 April 2004; Samuel Listopad II

- Modified mmad.cc to set HOME on windows to users application
        data directory when no HOME is set.
- Corrected some printouts and removed spurious ones.
- Use USERNAME enviroment variable on Windows when no USER
        set.
        
7 April 2004; Mathias Broxvall

- Applied small bugfix from sourceforge's bug tracker for uninitalized dx/dy 
        in player::tick.

6 June 2004; Mathias Broxvall:

- Cleaned up the TODO list
- Introduced new mod_nitro effect

?? June/July 2004; Yannick Perret:

- Made the fontsystem use png images instead of raw rgb's.

14 July 2004; Mathias Broxvall:

- Added true reflections to balls at highest graphics settings
- Option to disable mousesteering and the grabbing of the mouse
- Descriptive signs after taking modPills / savepoints
- Small performance fixes

11 December 2004; Mathias Broxvall:

- Added displaylists to the mapdrawing, approx. 3x speed increase on my computer
- Replaced some 2D graphics SDL_Surface with cached textures. Huge speed increase.
- Added visibility (onScreen) test for all objects before calling their draw routine.
- New specular highlighting of (some of) the balls.
- Disabled antialiasing of the cell lines for now, does not work good with the changed map drawing code.

9 January 2005; Ari Pollak <ari@debian.org>:

- Fix compile error when building on amd64/gcc-4.0

10 January 2005; Mathias Broxvall

- Disabled / simplified drawing of fountain for the fountain when simple graphic settings 

11 January 2005; Ari Pollak <ari@debian.org>:

- Apply modified patch from Steve Kemp <skx@steve.ork.uk> to 
          fix some buffer overflows
        
29 January 2005; Mathias Broxvall:

- Adding gettext support for internationalization efforts. Approx 80% of i18n strings extracted.
- Started (partial) swedish translation of extracted strings
- Started rewriting menuMode to better work with i18n strings


06 February 2005; Mathias Broxvall:

- Added swedish characters to font.png
- Fixed bug with 8bit ascii values in font.cc
- Completed 95% of swedish translation
- Fixed the boundingbox bug

19-22 February 2005; Mathias Broxvall

- Added load/save/open/new etc. commands in editor
- Integrated editor into the normal menus.
- Creating default script files when creating new maps.
- Rewrote most game modes to use texts instead of image for i18n support
- Removed some images no longer in use 
- Made the gui slightly more consistent in eg. hofMode.
- Finally fixed the "fall through ground" bug. Implemented "onRemove" for pipe's and pipeConnectors
        so that on restart the old (now deleted) objects where not used again inside Ball::physics
- Fixed problem compiling for slackware by hardcoding extra check under -L/usr/X11R6/lib 

2 March 2005; Ari Pollak <ari@debian.org>:

- Apply modified patch from Ulf Harnhammar <metaur@telia.com> to prevent
          a crash when the environment variable USER=%n%n%n%n%n%n or similar.

2 March 2005; Mathias Broxvall:

- Disabled splashes from water/acid when playing under gfx details low or minimalisitc.

4 March 2005; Mathias Broxvall:

- Releasing as trackballs v1.1.0

5 March 2005; Ari Pollak <ari@debian.org>:

- Fixed some build problems after configuring with --disable-nls

7 March 2005; Mathias Broxvall:

- Added new language (french) submitted by Guillaume Bedot. 

2 April 2005; Mathias Broxvall

- Added checks against symlinks whenever opening/creating a file in write mode. I _believe_ that this fixes 
        the security problem with symlinks and a trackballs that's GID'ed.
- Replaced all sprintf with snprintf (with suitable size) as a precaution against buffer overflows.
- New configure flag "--with-broken-snarf" that fixes a problem with solaris and guile 1.6.0

6 April 2005; Mathias Broxvall

- Allow '~' argument for --with-highscores configure argument. Allows using highscore files on a per user basis.
        
14 May 2005; Mathias Broxvall

- Finally I have internet access at home again!
- Added a test screen when switching resolutions and asks users if 
        it is ok
- Introduced two togglefullscreen calls in a row when starting a
        game, this fixes a bug with SDL_WarpMouse on somesystems. Check to
        see that it doesn't mess anything up for
        others?
        

13 November 2005; Mathias Broxvall

- New webpage for trackballs
- Fixed critical bug affecting gentoo + SDL 1.2.8
- Releasing as another minor release, Trackballs v1.1.1, just to get started again.

15 November 2005; Ari Pollak <ari@debian.org>

- Fix crash and/or infinite loop if initializing the screen
          resolution has failed
- Disable useMipmaps since gluBuild2DMipmaps() currently segfaults
          using the X.org r200 DRI driver.
- Fix dimensions of screenResolutions[][] in settingsMode.cc

16 July 2006; Mathias Broxvall

- (Re)moved level boxofun.* in favour for bx.*

4 August 2006; Mathias Broxvall

- Added new level sets by Attila Boros
- Use 'f' key to change between fullscreen/windowed mode and
        capslock key to toggle grabbing and showing of cursor.
        
6 August 2006; Mathias Broxvall

- Implemented new moving backgrounds for main menu screen
- Fixed a bug with repeated keystrokes 
- Added support descriptive text for each levelset
- Added custom backgrounds in the setup game mode for each levelset
- New sandbox difficulty mode (no lives are lost)
- Releasing as trackballs v1.1.2

18 August 2006; Mathias Broxvall

- Added two new songs by Attila Boros
- New script commands set-song-preference, force-next-song and 
        clear-song-preferences to allow choosing specific songs for levels.

23 September 2006; Mathias Broxvall

- General cleanup of guile.cc and adding a few new functions
- Updated level castle4 script from patch by Attila
        
17 May 2007; Mathias Broxvall

- Implemented event callbacks on arbitrary animated objects
        triggering on death and tick events.
- Replaced depracated guile functions with the proper ones
- Implemented the "features" part of the map editor

25 May 2007; Mathias Broxvall

- Added a general interface for score and time bonus when objects
        are killed. 

23 June 2017; M Stoeckl
      
- Converted metadata files in repository to Markdown formatting
- Previous changes visible in git commit log
