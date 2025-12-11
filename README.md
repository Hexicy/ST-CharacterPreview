# Character Details Popup

SillyTavern extension that displays character information in a pop-up box when clicking character cards.

## Fork Notes

First off, I have no idea what I'm doing. At this moment, I don't know how to code. But, with the help of ChatGPT, I was able to change the code to add some more features that I wanted from this really great extension. For example, I was able to change the code to allow CSS to load on the creator notes tab. 

Just to be clear, everything I've done was thanks to Chat GPT and the awesome work of the original author. If you want to support anyone, do it to the original creator.

Anyways, I'm probably going to keep using ChatGPT to modify the code and whatnot in my attempts to make some of my ideas for this extension a reality.

## Changes:

* Made the "Creator Notes" dropdown able to display CSS so that it's no longer unreadable when viewing the creator Notes that use CSS.
* Fixed the issue of the text/images going past the screen on mobile. It'll now be properly displayed within the device's screen.
* Gave the "First Message" dropdown the ability to display all of the character's available greetings.
* Because of the change above, I changed the "First Message" dropdown to instead be called "Greeting" or "Greetings" depending on the amount of available greetings.
* Markdown is now visable in creator notes.
* The "Start chat" and "Close" buttons will no longer get covered on mobile.
* Option in settings to allow the individual user to toggle which dropdowns are visable in the popup, what order they appear in, and which dropdown opens automatically.

I'll be working on trying to add more to this extension in the future. I currently plan on trying to add more user configuration to the settings, more mobile support/features, and ensure that this extension is as user-friendly as possible.

Just to quickly clarify, I am a mobile user so rest assured that, if you're on mobile, this extension works. However, I am a mobile user only so I have no idea how this extension works on PC. If you use this extension on PC, please tell me how it goes.

As always, if you notice any issues, please tell me so that I can fix them. By me, I mean ChatGPT. Even though you could do it yourself, please tell me so that I can fix it for everyone else. Anyway, enjoy the extension!

# Original Author's Notes:

## Author's Note

My biggest complaint about SillyTavern has long been the fact that clicking on a character card to examine it immediately launches a chat. This plugin is my attempt to circumvent this issue by creating a popup box with options to start a chat. This way I can look at a character properly before I make my decision. I made additional adjustments so that it works with lazy loading, as I have 1,000+ cards (I'm a data hoarder leave me alone) and so lazy loading is a requirement for my container not to overload itself on every refresh.

I hope this works for others. No promises on mobile functionality. I tested this in Firefox 1.44 x64 on Windows 11, I do not have the time or patience to test it elsewhere.

Please consider [supporting me](https://ko-fi.com/tydorius) if you like what I'm doing.

## Features

- Character details displayed in popup before starting chat
- Collapsible sections for spoiler-sensitive content
- Markdown rendering for description and first message fields
- Full character data: name, avatar, description, first message, scenario, personality, creator notes, example messages
- Theme integration with customizable colors and blur effects
- Bulk edit mode compatibility
- Lazy loading support for large character libraries
- Character panel state preservation when closing popup
- Keyboard shortcuts: Escape to close, SHIFT+click to bypass popup

## Installation

### Via Extension Manager

1. Open SillyTavern Extensions menu
2. Click Install Extension
3. Enter repository URL
4. Click Save

### Manual Installation

1. Copy extension folder to `SillyTavern/public/scripts/extensions/third-party/`
2. Restart SillyTavern

## Usage

Click any character card to open the preview popup. Description section expands by default. Other sections (First Message, Scenario, Personality, Creator Notes, Example Messages) remain collapsed.

**Actions:**
- Click Start Chat to begin conversation
- Click Close, press Escape, or click outside popup to dismiss
- Character panel remains open after closing popup
- Hold SHIFT while clicking character card to bypass popup and start chat directly

## Configuration

Access settings via Extensions panel. Available options:

### Display Settings
- Box width and height
- Content width
- Padding and border radius
- Image maximum height
- Responsive breakpoint

### Colors & Effects
- Overlay opacity
- Font color (theme or custom)
- Background color (theme or custom)
- Background opacity
- Blur strength
- Primary and secondary button colors (theme or custom)

## Compatibility

- SillyTavern 1.13.4 or higher
- Compatible with all SillyTavern themes
- Supports lazy loading configuration (lazyLoadCharacters: true)
- Works with user profile directories

## Technical Details

- Type: UI Extension
- Loading order: 100
- Files:
  - `manifest.json` - Extension metadata
  - `index.js` - Main logic
  - `style.css` - Styling
  - `settings.html` - Configuration UI

Uses ES6 modules, SillyTavern API imports, and marked.js for markdown rendering.

## License

AGPL-3.0
