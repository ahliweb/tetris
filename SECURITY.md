# Security & Best Practices

## 🔒 Keamanan yang Diimplementasikan

### 1. LocalStorage Data Validation

#### Sanitasi Input
```javascript
function sanitizeNumber(value, defaultValue = 0, min = 0, max = Infinity) {
  const num = parseInt(value, 10);
  if(isNaN(num) || num < min || num > max) return defaultValue;
  return num;
}
```

**Perlindungan terhadap:**
- Invalid data types (string, object, undefined)
- Out of range values
- NaN (Not a Number)
- Negative scores (jika tidak diinginkan)
- Extremely large numbers yang bisa menyebabkan overflow

#### Contoh Penggunaan
```javascript
// Load high score dengan validation
gameState.highscore = sanitizeNumber(data.highscore, 0, 0, 999999999);
```

### 2. Error Handling untuk Audio Context

#### Problem
Browser modern memerlukan user interaction sebelum audio dapat diputar (autoplay policy).

#### Solution
```javascript
function ensureAudio() { 
  if(!audioCtx) { 
    try { 
      audioCtx = new AudioCtx(); 
    } catch(e) { 
      console.error('Audio not supported:', e);
      audioCtx = null; 
    } 
  } 
}
```

**Perlindungan terhadap:**
- Browser yang tidak support Web Audio API
- Permission errors
- Autoplay policy violations
- Memory leaks dari audio context

### 3. Try-Catch Blocks untuk External APIs

#### LocalStorage Operations
```javascript
function loadHighscore() { 
  try { 
    const saved = localStorage.getItem(CONFIG.STORAGE_KEY);
    if(saved) {
      const data = JSON.parse(saved);
      gameState.highscore = sanitizeNumber(data.highscore, 0, 0, 999999999);
    }
  } catch(e) { 
    console.error('Error loading highscore:', e);
    gameState.highscore = 0; 
  }
}
```

**Perlindungan terhadap:**
- QuotaExceededError (storage penuh)
- SecurityError (private browsing mode)
- JSON parsing errors (corrupt data)
- localStorage tidak available

### 4. Settings Persistence dengan Validation

```javascript
function loadSettings() {
  try {
    const saved = localStorage.getItem(CONFIG.SETTINGS_KEY);
    if(saved) {
      const parsed = JSON.parse(saved);
      if(typeof parsed === 'object') {
        gameState.settings = {
          soundEnabled: parsed.soundEnabled !== false,
          ghostEnabled: parsed.ghostEnabled !== false,
          gridEnabled: parsed.gridEnabled !== false
        };
        updateSettingsUI();
      }
    }
  } catch(e) {
    console.error('Error loading settings:', e);
  }
}
```

**Perlindungan terhadap:**
- Type coercion attacks
- Undefined properties
- Invalid boolean values

## 🛡️ Code Quality & Maintainability

### 1. Organized Code Structure

Kode diorganisir dalam sections yang jelas:
```javascript
// ==================== CONFIGURATION ====================
// ==================== GAME STATE ====================
// ==================== DOM ELEMENTS ====================
// ==================== TETROMINO DEFINITIONS ====================
// ==================== AUDIO SYSTEM ====================
// ==================== UTILITY FUNCTIONS ====================
// ==================== DRAWING FUNCTIONS ====================
// ==================== GAME LOGIC ====================
// ==================== GAME LOOP ====================
// ==================== INPUT HANDLERS ====================
// ==================== INITIALIZATION ====================
```

### 2. JSDoc Comments

Setiap fungsi didokumentasikan:
```javascript
/**
 * Validate and sanitize localStorage data
 */
function sanitizeNumber(value, defaultValue = 0, min = 0, max = Infinity) {
  // implementation
}
```

### 3. Configuration Object

Semua konstanta dikumpulkan di satu tempat:
```javascript
const CONFIG = {
  COLS: 10,
  ROWS: 20,
  CELL_SIZE: 28,
  STORAGE_KEY: 'tetris_v2_data',
  SETTINGS_KEY: 'tetris_v2_settings'
};
```

**Keuntungan:**
- Easy to modify
- No magic numbers
- Centralized configuration
- Version control friendly

### 4. Game State Object

State management yang terpusat:
```javascript
const gameState = {
  arena: null,
  score: 0,
  lines: 0,
  level: 1,
  highscore: 0,
  dropCounter: 0,
  dropInterval: 1000,
  lastTime: 0,
  paused: false,
  running: false,
  gameStartTime: 0,
  totalPieces: 0,
  holdUsed: false,
  settings: {
    soundEnabled: true,
    ghostEnabled: true,
    gridEnabled: true
  }
};
```

**Keuntungan:**
- Single source of truth
- Easy debugging
- Clear state management
- Prevent global variable pollution

## 🧪 Testing Support

### Data-testid Attributes

Semua elemen interaktif memiliki data-testid:
```html
<canvas id="tetris" data-testid="game-canvas"></canvas>
<button id="btn-left" data-testid="btn-left">←</button>
<div id="score" data-testid="score">0</div>
```

**Keuntungan:**
- Automated testing dengan Playwright/Cypress
- Stable selectors (tidak bergantung pada class/id)
- Better test maintainability

## 🚀 Performance Best Practices

### 1. RequestAnimationFrame

Menggunakan requestAnimationFrame untuk game loop:
```javascript
function update(time = 0) {
  if(!gameState.running) return;
  // game logic
  requestAnimationFrame(update);
}
```

**Keuntungan:**
- Browser-optimized rendering
- Better frame rate
- Automatic pause when tab inactive
- Efficient CPU usage

### 2. Canvas Optimization

Clear dan redraw yang efisien:
```javascript
function draw() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  // draw only what's needed
}
```

### 3. Event Delegation

Efficient event handling:
```javascript
// Single event listener untuk keyboard
window.addEventListener('keydown', handleKey);
```

## 🔐 Privacy & Data Protection

### What Data is Stored?

```javascript
// High score data
{
  "highscore": 12500,
  "timestamp": 1704067200000
}

// Settings data
{
  "soundEnabled": true,
  "ghostEnabled": true,
  "gridEnabled": true
}
```

### Data Retention
- Data disimpan di browser user (localStorage)
- Tidak ada data yang dikirim ke server
- User dapat clear data kapan saja (browser settings)
- No cookies, no tracking, no analytics

## 📋 Security Checklist

- [x] Input validation untuk semua user input
- [x] Sanitasi data localStorage
- [x] Error handling untuk external APIs
- [x] No eval() atau dangerous functions
- [x] No inline event handlers
- [x] Content Security Policy compatible
- [x] HTTPS ready
- [x] No external dependencies (no supply chain attacks)
- [x] No user-generated content execution
- [x] Private browsing mode compatible

## 🛠️ Recommended Browser Settings

Untuk pengalaman terbaik:
- Enable JavaScript
- Enable localStorage
- Allow Web Audio API
- Modern browser (Chrome 90+, Firefox 88+, Safari 14+, Edge 90+)

## 📝 Vulnerability Reporting

Jika menemukan kerentanan keamanan, silakan laporkan ke:
- Email: security@ahliweb.co.id
- Atau buat issue di GitHub dengan label "security"

---

**Last Updated:** January 2025  
**Version:** 2.0.0
