# DEFINITIONS #
 = define README = this .
 = define PLUGIN = any exstension that affects included software .

# AGREEMENT #
THIS AGREEMENT APPLIES TO ANY AND ALL INCLUDED FILES, DATA, SOFTWARE AND INFORMATION,

BY USING ANY OF THE INCLUDED FILES, DATA, SOFTWARE, OR INFORMATION,
YOU AGREE THAT:
THE AUTHOR, AND OTHER ASSOCIATES ARE NOT LIABLE FOR ANY DAMAGE THIS PROGRAM MAY CAUSE
TO THE USER'S COMPUTER, DATA, EMOTIONAL FEELINGS, OR OTHER PROPERTY,
THAT YOU WILL NOT REDISTRIBUTE OR ASSIST IN REDISTRIBUTING  ANY OF THE INCLUDED FILES WITHOUT 
EXPLICIT PERMISSION FROM THE ORIGINAL AUTHOR OR AUTHORS IF THERE ARE MORE THAN ONE,
AND SHOULD REDISTRIBUTE NOT ANY PORTION OF THIS SOFTWARE WITHOUT INCLUDING THIS README, UNLESS GIVEN 
EXPLICIT PERMISSIN TO DO SO FROM THE ORIGINAL  AUTHOR OR AUTHORS IF THERE ARE MORE THAN ONE :
THIS INCLUDES TRANSLATIONS AND CERTAIN PLUGINS. WHICH MAY BE PROVIDED OR SUPPORTED LEGITAMETLY AT A LATER TIME,
WILL NOT REVERSE ENGINEER OR ASSIST IN REVERSE ENGINEERING ANY PORTION OF THE INCLUDED DATA
AND AKNOWLEDGE THAT FAILURE TO ADHERE TO THESE CONDITIONS MAY RESULT IN PENALTIES OF ANY DEGREE
OF PERSONAL, INTERNATIONAL, OR LEGAL INFRACTION.

# INFO #

Nameless Sprite Editor is created entirely by Link12552 ,the author.
"A tool used to edit sprites and other data in Gameboy Advance games"

###### Requirements #
- .net framework 4.0 or better
- the included files to ALL stay in the same directory
- more than 20mb of RAM (should NOT be a problem)

###### Beta Status #
- This is a beta build
  - Turbo - charged manipulation engine ~1000% faster than NSE 1.X
       in other words: NSE 2.X is blazing fast! (ie. can open AND draw an ENTIRE! 16mb ROM ~ 2 sec!
  - Editor = done
  - Plugins in any .net language
  - 16 and 256 color
  - Perfect (MAX compression) Lz77! (Note: some data is given a 2 byte floating buffer)
  - more...

### 6/9/2011
- Still in alpha
  - Imports (*.nslx, *.bmp, *.png)
    - Support for 16 and 256 color palettes
    - Perfect image data loading (loads data from byte arrays)
    - Works with unlz exports (Error in unlz's exporting algorithm, it treats all sprites as 256 color)
    - Full *.nslx support
    - imported through NSE_Framework.IO
  - Exports (*.nslx, *.bmp)
    - Exports 16 and 256 color bitmaps
    - bitmaps physicaly written byte by byte
    - exports sprite libraries
    - exports all sprites in an editor control
    - exported through NSE_Framework.IO
 - NSLX (the new sprite library format *.nslx)
    - New hierarchy Library >> SpriteSets >> SpriteData
       - Library (string Origin, List<SpriteSets> Sprites)
       - SpriteSet (int width, int height, SpritePalette Palette, List<SpriteData> SpriteData)
       - SpriteData (byte[] Data, bool compressed)
    - Store an infinate amount of SpriteSets
    - Both 16 and 256 color in a single nsl
    - Lz compression (smaller file size)
    - Created through .net reflection using NSE_Framework.IO
- Lz functions handled by static class NSE_Framework.Data.Lz77
- Controls Editor.cs and SelectColor.cs added to NSE_Framework.Controls
- ShortCuts Changed
    - Scrolling zoom Ctrl+Scroll
    - Zoom in Ctrl++
    - Zoom in Ctrl+-
    - Palette Tab
    - Pencil P
    - Brush B
    - Fill F
    - Eyedropper E

### 6/17/2011
-Finnaly a useful plugin!
-Fixed a bug in the NSE applications nslx exporter.

### 7/10/2011
-BookMarks!!!
    - Core\\Settings.ini [NSE]
    - Example BookMark file provided
    - BookMark scripting there, but disabled, incomplete
    - No larger than 16mb support enabled

### 8/1/2011
-Support for 32MB roms
-Safety Repointing
-Advanced Repointing
-Palette Editing
-Import Palettes (ACT, PNG, BMP)
-Shows current color in editor
-Some cursors
-Better Color Selector
-BUG Fixes

### 8/6/2011
-Fixed a bug!

### 8/28/2011
!BETA!
-Undo(ctrl+z) and Redo(ctrl+shift+z)
-Color swaping (alternate or preserve)(ctrl or alt click in the palette editor)
-Dynamic cursors (change size with zoom and brush stroke)
-Drag bookmarks and folders around in the editor
-Some new bookmarks added (now around 90 total)
-NSE_Framework.IO.BookMark and NSE_Framework.IO.BookMarkTree now have a parent identifier
-Events added to editor and selectcolor controlls
-Slight speed increase
-NSE command line support (means you can "open with" gba files in NSE)
-Bugs squashed!
-Export All button in pokemon plugin
-Insert Image and Palette (Normal or Compressed)
-Edit>Palette

## 9/18/2011
-New Sprite button works, FINALLY!
-Open Sprite (opens indexed bitmmap, png, and nslx format)
-Can natively open *.nslx, *.bmp, *.png, *.gba (Settable via widows "open with")
-Checks for updates once a day (to disable change in settings.ini "LastUpdate = disable")
-Logs (Records opening, repointing, saving...)
-Fixed bug while minimizing.
-Fixed editting bounds bug.
-Drag files into main window to open.

## 10/12/2011
-Fixed update system
-Points to my new site (http://lastlink.tk)
-New plugin features
 -Host.NewImport()... Create custom content importers for NSE 2.X
 -Host.NewExport()... Create custom content exporters for NSE 2.X
 -Host.NewEditor()... Create a standard editor window
 -Host.currentEditor... Points to the current editor
-A plugin menu
-Includes ClassicExchange plugin. (Adds support for NSL [classic] files)
-Fixed a bug with the stroke menu causing a loss-of-focus
-Fixed a "navigate" bug

## 12/1/2011
-Minor Tune-ups
-Some small speed increases

## 12/21/2011
-Bug fixes
-Safety-saving
-More visible cursor
-Fixed issues with the NSE_Framework
-Added a CkeckLz77 function to the Framework

## 12/22/2011
-FOOTPRINTS!!!! new plugin.
-footrpint editor excepts an INI
-Added a set property to NSE_Framework.Data.GBAcolor.Color

## 1/6/2012
-Fixed an annoying bu that prevented opening images
-Color match alpha added as a beta

## 2/10/2012
-Faster draw code
-Much better memory usage
-Slightly larger navigate window
-Faster code in place for next version
-ExtendedPictureBox control added
-Fixed the same bug, that I thought I had fixed last time
-EDIT: fixed a bug... Yes, I know that the version now shows up weird on the strat page, live with it!

## 3/13/2012
-Worked on a bug
-Logs can be disbaled through the LogFiles=false command in the settings.ni
