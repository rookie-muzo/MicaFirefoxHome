# MicaFox

<img src="https://github.com/user-attachments/assets/b2e34840-907a-4d0c-b83d-cf6b58a4ece4" alt="image" width="700"/>

Firefox CSS theme to match Windows 11 with transparent new tab page and Mica effect

Tested working on Windows 11 25H2.

I sorta slopped this one together just for myself so don't expect many updates.

## Setup Instructions

### Step 1: Download and Install

1. Click the `Code` button at the top of this page
2. Click `Download ZIP`
3. Extract the ZIP file
4. Copy the `chrome` folder to your Firefox profile folder
   - Open Firefox and type `about:profiles` in the address bar
   - Click "Open Folder" next to your profile (the one in use)
   - Copy the `chrome` folder into that folder

### Step 2: Enable Required Firefox Settings

1. Open Firefox and type `about:config` in the address bar
2. Click "Accept the Risk and Continue"
3. Search for and set each of these to `true`:
   - `toolkit.legacyUserProfileCustomizations.stylesheets`
   - `widget.windows.mica`
   - `widget.windows.use-acrylic-effects`
   - `widget.windows.use-mica-effects`
   - `browser.tabs.allow_transparent_browser`

### Step 3: GPU Workaround (If Needed)

If the transparency isn't working, try this:

1. Go to `about:config`
2. Search for `gfx.webrender.compositor.force-enabled`
3. Set it to `true`

### Step 4: Install Mica For Everyone

1. Download and install [Mica For Everyone](https://github.com/minusium/MicaForEveryone)
2. Open Mica For Everyone
3. Add a new rule for Firefox:
   - Title bar Color: System
   - Set "Backdrop Type" to "Mica"

### Step 5: Restart Firefox

Close Firefox completely and open it again. The transparent new tab page with Mica effect should now be working.

## Requirements

- Windows 11
- Firefox browser
- Mica For Everyone (for the Mica effect)

## Notes

- The new tab page background will be transparent, allowing the Mica effect to show through
- The customize button on the new tab page is hidden by default
- If you don't see the Mica effect, make sure Mica For Everyone is running and configured correctly

## Preventing Mica Effect on Regular Websites

By default, websites with transparent backgrounds will also show the Mica effect through them. If you want to prevent this and only have transparency on the new tab page, follow these steps:

1. Open the `chrome` folder in your Firefox profile
2. Open `userContent.css` in a text editor
3. Scroll to the bottom of the file
4. Find the section that says "OPTIONAL: Make regular websites opaque"
5. Remove the `/*` at the start and `*/` at the end of that section (uncomment it)
6. Save the file and restart Firefox

To re-enable transparency on websites, add `/*` and `*/` back around that section (comment it out again).

You can also customize the background color in that section - change `#ffffff` to any color you prefer for light mode, and `#1a1a1a` for dark mode. 
