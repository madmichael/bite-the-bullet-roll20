# Bite the Bullet Roll20 Sheet - Testing Checklist

## Pre-Upload Testing

### File Validation
- [ ] `bite-the-bullet.html` - Complete character sheet
- [ ] `sheet.json` - Roll20 configuration file
- [ ] `README.md` - Project documentation
- [ ] `USER-GUIDE.md` - User instructions
- [ ] `sample-npcs.json` - Example NPC data

### HTML Validation
- [ ] Valid HTML5 structure
- [ ] All form elements have proper `name` attributes
- [ ] Roll buttons have correct `value` attributes
- [ ] Repeating sections properly structured

## Roll20 Integration Testing

### Sheet Upload
- [ ] Upload `bite-the-bullet.html` and `sheet.json` to Roll20
- [ ] Select "Bite the Bullet" as character sheet template
- [ ] Create new character to test sheet loads

### Basic Functionality
- [ ] Character name and player name inputs work
- [ ] Attribute inputs accept numbers and calculate properly
- [ ] Resources auto-calculate (Load, Reserve, Inventory)
- [ ] All buttons are clickable and responsive

## Character Generation Testing

### Complete Generation
- [ ] "Generate Complete Character" button works
- [ ] All attributes populated (Vigor, Presence, Faith, Sand)
- [ ] Character name generated with nickname format
- [ ] All characteristics filled from tables
- [ ] Starting equipment added (weapon, armor, lead, money)

### Individual Generators
- [ ] "Roll Attributes" generates 3d6/2d6 values
- [ ] "Roll Characteristics" populates all six characteristics
- [ ] "Generate Equipment" adds weapon and armor
- [ ] Name generators create authentic Wild West names

### Name Generation
- [ ] Male names generate masculine options
- [ ] Female names generate feminine options
- [ ] Random names vary between genders
- [ ] Names follow "First 'Nickname' Last" format

## Combat System Testing

### Weapon Management
- [ ] Weapon attacks roll damage correctly
- [ ] Ammunition decreases on attack (if weapon has shots)
- [ ] Reload button consumes Lead and refills ammunition
- [ ] Weapon traits display properly

### Roll Templates
- [ ] Damage rolls display with proper formatting
- [ ] Weapon name and ammunition status shown
- [ ] Roll templates have consistent styling
- [ ] Chat output is readable and informative

### Save Rolls
- [ ] Vigor/Presence/Faith save buttons work
- [ ] Save rolls compare against attribute values
- [ ] Success/failure clearly indicated
- [ ] Roll templates display properly

## Characteristic System Testing

