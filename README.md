# 🎹 GRAND STUDIO — Professional Digital Audio Workstation

> A full-featured, real-time piano and music production studio that runs entirely in your browser. No installs, no plugins — just open the HTML file and play.

---

## ✨ Features at a Glance

| Module | Description |
|---|---|
| 🎹 88-Key Piano | Full grand piano layout, playable via keyboard or mouse |
| 🥁 MPC Drum Pads | 12 velocity-sensitive pads with real drum synthesis |
| 🎛 FX / EQ | 8-band equalizer, reverb, delay, chorus, drive |
| 🎼 MIDI Support | Plug-and-play hardware MIDI keyboard support |
| 🤖 AI Chords | Smart chord progressions by key, scale & style |
| 📀 Loop Maker | Record, loop, and replay your performances |
| 🎚 Beat Sequencer | FL Studio–style 16-step sequencer with swing |
| 🎵 Arpeggiator | 5 modes, multi-octave with pattern editor |
| ⬇ WAV Export | Export your recorded session as a `.wav` file |
| 💥 Beat Drop | One-click BPM surge + reverb swell effect |

---

## 🚀 Getting Started

### Run Instantly
1. Download `piano-studio.html`
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. Click any key or press a keyboard key to start playing

> **No server required.** Everything runs client-side using the Web Audio API.

### Browser Compatibility
| Browser | Support |
|---|---|
| Chrome 80+ | ✅ Full support |
| Firefox 75+ | ✅ Full support |
| Safari 14+ | ✅ Full support |
| Edge 80+ | ✅ Full support |
| Mobile (touch) | ✅ Touch-enabled |

---

## ⌨️ Keyboard Mapping

### Piano Keys (Current Octave)

```
  W   E       R   T   Y
A   S   D   F   G   H   J   K
C  C#  D  D#  E  F  F#  G  G#  A  A#  B  C+1
```

| Key | Note | Key | Note (Black) |
|-----|------|-----|--------------|
| `A` | C (Do) | `W` | C# / Db |
| `S` | D (Re) | `E` | D# / Eb |
| `D` | E (Mi) | `R` | F# / Gb |
| `F` | F (Fa) | `T` | G# / Ab |
| `G` | G (Sol) | `Y` | A# / Bb |
| `H` | A (La) | `U` | C#+1 |
| `J` | B (Si) | `O` | D#+1 |
| `K` | C+1 | `;` | E+1 |

### Global Shortcuts

| Key | Action |
|-----|--------|
| `Z` | Octave Down |
| `X` | Octave Up |
| `Space` | Play / Pause sequencer |
| `Shift + R` | Toggle recording |
| `1` – `8` | Trigger drum pads 1–8 |

---

## 🎹 Piano Engine

Grand Studio uses **multi-partial harmonic synthesis** to model a real piano. Each note is built from 7 harmonic overtones with:

- **Inharmonicity simulation** — upper partials stretch slightly, just like real piano strings
- **Key thump** — a filtered noise burst on note-on for the mechanical feel
- **Full ADSR envelope** — attack, decay, sustain, release per note
- **Per-instrument character** — different decay curves and brightness per instrument type

### Instruments

| Instrument | Character |
|------------|-----------|
| **GRAND** | Warm, long decay — Yamaha concert grand style |
| **BRIGHT** | Faster decay, boosted upper harmonics |
| **E.PIANO** | Shorter sustain, Rhodes-like timbre |
| **ORGAN** | Very long sustain, held tones |

### Synth Waveforms
Switch away from piano mode into pure synthesis:
`Sine` · `Sawtooth` · `Square` · `Triangle`

---

## 🥁 Drum Pads (MPC Style)

12 pads with unique synthesis per drum type:

