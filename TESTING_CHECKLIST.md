# ✅ Testing Checklist - Tetris Game v2.0

## 🎯 Pre-Release Testing Checklist

Gunakan checklist ini untuk memastikan semua fitur berfungsi dengan baik sebelum release.

---

## 1️⃣ Core Gameplay

### Basic Movement
- [ ] Arrow Left - Piece bergerak ke kiri
- [ ] Arrow Right - Piece bergerak ke kanan
- [ ] Arrow Down - Soft drop (turun cepat)
- [ ] Space - Hard drop (langsung jatuh)
- [ ] Arrow Up - Rotasi clockwise
- [ ] Piece stop di dasar arena
- [ ] Piece lock setelah landed

### Collision Detection
- [ ] Piece tidak bisa keluar dari arena (left)
- [ ] Piece tidak bisa keluar dari arena (right)
- [ ] Piece tidak bisa tembus arena bottom
- [ ] Piece tidak overlap dengan locked pieces
- [ ] Rotasi di-cancel jika collision

### Line Clearing
- [ ] 1 line cleared → score +40×level
- [ ] 2 lines cleared → score +100×level
- [ ] 3 lines cleared → score +300×level
- [ ] 4 lines cleared (Tetris) → score +1200×level
- [ ] Cleared lines removed dari arena
- [ ] Rows above drop down correctly

### Level & Speed
- [ ] Level naik setiap 10 lines cleared
- [ ] Drop speed increase dengan level
- [ ] Level display update correctly
- [ ] Max speed capped di level 13+

### Game Over
- [ ] Game over saat piece spawn di occupied space
- [ ] Overlay muncul dengan message
- [ ] Score akhir ditampilkan
- [ ] Restart button berfungsi

---

## 2️⃣ New Features (v2.0)

### Hold Piece
- [ ] Press C → piece disimpan ke hold
- [ ] Hold button UI berfungsi
- [ ] First hold → spawn next piece immediately
- [ ] Swap hold ↔ current berfungsi
- [ ] Hold disabled setelah digunakan (gray out)
- [ ] Hold reset setelah piece lock
- [ ] Hold canvas menampilkan piece correctly
- [ ] Hold piece centered di canvas

### Ghost Piece
- [ ] Ghost piece muncul di landing position
- [ ] Ghost piece transparan (outline only)
- [ ] Ghost update real-time saat move
- [ ] Ghost update saat rotasi
- [ ] Ghost tidak muncul jika sudah di bottom
- [ ] Toggle ghost di settings berfungsi

### Wall Kick (SRS)
- [ ] Rotasi near left wall → wall kick right
- [ ] Rotasi near right wall → wall kick left
- [ ] I-piece wall kick differently
- [ ] JLSTZ pieces wall kick correctly
- [ ] O-piece tidak butuh wall kick
- [ ] Multiple kick attempts (up to 5)
- [ ] Kick cancel jika semua fail

---

## 3️⃣ UI/UX

### Welcome Screen
- [ ] Overlay muncul saat page load
- [ ] Instruksi keyboard ditampilkan
- [ ] Start button berfungsi
- [ ] Overlay hide setelah start

### Layout Desktop (>900px)
- [ ] 3-column layout: Hold | Game | Stats
- [ ] All panels visible
- [ ] Proper spacing
- [ ] Responsive width

### Layout Mobile (<768px)
- [ ] Single column stacked
- [ ] Touch controls muncul
- [ ] Readable font sizes
- [ ] Proper scrolling

### Statistics Panel
- [ ] Waktu bermain update setiap detik
- [ ] Total pieces count correctly
- [ ] PPM (pieces per minute) calculated
- [ ] Time format MM:SS

### Settings Panel
- [ ] Sound toggle berfungsi
- [ ] Ghost toggle berfungsi
- [ ] Grid toggle berfungsi
- [ ] Toggle animation smooth
- [ ] Settings persist di localStorage
- [ ] Settings load on page reload