### Tap Mechanics
- [ ] Tap buttons increment use counter
- [ ] Rank value applied as bonus
- [ ] Tapping restriction enforced (can't repeat until using others)
- [ ] Tap results display in chat

### Advancement System
- [ ] "+" buttons only work when sufficient uses accumulated
- [ ] Advancement rolls d6 vs current rank
- [ ] Successful advancement increases rank and resets uses
- [ ] Failed advancement resets uses to 0

### Table Rolls
- [ ] Each characteristic has working table roll button
- [ ] Rolls generate appropriate results from tables
- [ ] Results display in chat with proper formatting

## Acts of Faith Testing

### Faith Scale Buttons
- [ ] Trivial (0 Reserve, +0) button works
- [ ] Minor (1 Reserve, -1) button works
- [ ] Moderate (2 Reserve, -2) button works
- [ ] Major (3 Reserve, -3) button works

### Faith Mechanics
- [ ] Reserve requirement checked before allowing roll
- [ ] Faith saves modified by scale difficulty
- [ ] Success/failure properly determined
- [ ] Failure damage calculated correctly (d6 per Reserve level)

## Inventory System Testing

### Load Calculation
- [ ] Equipment slots automatically sum to Load
- [ ] Armor slots included in calculation
- [ ] Burden/status slots included
- [ ] Load updates when equipment changes

### Reserve Calculation
- [ ] Reserve = Inventory - Load
- [ ] Updates automatically when Load or Vigor changes
- [ ] Minimum value of 0 enforced
- [ ] Used for Acts of Faith requirements

## NPC Management Testing

### Manual NPC Creation
- [ ] Repeating NPC sections can be added
- [ ] All NPC attributes editable
- [ ] NPC attack buttons work
- [ ] NPC roll templates display correctly

### JSON Import
- [ ] Sample JSON data imports successfully
- [ ] All NPC attributes populated correctly
- [ ] Attack data imported properly
- [ ] Armor values mapped correctly (physical/social/faith)
- [ ] Notes and descriptions preserved

### NPC Combat
- [ ] NPC attack buttons roll damage
- [ ] NPC roll templates display name and attack
- [ ] Multiple attacks per NPC supported

## Mobile Responsiveness Testing

### Screen Sizes
- [ ] 320px (iPhone SE) - Single column layout
- [ ] 768px (iPad) - Responsive grid adjustments
- [ ] 1024px+ (Desktop) - Full multi-column layout

### Touch Interface
- [ ] All buttons minimum 44px touch target
- [ ] Form inputs properly sized for touch
- [ ] No horizontal scrolling on mobile
- [ ] iOS zoom prevention working

### Mobile Browsers
- [ ] Safari iOS - Full functionality
- [ ] Chrome Android - Full functionality
- [ ] Firefox Mobile - Basic functionality
- [ ] Samsung Internet - Basic functionality

## Cross-Browser Testing

### Desktop Browsers
- [ ] Chrome - Full functionality and performance
- [ ] Firefox - Full functionality
- [ ] Safari - Full functionality
- [ ] Edge - Full functionality

### Known Issues
- [ ] Internet Explorer - Not supported (document)
- [ ] Older browsers - Limited functionality (document)

## Performance Testing

### Load Times
- [ ] Sheet loads in < 3 seconds on desktop
- [ ] Sheet loads in < 5 seconds on mobile 3G
- [ ] No blocking JavaScript errors
- [ ] Smooth scrolling and interactions

### Memory Usage
- [ ] Character sheet uses < 50MB memory
- [ ] No memory leaks during extended use
- [ ] Repeating sections don't cause performance issues
- [ ] Large NPC imports handled efficiently

## Accessibility Testing

### Keyboard Navigation
- [ ] All form elements reachable via Tab
- [ ] Buttons activatable with Enter/Space
- [ ] Logical tab order maintained
- [ ] No keyboard traps

### Screen Reader Support
- [ ] Form labels properly associated
- [ ] Button purposes clear
- [ ] Heading structure semantic
- [ ] ARIA labels where needed

### Visual Accessibility
- [ ] Color contrast meets WCAG AA standards
- [ ] Text remains readable when zoomed to 200%
- [ ] Focus indicators visible
- [ ] No information conveyed by color alone

## Error Handling Testing

### Invalid Inputs
- [ ] Non-numeric values in number fields handled
- [ ] Negative values prevented where inappropriate
- [ ] Empty required fields handled gracefully
- [ ] Malformed JSON import handled with error message

### Edge Cases
- [ ] Zero values in attributes handled
- [ ] Maximum attribute values (18+) supported
- [ ] Large numbers of repeating sections handled
- [ ] Rapid button clicking doesn't break functionality

## Documentation Testing

### User Guide
- [ ] All features documented with examples
- [ ] Screenshots/examples current and accurate
- [ ] Troubleshooting section addresses common issues
- [ ] Installation instructions clear and complete

### Code Documentation
- [ ] Sheet workers commented appropriately
- [ ] CSS organized with clear sections
- [ ] HTML structure semantic and clear
- [ ] JSON schema documented with examples

## Final Validation

### Roll20 Submission Readiness
- [ ] All files properly named and formatted
- [ ] Sheet.json contains accurate metadata
- [ ] No console errors in browser developer tools
- [ ] Preview image created (if available)
- [ ] Instructions complete and accurate

### Feature Parity Check
- [ ] All FoundryVTT features replicated
- [ ] NPC import format compatible
- [ ] Character generation matches core rules
- [ ] Combat mechanics faithful to system
- [ ] Acts of Faith implementation complete

## Post-Upload Testing

### Roll20 Environment
- [ ] Sheet displays correctly in Roll20 interface
- [ ] All buttons work within Roll20 chat system
- [ ] Roll templates render properly in chat
- [ ] Character data saves and loads correctly
- [ ] Multiple characters can use sheet simultaneously

### User Acceptance
- [ ] New users can create characters easily
- [ ] Experienced users find all expected features
- [ ] Mobile users can play effectively
- [ ] GMs can manage NPCs efficiently
- [ ] No major usability issues reported

---

## Testing Notes

**Priority Order:**
1. Core functionality (character creation, combat)
2. Mobile responsiveness
3. Cross-browser compatibility
4. Advanced features (NPC import, Acts of Faith)
5. Performance and accessibility

**Test Data:**
- Use `sample-npcs.json` for import testing
- Create characters with various attribute combinations
- Test with both generated and manually created characters

**Known Limitations:**
- Roll20 sheet workers have some timing constraints
- Mobile browsers may have limited JavaScript performance
- Some advanced CSS features may not work in older browsers