| Pad | Sound | Key |
|-----|-------|-----|
| KICK | Sub-oscillator pitch sweep | `Q` / `1` |
| SNARE | Bandpass-filtered noise burst | `W` / `2` |
| HIHAT | High-pass filtered noise (short) | `E` / `3` |
| OPEN HH | High-pass filtered noise (long) | `R` / `4` |
| CLAP | Mid-frequency noise burst | `T` / `5` |
| TOM 1 | Sine oscillator, 150Hz | `Y` / `6` |
| TOM 2 | Sine oscillator, 100Hz | `U` / `7` |
| CRASH | Filtered noise, long decay | `I` / `8` |
| RIDE | Mid-high oscillator | `O` |
| PERC 1 | 300Hz tone burst | `P` |
| PERC 2 | 400Hz tone burst | `[` |
| FX | 900Hz sweep | `]` |

---

## 🎚 Beat Sequencer

An **FL Studio–style step sequencer** with 6 tracks (Kick, Snare, Hi-Hat, Open, Clap, Tom).

- **Steps:** 8 / 16 / 32 configurable steps per pattern
- **Swing:** Drag the swing knob to add groove (delays every 2nd 16th note)
- **Live editing:** Click any step cell to toggle it on/off while the sequencer is running
- **BPM range:** 40 – 300 BPM, adjustable via slider or +/− buttons
- **Default pattern:** Kick on beats, snare on 2 and 4, hi-hat on 8ths — ready to play immediately

---

## 🎛 FX & EQ

### 8-Band Parametric Equalizer
Drag each vertical fader to boost or cut by ±12dB:

`80Hz · 160Hz · 320Hz · 640Hz · 1.2kHz · 2.5kHz · 5kHz · 10kHz`

### FX Knobs (drag up/down)
- **CHORUS** — Width and shimmer
- **DRIVE** — Harmonic saturation
- **ROOM** — Room size for reverb tail
- **BRIGHT** — High-frequency presence boost

### Real-Time Controls
| Control | Range | Effect |
|---------|-------|--------|
| Reverb | 0 – 100% | Convolution reverb with 2.5s impulse |
| Delay | 0 – 80% | 250ms feedback delay |
| Sustain | 0 – 4s | Note release time |
| Attack | 1ms – 300ms | Note fade-in speed |
| Velocity | 10 – 100% | Overall note loudness |

---

## 🎼 Pitch Controls

| Control | Range | Description |
|---------|-------|-------------|
| **Pitch Bend** | −12 to +12 semitones | Shift all played notes by semitones |
| **Octave Shift** | 0 – 7 | Move the keyboard mapping up or down |
| **Detune** | −50 to +50 cents | Fine-tune all notes (cents = 1/100 semitone) |

---

## 🤖 AI Chord Generator

Generates musically intelligent chord progressions based on your choices:

**Key** × **Scale** × **Style** → Progression

### Scales Available
`Major · Minor · Dorian · Mixolydian · Pentatonic · Blues`

### Styles
| Style | Typical Progressions |
|-------|----------------------|
| Pop | I–V–vi–IV, I–IV–V |
| Jazz | ii–V–I, iii–VI–ii–V |
| EDM | i–VI–III–VII |
| Lo-Fi | I–iii–IV–V, ii–V–I |
| Classical | I–IV–V–I cadences |

Click any generated chord chip to hear it played. Chords are voiced with root, third, and fifth.

---

## 📀 Loop Maker

1. Press **⬤ LOOP REC** to start recording your piano playing
2. Play anything — notes are timestamped precisely
3. Press **⬤ LOOP REC** again to stop
4. Press **▶ LOOP PLAY** to hear it loop continuously
5. Choose loop length: **2 / 4 / 8 bars**
6. Press **✕ CLEAR** to erase and start over

The loop position bar shows playback progress in real time.

---

## 🎵 Arpeggiator

Hold one or more notes on the piano to arpeggiate them.

### Modes
| Mode | Behavior |
|------|----------|
| Up | Plays notes from lowest to highest |
| Down | Plays notes from highest to lowest |
| Up-Down | Bounces between low and high |
| Random | Shuffles note order each step |
| Chord | Plays all held notes simultaneously |

