# Bite the Bullet - Roll20 Character Sheet

A comprehensive Roll20 character sheet implementation for the **Bite the Bullet** RPG system, providing full feature parity with the FoundryVTT version while being optimized for Roll20's platform.

## 🤠 Features

### Core Functionality
- **Complete Character Management**: All attributes, characteristics, resources, and equipment
- **Automated Systems**: Ammunition tracking, reload mechanics, inventory calculations
- **Character Generator**: One-click complete character creation with Wild West names
- **Tap System**: Full characteristic tapping, use tracking, and advancement mechanics
- **Acts of Faith**: Scaling faith-based actions with reserve requirements
- **Mobile-First Design**: Responsive layout optimized for all devices

### Advanced Features
- **NPC Management**: JSON import system compatible with FoundryVTT data
- **Roll Templates**: Beautiful, themed roll outputs for all roll types
- **Table Integration**: One-click rolls for characteristics and equipment
- **Dark Mode Support**: Toggle between light and dark themes
- **Cross-Platform**: Works on desktop, tablet, and mobile devices

## 🎯 Quick Start

1. **Upload to Roll20**: Upload `bite-the-bullet.html` and `sheet.json` to your Roll20 game
2. **Generate Character**: Click "Generate Complete Character" for instant setup
3. **Start Playing**: Use weapon attacks, tap characteristics, and perform Acts of Faith

## 📋 Character Generation

The sheet includes comprehensive character generation based on the core rulebook:

### Attributes
- **Vigor**: 3d6 (Endurance, strength, reflexes)
- **Presence**: 3d6 (Charisma, mental tenacity, grace under pressure)  
- **Faith**: 3d6 (Spiritual composure, manifested will)
- **Sand**: 2d6 (Determination, mental stamina, morale)

### Wild West Names
Authentic period names with over 200 combinations:
- **First Names**: Period-appropriate male and female names
- **Nicknames**: Colorful Wild West monikers like "Dead-Eye" and "Lightning"
- **Last Names**: Common frontier surnames

### Characteristics
Random generation from core rulebook tables:
- **Background**: Mine-born, Drifter, Ex-preacher, Scout, etc.
- **Reputation**: Shot Wyatt at sundown, Hex-touched, Cold-eyed killer, etc.
- **Fortitude**: Justice above all, Blood oath, Grace under fire, etc.
- **Foible**: Short fuse, Haunted by dreams, Never backs down, etc.
- **Issue**: Craves meaning, Marked by prophecy, Addicted to risk, etc.
- **The Bond**: Shared group characteristic (The Pact, The Ledger, etc.)

## ⚔️ Combat & Equipment

### Weapons System
- **Ammunition Tracking**: Automatic shot counting with visual indicators
- **Reload Mechanics**: Consume Lead to reload weapons
- **Weapon Traits**: AoE, Melee, Concealable, etc.
- **Range Bands**: Personal, Close, Medium, Long

### Armor & Protection
- **Physical Armor**: Protection against physical damage
- **Social Armor**: Protection in social conflicts  
- **Faith Armor**: Supernatural protection

### Inventory Management
- **Load Calculation**: Automatic calculation based on equipment slots
- **Reserve System**: Available capacity for Acts of Faith
- **Burden Tracking**: Status effects that consume inventory slots

## 🙏 Acts of Faith

Faith-based actions with scaling difficulty and effects:

| Scale | Reserve | Modifier | Examples |
|-------|---------|----------|----------|
| Trivial | 0 | +0 | Light candle, hear whisper |
| Minor | 1 | -1 | Bless food, calm fear, detect spirits |
| Moderate | 2 | -2 | Heal attributes, repel spirits, vision |
| Major | 3 | -3 | Banish creature, call down fire |
| Legendary | 4+ | Special | Bring back from grave, stop time |

## 🎲 Characteristic System

### Tapping Characteristics
- Add characteristic rank to rolls or damage
- Track uses for advancement
- Restriction: Can't tap same characteristic until using two others

