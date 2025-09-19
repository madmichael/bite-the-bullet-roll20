# Bite the Bullet Roll20 Character Sheet - User Guide

## Table of Contents
1. [Getting Started](#getting-started)
2. [Character Creation](#character-creation)
3. [Using the Sheet](#using-the-sheet)
4. [Combat System](#combat-system)
5. [Characteristics & Advancement](#characteristics--advancement)
6. [Acts of Faith](#acts-of-faith)
7. [NPC Management](#npc-management)
8. [Troubleshooting](#troubleshooting)

## Getting Started

### Installation
1. Download `bite-the-bullet.html` and `sheet.json`
2. In your Roll20 game, go to Settings → Game Settings
3. Upload both files in the Character Sheet Template section
4. Select "Bite the Bullet" as your character sheet

### First Time Setup
1. Create a new character
2. Click "🎲 Generate Complete Character" for instant setup
3. Or manually fill in attributes and characteristics

## Character Creation

### Quick Generation
The **"Generate Complete Character"** button creates a fully functional character:
- Rolls all attributes (3d6 for Vigor/Presence/Faith, 2d6 for Sand)
- Generates Wild West name with nickname
- Selects random characteristics from core rulebook tables
- Provides starting weapon, armor, Lead, and money

### Manual Creation
1. **Attributes**: Roll or assign Vigor, Presence, Faith (3d6 each), Sand (2d6)
2. **Name**: Enter character name or use name generator
3. **Characteristics**: Fill in or use individual table roll buttons
4. **Equipment**: Add weapons, armor, and gear manually

### Wild West Names
Use the name generator for authentic period names:
- **Male Names**: Generate masculine frontier names
- **Female Names**: Generate feminine frontier names  
- **Random Gender**: Randomly select gender and generate name
- Names include first name, colorful nickname, and surname

## Using the Sheet

### Navigation
The sheet is organized into sections:
- **Header**: Character and player names
- **Generator**: Character creation tools
- **Attributes**: Core stats and saves
- **Resources**: Load, Reserve, Lead, Money
- **Characteristics**: Six character traits with tap system
- **Equipment**: Weapons, armor, gear, burdens
- **Acts of Faith**: Faith-based actions
- **NPCs**: GM tools for managing NPCs

### Mobile Use
The sheet is optimized for mobile devices:
- Single-column layout on phones
- Touch-friendly 44px+ button sizes
- Prevents iOS zoom on input focus
- Responsive design adapts to screen size

## Combat System

### Weapon Attacks
1. Click weapon **"Attack"** button
2. Damage is rolled automatically
3. Ammunition decreases by 1 (if applicable)
4. Results appear in chat with roll template

### Ammunition Management
- **Current Shots**: Automatically decreases on attack
- **Reload**: Click "Reload" button to consume 1 Lead and refill weapon
- **Lead Tracking**: Lead resource decreases when reloading

### Damage Resolution
1. Roll weapon damage
2. Apply tap bonuses (if used)
3. Subtract armor (if applicable)
4. Apply remaining damage to Sand
5. If Sand reaches 0, roll burden
6. If damage exceeds Sand, apply excess to attributes

### Save Rolls
Click attribute save buttons when needed:
- **Vigor Save**: Physical trauma, exhaustion
- **Presence Save**: Social pressure, fear
- **Faith Save**: Spiritual challenges, Acts of Faith

## Characteristics & Advancement

### The Six Characteristics
1. **Background**: What you know, skills, lifestyle
2. **Reputation**: How others see you
3. **Fortitude**: What anchors or drives you
4. **Foible**: Flaws, compulsions, emotional scars
5. **Issue**: Your burden, obsession, or flaw
6. **The Bond**: What ties your group together

### Tapping System
- Click **"Tap"** button to use characteristic
- Adds rank to damage or saves
- Tracks uses for advancement
- **Restriction**: Can't tap same characteristic until using two others

### Advancement
- **Uses Required**: Rank × 10 (Rank 1 = 10 uses, Rank 2 = 20 uses, etc.)
- **Advancement Roll**: Click **"+"** button when ready
- **Success**: Roll d6 > current rank to advance
- **Failure**: Reset uses to 0, try again after more uses

### Table Rolls
Each characteristic has a **"🎲 Roll [Type]"** button:
- Rolls on appropriate table from core rulebook
- Results appear in chat
- Use for inspiration or random generation

## Acts of Faith

### Faith Scale
Acts of Faith require Reserve (Inventory - Load):

| Scale | Reserve | Modifier | Examples |
|-------|---------|----------|----------|
| Trivial | 0 | +0 | Light candle, sense presence |
| Minor | 1 | -1 | Bless food, calm fear |
| Moderate | 2 | -2 | Heal wounds, repel spirits |
| Major | 3 | -3 | Banish demons, call lightning |
| Legendary | 4+ | Special | Resurrect dead, stop time |

### Using Acts of Faith
1. **Check Reserve**: Must have required Reserve available
2. **Click Button**: Choose appropriate scale button
3. **Roll Faith Save**: Modified by scale difficulty
4. **Success**: Act manifests as described
5. **Failure**: Take d6 damage per Reserve level required

### Faith Damage
- Failed Acts of Faith cause damage
- Can be mitigated by tapping characteristics
- Applied to Sand first, then Faith attribute

## NPC Management

### Creating NPCs
**Manual Entry**:
1. Add new repeating NPC section
2. Fill in name, attributes, armor, attacks
3. Add notes and descriptions

**JSON Import**:
1. Paste JSON data in import textarea
2. Click "Import NPCs" button
3. NPCs automatically created from data

### JSON Format
```json
[
  {
    "name": "Bear",
    "attributes": {"vigor": 16, "presence": 6, "faith": 3, "sand": 12},
    "attacks": [{"name": "Claw", "damage": "1d6"}],
    "armor": {"physical": 0, "social": 0, "faith": 0},
    "notes": "Large wilderness predator"
  }
]
```

### NPC Combat
- Click **"Attack"** button for NPC attacks
- Damage rolled automatically
- Results appear in themed chat template

## Troubleshooting

### Common Issues

**Character Generator Not Working**
- Ensure JavaScript is enabled
- Refresh the page and try again
- Check browser console for errors

**Buttons Not Responding**
- Sheet workers may be loading
- Wait a few seconds and try again
- Refresh page if problem persists

**Mobile Display Issues**
- Rotate device to landscape if needed
- Zoom out if content appears cut off
- Use Chrome or Safari for best mobile experience

**Ammunition Not Tracking**
- Ensure weapon has "shots" value set
- Check that Lead resource is available for reloading
- Verify sheet workers are functioning

**Load Not Calculating**
- Check that equipment has "slots" values
- Verify sheet workers are active
- Manually refresh calculation by changing Vigor

### Performance Tips

**Large Character Sheets**
- Limit number of repeating sections
- Remove unused equipment entries
- Clear old burden/status entries when healed

**Mobile Performance**
- Close other browser tabs
- Use latest browser version
- Clear browser cache if sluggish

### Browser Compatibility

**Recommended Browsers**:
- Chrome (Desktop & Mobile) ✅
- Firefox (Desktop & Mobile) ✅
- Safari (Desktop & iOS) ✅
- Edge (Desktop) ✅

**Known Issues**:
- Internet Explorer: Not supported
- Older mobile browsers: Limited functionality

## Advanced Features

### Sheet Options
Access via Roll20 sheet settings:
- **Dark Mode**: Toggle dark theme
- **Show NPC Section**: Hide/show NPC tools
- **Auto-Calculate Load**: Enable/disable automatic load calculation
- **Show Advancement Hints**: Display advancement readiness indicators

### Keyboard Shortcuts
- **Tab**: Navigate between form fields
- **Enter**: Activate focused button
- **Space**: Toggle checkboxes
- **Escape**: Close modals/dropdowns

### Data Export/Import
- Character data stored in Roll20 character sheets
- NPC data can be exported from Foundry VTT system
- JSON format allows cross-platform compatibility

## Getting Help

### Resources
- **Core Rules**: See `Docs/Bite-the-Bullet-Rules.md`
- **Project Documentation**: Check README.md
- **FoundryVTT System**: [GitHub Repository](https://github.com/madmichael/bite-the-bullet-foundryvtt)

### Support
- Check browser console for JavaScript errors
- Verify Roll20 sheet is latest version
- Test in different browser if issues persist
- Report bugs with specific steps to reproduce

---

*"The world didn't end with a bang. It just...dried up."*