### Settings
- **Speed:** 1/4 · 1/8 · 1/16 · 1/32 note resolution
- **Octaves:** Spreads the arp across 1, 2, or 3 octaves
- **Pattern editor:** 16-step grid — toggle individual arp steps on/off

Enable with **CHORD HOLD** to sustain notes without holding keys.

---

## 🎧 MIDI Keyboard Support

Grand Studio automatically detects any connected MIDI controller via the Web MIDI API.

- **Note On / Off** messages are handled in real time
- Velocity-sensitive (softer press = quieter note)
- Visual key highlighting on the on-screen piano
- Status shown in the bottom bar: `MIDI: CONNECTED`

> **Note:** MIDI requires Chrome or a Chromium-based browser. Firefox requires the [Web MIDI API polyfill](https://github.com/cwilso/WebMIDIAPIShim).

---

## ⬇ WAV Export

1. Click **● REC** in the transport bar to begin recording
2. Play your performance (piano, drums, chords — anything)
3. Click **● REC** again to stop
4. Click **⬇ EXPORT WAV** — the file downloads immediately

> The export renders your recorded MIDI events through the synthesis engine into a stereo 44.1kHz 16-bit PCM `.wav` file using the Web Audio `OfflineAudioContext`.

---

## 💥 Beat Drop

Press the **DROP** button for an instant crowd drop effect:
- BPM spikes by +32 for 2 seconds
- Reverb swells to 90% wet
- Rapid kick drum pattern fires
- Everything returns to normal automatically

---

## 🎨 Visual Design

- **Dark studio aesthetic** — near-black background with gold accent glow
- **Real-time spectrum analyzer** — frequency bars + waveform overlay at the top
- **Authentic piano keys** — ivory gradient whites, dark blacks with proper proportions
- **Key labels** — mapped keyboard shortcuts shown directly on keys
- **Active key glow** — gold highlight when a key is pressed
- **Fonts:** Orbitron (headers) · Rajdhani (UI) · Share Tech Mono (values)

---

## 🏗 Technical Architecture

```
piano-studio.html
│
├── Web Audio API
│   ├── AudioContext / OfflineAudioContext
│   ├── OscillatorNode (multi-partial synthesis)
│   ├── BiquadFilterNode (8-band EQ)
│   ├── ConvolverNode (reverb impulse response)
│   ├── DelayNode (echo)
│   ├── GainNode (ADSR envelopes)
│   └── AnalyserNode (visualizer)
│
├── Web MIDI API (hardware controller input)
│
├── Piano Layout
│   ├── 88-key DOM generation
│   ├── Black key absolute positioning
│   └── Mouse + touch + keyboard event handling
│
├── Sequencer Engine
│   ├── setInterval-based step clock
│   ├── Swing offset calculation
│   └── Per-track step arrays
│
└── Export
    ├── OfflineAudioContext rendering
    └── PCM → WAV ArrayBuffer encoding
```

**No dependencies. No frameworks. No build step.**  
Pure HTML + CSS + Vanilla JavaScript (~1,200 lines).

---

## 📁 File Structure

```
grand-studio/
└── piano-studio.html    # The entire application (single file)
└── README.md            # This file
```

---

## 🔧 Customization Tips

**Change default BPM:** Find `value="128"` in the BPM slider and change it.

**Add more drum pads:** Extend the `DRUMS` array with a new `{name, key, color, freq, type}` entry.

**Add a scale:** Add an entry to the `SCALES` object, e.g.:
```js
'Harmonic Minor': [0,2,3,5,7,8,11]
```

**Change reverb length:** Modify `audioCtx.sampleRate * 2.5` in `createReverb()` (seconds).

**Remap keyboard keys:** Edit the `KEY_MAP` object at the top of the script section.

---

## 📜 License

This project is released as open source. Feel free to use, modify, and distribute.

---

*Built with the Web Audio API · No dependencies · Single HTML file*

<div align="center">
Made with ❤️ by Mohammad Shakeel
Powered by MediaPipe Hands · Web Audio API · Vanilla JavaScript
</div>