### Score Display
- [ ] Score update immediately
- [ ] Level update correctly
- [ ] Lines update correctly
- [ ] High score update jika beaten
- [ ] High score persist di localStorage

### Buttons
- [ ] All buttons clickable
- [ ] Hover effects work
- [ ] Active state visual feedback
- [ ] Disabled state when game not running

---

## 4️⃣ Touch Controls (Mobile)

### Touch Buttons
- [ ] Touch Left - move left
- [ ] Touch Right - move right
- [ ] Touch Rotate - rotate piece
- [ ] Touch Down - soft drop
- [ ] Touch Drop - hard drop
- [ ] Touch Hold - hold piece
- [ ] Buttons visible pada mobile
- [ ] Buttons hidden pada desktop
- [ ] Touch targets ≥48×48px
- [ ] No accidental double-tap

---

## 5️⃣ Audio System

### Sound Effects
- [ ] Lock sound saat piece lands
- [ ] Line clear sound (pitch varies by lines)
- [ ] Move sound saat geser/rotasi
- [ ] Sound toggle mute/unmute
- [ ] Audio work di Chrome
- [ ] Audio work di Firefox
- [ ] Audio work di Safari
- [ ] No audio errors di console

### Audio Context
- [ ] Audio init after user interaction
- [ ] No autoplay violations
- [ ] Error handling graceful
- [ ] Audio cleanup proper

---

## 6️⃣ Data Persistence

### High Score
- [ ] High score save to localStorage
- [ ] High score load on page load
- [ ] High score survive page reload
- [ ] Invalid data handled gracefully
- [ ] Data sanitized (no negative, no NaN)

### Settings
- [ ] Settings save immediately
- [ ] Settings load on init
- [ ] Settings persist across sessions
- [ ] Corrupt settings handled

### LocalStorage Errors
- [ ] QuotaExceededError handled
- [ ] SecurityError handled (private mode)
- [ ] JSON parse errors handled
- [ ] Missing key handled

---

## 7️⃣ Game Controls

### Keyboard
- [ ] All arrow keys work
- [ ] Space bar work
- [ ] C key (hold) work
- [ ] P key (pause) work
- [ ] Keys work saat game running only
- [ ] No browser default actions (scroll)

### UI Buttons
- [ ] Left button
- [ ] Right button
- [ ] Rotate button
- [ ] Down button
- [ ] Drop button
- [ ] Hold button
- [ ] Pause button
- [ ] Restart button

### Pause System
- [ ] P key pause/resume
- [ ] Pause button pause/resume
- [ ] Button text change (Pause ↔ Resume)
- [ ] Overlay muncul saat pause
- [ ] Game state frozen saat pause
- [ ] Resume continue correctly

---

## 8️⃣ Visual Polish

### Animations
- [ ] Button hover effects smooth
- [ ] Toggle switch animation smooth
- [ ] Overlay fade in/out
- [ ] Piece movement smooth

### Colors & Styling
- [ ] All 7 piece colors distinct
- [ ] Ghost piece transparan
- [ ] Grid lines subtle
- [ ] Neon border effect
- [ ] Gradient backgrounds

### Canvas Rendering
- [ ] No flickering
- [ ] 60 FPS smooth
- [ ] Pieces drawn correctly
- [ ] Grid aligned properly
- [ ] Next piece centered
- [ ] Hold piece centered

---

## 9️⃣ Browser Compatibility

### Desktop Browsers
- [ ] Chrome 90+ ✅
- [ ] Firefox 88+ ✅
- [ ] Safari 14+ ✅
- [ ] Edge 90+ ✅

### Mobile Browsers
- [ ] iOS Safari ✅
- [ ] Chrome Android ✅
- [ ] Samsung Internet ✅
- [ ] Firefox Mobile ✅

### Features Support
- [ ] Canvas API
- [ ] Web Audio API
- [ ] LocalStorage
- [ ] RequestAnimationFrame
- [ ] ES6 features
- [ ] CSS Grid
- [ ] Media Queries