### Advancement
- **Rank 1→2**: 10 uses, then roll d6 > current rank
- **Rank 2→3**: 20 uses, then roll d6 > current rank  
- **Rank 3→4**: 30 uses, then roll d6 > current rank
- Continue pattern for higher ranks

## 👥 NPC Management

### JSON Import System
Compatible with FoundryVTT NPC data format:

```json
[
  {
    "name": "Bear",
    "attributes": {
      "vigor": 16,
      "presence": 6, 
      "faith": 3,
      "sand": 12
    },
    "attacks": [
      {"name": "Claw", "damage": "1d6"},
      {"name": "Bite", "damage": "1d8"}
    ],
    "armor": {
      "physical": 0,
      "social": 0,
      "faith": 0
    },
    "notes": "Large predator",
    "tags": ["beast"]
  }
]
```

### NPC Features
- **Attribute Management**: Vigor, Presence, Faith, Sand
- **Attack Tracking**: Multiple attacks with different damage
- **Armor Values**: Physical, Social, Faith protection
- **Notes & Tags**: Descriptive information and categorization

## 📱 Mobile Support

### Responsive Design
- **Mobile-First**: Optimized for 320px+ screens
- **Touch-Friendly**: 44px minimum button sizes
- **Single-Column**: Mobile layout prevents horizontal scrolling
- **Font Optimization**: Prevents iOS zoom on input focus

### Cross-Platform Testing
- ✅ Chrome (Desktop & Mobile)
- ✅ Firefox (Desktop & Mobile)  
- ✅ Safari (Desktop & iOS)
- ✅ Edge (Desktop)
- ✅ Android Chrome

## 🎨 Theming

### Wild West Aesthetic
- **Typography**: Cinzel serif headers, Crimson Text body
- **Color Scheme**: Warm browns and tans (#8b4513, #a0522d)
- **Visual Elements**: Leather textures, weathered borders
- **Dark Mode**: Alternative color scheme for low-light gaming

### Roll Templates
Themed output for all roll types:
- **Damage Rolls**: Prominent damage display with ammunition info
- **Save Rolls**: Clear success/failure indication
- **Tap Results**: Characteristic usage and advancement tracking
- **Acts of Faith**: Success/failure with appropriate messaging
- **NPC Attacks**: Quick combat resolution

## 🛠️ Technical Details

### Roll20 Integration
- **Sheet Workers**: JavaScript automation for calculations
- **Roll Templates**: Mustache templating for chat output
- **Repeating Sections**: Dynamic inventory and NPC management
- **User Options**: Customizable sheet behavior

### Performance Optimization
- **Efficient Calculations**: O(1) lookups where possible
- **Memory Management**: Minimal DOM manipulation
- **Load Time**: < 3 seconds on mobile 3G
- **Battery Impact**: Minimal on mobile devices

### Accessibility
- **Semantic HTML**: Proper heading structure and labels
- **Keyboard Navigation**: Full keyboard accessibility
- **Screen Readers**: ARIA labels and descriptions
- **Color Contrast**: WCAG AA compliant contrast ratios

## 📚 Documentation

### User Guide
See the in-sheet instructions and tooltips for detailed usage information.

### Developer Notes
- **Architecture**: Single HTML file with embedded CSS/JavaScript
- **Data Format**: Compatible with FoundryVTT system data
- **Extensibility**: Modular sheet workers for easy modification

## 🤝 Contributing

This project maintains parity with the FoundryVTT system. When contributing:

1. **Test Thoroughly**: Verify functionality across browsers and devices
2. **Follow Patterns**: Use existing code patterns and naming conventions
3. **Document Changes**: Update README and inline documentation
4. **Mobile-First**: Ensure responsive design principles

## 📄 License

This character sheet is designed for use with the Bite the Bullet RPG system by Jason Hobbs and this Roll20 character sheet was created by Michael Spredemann.

## 🔗 Related Projects

- **FoundryVTT System**: [bite-the-bullet-foundryvtt](https://github.com/madmichael/bite-the-bullet-foundryvtt)
- **Core Rules**: See `Docs/Bite-the-Bullet-Rules.md`

---

*"You've got grit, ghosts, and something you believe in that's worth dying for. That's enough."*