---

## 🔟 Performance

### Desktop Performance
- [ ] 60 FPS consistent
- [ ] CPU usage <5%
- [ ] Memory usage <20MB
- [ ] No memory leaks
- [ ] Fast load time (<100ms)

### Mobile Performance
- [ ] 60 FPS on high-end
- [ ] 30 FPS acceptable on low-end
- [ ] Touch response <50ms
- [ ] Battery drain reasonable
- [ ] No overheating

### Code Quality
- [ ] No console errors
- [ ] No console warnings
- [ ] Proper error handling
- [ ] Clean code structure

---

## 1️⃣1️⃣ Security

### Input Validation
- [ ] LocalStorage data validated
- [ ] Score range checked (0-999999999)
- [ ] Level range checked
- [ ] Settings type checked
- [ ] NaN values rejected
- [ ] Undefined handled

### Error Handling
- [ ] Try-catch di localStorage ops
- [ ] Try-catch di audio ops
- [ ] Try-catch di JSON parse
- [ ] Errors logged to console
- [ ] Graceful degradation

### Privacy
- [ ] No external requests
- [ ] No tracking code
- [ ] No cookies
- [ ] Data stays local
- [ ] User control over data

---

## 1️⃣2️⃣ Documentation

### Code Documentation
- [ ] All functions have JSDoc
- [ ] Complex logic commented
- [ ] Sections clearly marked
- [ ] Variable names descriptive

### External Docs
- [ ] README.md complete
- [ ] CHANGELOG.md updated
- [ ] SECURITY.md present
- [ ] TECHNICAL_DOCS.md detailed
- [ ] IMPROVEMENTS_SUMMARY.md accurate

---

## 1️⃣3️⃣ Testing Support

### Test IDs
- [ ] All interactive elements have data-testid
- [ ] Canvas elements have test IDs
- [ ] Display elements have test IDs
- [ ] 32 total test IDs present

### Testability
- [ ] Functions are pure where possible
- [ ] State centralized
- [ ] Side effects isolated
- [ ] Easy to mock

---

## 🎯 Critical Path Test

**Quick smoke test (5 minutes):**

1. [ ] Open tetris.html
2. [ ] Click Start Game
3. [ ] Play for 30 seconds
4. [ ] Clear at least 1 line
5. [ ] Test hold piece (press C)
6. [ ] Test ghost piece visible
7. [ ] Test pause (press P)
8. [ ] Test restart button
9. [ ] Check high score persists (reload page)
10. [ ] Test on mobile device

**Result:** All pass? ✅ Ready to ship!

---

## 🐛 Known Issues

### Current Issues (If any)
- [ ] None identified

### Wontfix (Out of scope)
- [ ] Multiplayer (planned for v3.0)
- [ ] Online leaderboard (planned for v3.0)
- [ ] T-Spin detection (planned for v3.0)

---

## 📊 Test Results Log

### Test Date: _______________
### Tester: _______________
### Browser: _______________
### OS: _______________

**Overall Status:**
- [ ] ✅ Pass - Ready to release
- [ ] ⚠️ Pass with minor issues - Can release
- [ ] ❌ Fail - Needs fixes

**Issues Found:**
1. _______________________________________________
2. _______________________________________________
3. _______________________________________________

**Notes:**
_______________________________________________
_______________________________________________
_______________________________________________

---

## 🚀 Release Checklist

Before releasing v2.0:

- [ ] All tests passed
- [ ] Documentation complete
- [ ] No console errors
- [ ] Tested on 3+ browsers
- [ ] Tested on mobile
- [ ] High score persistence verified
- [ ] Performance acceptable
- [ ] Code reviewed
- [ ] Git tagged (v2.0.0)
- [ ] CHANGELOG updated

---

**Version:** 2.0.0  
**Last Updated:** January 2025  
**Status:** Ready for Testing ✅
