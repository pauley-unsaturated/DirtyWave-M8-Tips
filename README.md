# DirtyWave M8 Tracker - Comprehensive Guide

## Introduction

The DirtyWave M8 is a portable tracker sequencer and synthesizer, inspired by the renowned Gameboy tracker Little Sound DJ. Packed into its handheld form factor is a powerful music production system capable of creating complete compositions using a combination of synthesis engines, sample playback, and MIDI control.

This guide aims to provide a comprehensive overview of the M8's features, interface, and workflow, combining official documentation with community-discovered techniques and tips.

## Hardware Overview

The M8 is a compact device with the following specifications:

- High-quality IPS display with capacitive touch (2.8" on Model:01, 3.5" on Model:02)
- 3.5mm TRS MIDI (Type A) input and output
- Stereo audio input and headphone/main output
- USB MIDI and Audio compliant
- SDHC Micro SD slot for storage
- Rechargeable battery (1200mAh with ~4 hours use on Model:01, 4300mAh with ~12 hours use on Model:02)
- Built-in MEMS microphone (Model:02 only)

## Core Features

- 8 Monophonic Tracks/Voices
- 255 Patterns/Phrases & chains
- 256 Instrument Tables for advanced modulation
- 128 Instruments per song
- Song Arranger with Live mode
- Full MIDI input & output support

## Synthesis Engines

The M8 comes equipped with multiple synthesis engines:

1. **Wavsynth** - Classic console & computer chip emulation for those 8-bit sounds
2. **Macrosynth** - Based on Mutable Instruments Braids with 40+ versatile synthesis types
3. **FM Synth** - 4-operator FM synthesis with 12 algorithms and feedback per operator
4. **Sampler** - 8/16-bit mono and full stereo WAV format playback
5. **Hypersynth** - 6-note chord synthesizer
6. **MIDI Out** - MIDI instruments with 10 user-definable CCs
7. **External Instrument** - MIDI output with audio input processing

Global effects include reverb, chorus, delay, EQ, DJ filter, and a master bus limiter.

## Interface Navigation

The M8's interface follows a logical hierarchical structure. Navigation is primarily handled by holding the Shift button and using directional keys.

### Basic Navigation:

- **Shift + Up/Down/Left/Right**: Navigate between related screens
- **Option + Left/Right**: Navigate to previous/next instrument, phrase, etc.
- **Option + Up/Down**: Skip by larger increments (typically 16 steps)
- A small map in the bottom-right corner of the screen helps you keep track of where you are in the interface

### Main Screens:

1. **Song View**: Organize chains for each of the 8 tracks
2. **Chain View**: Create sequences of phrases
3. **Phrase View**: Program individual steps with notes, instruments, and effects
4. **Instrument View**: Configure synthesis parameters for each instrument
5. **Instrument Modulation View**: Configure envelopes, LFOs and other modulators
6. **Instrument Pool View**: Overview of all instrument slots
7. **Table View**: Create modulation patterns for instruments
8. **Groove View**: Set timing variations for more human feel
9. **Scale View**: Define and edit musical scales
10. **Mixer View**: Adjust volumes and effects sends
11. **EQ Editor View**: Configure parametric EQ settings
12. **Limiter & Mix Scope View**: Adjust limiter settings and view audio levels
13. **Effect Settings View**: Configure global effects
14. **Project View**: Save/load songs and project settings
15. **Theme View**: Customize the visual appearance
16. **MIDI Mapping View**: Assign MIDI controls
17. **MIDI Settings View**: Configure MIDI behavior
18. **Time Stats View**: View time statistics
19. **Render View**: Export audio
20. **Effect Command Help View**: Reference for effect commands

## Basic Workflow

The workflow in M8 follows the tracker paradigm but with a unique hierarchical structure:

1. **Songs** contain chains for each of the 8 tracks
2. **Chains** are sequences of phrases
3. **Phrases** are 16-step patterns containing notes, instruments, and effect commands
4. **Instruments** can be one of the available synthesis engines with various parameters
5. **Tables** provide additional modulation capabilities per instrument

## Key Shortcuts and Tips

### Common Shortcuts:
- **UP/DOWN/LEFT/RIGHT**: Move cursor position
- **SHIFT + UP/DOWN/LEFT/RIGHT**: Screen navigation
- **EDIT + LEFT/RIGHT**: Fine edit value
- **EDIT + UP/DOWN**: Coarse edit value
- **EDIT + OPTION**: Delete value or reset to default
- **SHIFT + OPTION**: Enter selection mode or copy selection
- **SHIFT + EDIT**: Paste selection
- **PLAY**: Start/stop playback
- **SHIFT + PLAY**: Play all tracks from current position

### Advanced Editing Techniques:

#### Selection and Interpolation
1. **Interpolation**: When in selection mode with a single column highlighted, press [SHIFT]+[EDIT] to interpolate values between the first and last selected cells. This is incredibly useful for creating smooth automation curves in effect columns or smooth transitions in table data.

2. **Multi-column selection**: Select multiple columns by moving the cursor horizontally after entering selection mode with [SHIFT]+[OPTION]. You can then cut/copy/paste entire blocks of data.

3. **Note fill techniques**: In selection mode with the note column selected:
   - [OPTION]+[LEFT]: Cycle through fill modes (scale, chord, random)
   - [OPTION]+[RIGHT]: Randomize note and instrument triggers
   - [OPTION]+[UP/DOWN]: Randomize the note values up or down
   These operations transform a selection into patterns following musical rules or randomized variations.

#### Cloning Operations
1. **Clone**: [SHIFT]+[OPTION, then EDIT] copies the content of the current chain/phrase/instrument to a new unused number. This creates a new identical item that can be modified independently.

2. **Deep Clone**: [SHIFT]+[OPTION, then double-tap EDIT] on a chain performs a "deep clone" that copies not only the chain but also all phrases within it to new numbers. This is perfect for creating variations of entire sections without affecting the original material.

#### Multi-edit Operations
1. **Quick Create**: Double-tap [EDIT] on an empty cell to create a new chain/phrase/instrument/table with the next available number.

2. **Pattern Nudge**: In selection mode with multiple rows and columns selected, use [EDIT]+[UP/DOWN] to shift the entire pattern up or down.

3. **Parameter jumping**: When on an instrument or effect parameter, use [SHIFT]+[LEFT/RIGHT] to navigate to the phrase or table view with that parameter pre-selected as the default FX command, speeding up automation creation.

### Community Tips and Tricks:

- Save a song to `/System/TEMPLATE.m8s` to use it as the default template when creating new songs
- When working with chains, be aware that copy/paste operations will push lower chains down and chains can permanently scroll out if pushed past row FF
- To fix choppy sample playback, try doing a directory sort (SHIFT + OPTION) in the file browser
- When loading a new sampler instrument, you can select a sample directly instead
- Use the HOP command to create polyrhythms by having independent play heads for each track
- There are three ways to slice samples: evenly, auto on transient, and auto on silence

## Advanced Techniques

### Sample Chopping for Drum and Bass Style Break Beats

Break chopping is a cornerstone technique for many electronic music genres. Here's how to effectively chop breaks on the M8:

#### Method 1: Slice Markers + Sampler Instrument

1. **Record or load your break**: Load a break into the sample editor.

2. **Set slice markers**: Use one of three methods:
   - **Auto-slice on transients**: In the sample editor, select PROCESS > SLICE:AUTO
   - **Manual slicing**: In SLICE MARKER mode, press [EDIT] during playback to add slice markers at the playhead position (often called "lazy chop" technique)
   - **Even divisions**: Use PROCESS > SLICE:[number] to divide into equal parts

3. **Set up a sampler instrument**: 
   - Set SLICE to "01 FILE" to use the slice markers stored in the file
   - Create a phrase with different notes starting from C-1 to trigger different slices
   - Use tables to create complex playback patterns

4. **Creative techniques**:
   - Create multiple sampler instruments pointing to the same break but with different filter, playback, and effect settings
   - Use the chance (CHA) command to randomize which slices play for more variety
   - Combine with the RND (randomize) command to create generative patterns

#### Method 2: Sample Start Position Automation

For more precise control:

1. Load your break into a sampler instrument
2. Instead of slices, use FX commands to alter the START and LEN parameters
3. Create a table with "STA" commands at different positions to "manually" slice
4. Combine with the PSL (portamento slide) command for pitched time-stretching effects

### Song Structure and Organization Techniques

#### Using "Empty" and "Stop" Chains

Clever use of empty and stop chains gives you more control over your song structure:

1. **Empty chain technique**: 
   - Create a chain (often numbered 00 or FE) with empty phrases
   - Use this as a placeholder to maintain track synchronization while a track is silent
   - This prevents tracks from getting out of sync during complex arrangements

2. **Stop chain technique**:
   - Create a dedicated chain with the "HOPFF" command in its phrase
   - This acts as a "stop" command that halts just that specific track
   - Place this at the end of sections where you want specific tracks to end

3. **Bookmarking technique**:
   - Use [OPTION]+[OPTION]+[OPTION] on important chains to create visual bookmarks
   - This helps navigate complex songs with many sections

#### Creating Intros and Outros

1. **Intro technique**:
   - Create a dedicated intro section in the song view
   - Use high-frequency filter automation with DJF commands for the classic filter sweep in
   - Gradually bring in elements using empty chains for initial tracks

2. **Outro technique**:
   - Use a reverse approach with filter sweeps down and gradual removal of elements
   - Consider rendering specific sections to samples, then using those samples pitched down for outro effects

### Advanced FX Automation Techniques

#### Command Column Automation

The three command columns per phrase step are powerful for creating movement:

1. **Ping-pong delay automation**:
   - Use XDT command to change delay times
   - Alternate between different settings to create rhythmic variations

2. **Filter sweeps**:
   - Use CUT and RES commands with REP (repeat) to gradually change values
   - Create filter envelopes using command columns instead of using the built-in envelopes

3. **Command stacking**:
   - Each of the three command columns operates independently
   - Stack multiple effects on a single step for complex sound design
   - Example: Stack a CUT (filter cutoff), AMP (amplitude), and RET (retrigger) on one step

#### Table-Based Automation

Tables offer a way to create intricate automation patterns tied to note triggers:

1. **Multi-rate table technique**:
   - Place the TIC (table tick rate) command in different columns in your table
   - Each column can run at different speeds, creating complex polyrhythmic modulation
   - Example: Column 1 runs at TIC0C, column 2 at TIC06, column 3 at TIC03

2. **Envelope shaping technique**:
   - Use tables as multi-stage envelopes beyond what the built-in envelopes offer
   - Create table automation for cutoff, resonance, and amplitude simultaneously
   - Shape the decay portion of sounds with fine precision

3. **Parallel table technique**:
   - Use the TBX (auxiliary table) command to run two tables simultaneously
   - Have one table focus on timbre changes while another handles rhythmic effects

### Advanced Mixing and Sound Design

#### Sound Layering Techniques

1. **Dual-track instrument layering**:
   - Assign the same MIDI channel to two consecutive tracks in MIDI Settings view
   - Set mode to POLY
   - When you play a note via MIDI, both tracks trigger simultaneously with different instruments

2. **Time-offset layering**:
   - Use two tracks with identical phrases but add a DEL (delay) command to one
   - This creates a precise layered sound with a controlled time offset
   - Great for wider stereo images and more complex textures

#### Bouncing and Resampling

1. **Sample to selection workflow**:
   - Create and perfect a section in the sequencer
   - Use [SHIFT]+[OPTION] to make a selection
   - Double-tap [EDIT] to render that selection to a new sample and instrument
   - This creates a new sampler instrument containing your rendered audio

2. **Resampling for effects**:
   - Apply heavy processing to a rendered sample
   - Re-render with additional effects for compound processing
   - Great for unique textures that would be CPU-intensive to play in real-time

3. **Track recording technique**:
   - Set up an External Instrument type
   - Route it to record from one of your playing tracks (TR1-8)
   - Record while the song plays to bounce specific elements

### Live Performance Techniques

#### Live Mode Mastery

Live mode transforms the M8 from a studio tool to a performance instrument:

1. **Song as template technique**:
   - Create a song with all your sounds and processing chains ready
   - Use Live Mode to trigger different sections on the fly
   - Adjust quantization settings in Project View for tighter or more immediate transitions

2. **Mute Groups**:
   - Organize your tracks into functional groups (drums, bass, melodies, etc.)
   - Use [OPTION]+[SHIFT] and [OPTION]+[PLAY] for quick muting/soloing
   - Practice patterns of muting and unmuting for build-ups and breakdowns

3. **MIDI Mapping for performance**:
   - Map critical parameters to the touchscreen's X and Y axes
   - Create dedicated control instruments with CCx parameters for controlling external gear
   - Use the DJ filter mapped to a physical controller for hands-on filtering

### Groove and Rhythm Techniques

#### Creating Complex Polyrhythms

1. **Multi-groove technique**:
   - Assign different grooves to different tracks using the GRV command
   - Create groove patterns with odd numbers of steps to create shifting phase relationships
   - Example: Track 1 with a 6-step groove, Track 2 with a 7-step groove

2. **Step skipping in grooves**:
   - Use "00" in a groove to completely skip a step
   - Create rhythmic displacement by strategically skipping steps
   - Combine with the "NTH" command to create evolving patterns that change over time

#### Making "Human" Rhythms

1. **Velocity variations**:
   - Use probability commands (CHA) on velocity columns for natural dynamics
   - Create humanized hi-hat patterns by varying velocities slightly

2. **Micro-timing**:
   - Add small DEL (delay) values to notes for subtle timing shifts
   - Create groove templates that introduce subtle timing variations

3. **Random element technique**:
   - Use RND commands with small ranges for subtle variations
   - Apply random seed (SED) commands at section changes for controlled randomness

### Working with Tables

Tables are instrument-specific automation patterns that trigger when a note from that instrument is played. Think of them as "patterns within a note" that can modulate various parameters Tables sequence commands per each note/instrument trigger, running alongside the main sequence.

#### Table Fundamentals
- Tables run at the speed defined by TABLE TIC in the instrument settings
- Each table has 16 rows with columns for note transpose, volume, and three FX commands
- The table rate can be set from 00 to FF:
  - 00: Only advances when a new note is triggered (automation mode)
  - 01-FE: Speed in ticks (at 24 ticks per quarter note)
  - FF: Maximum speed (400 Hz)
  - FE: Maps note to table position

#### Advanced Table Techniques
- **Independent column speeds**: Use the TIC command in different FX columns to create polyrhythmic modulations within a single table
- **Table jumping**: Use the HOP command to create loops or shorter repeating patterns within a table
- **Multiple table sequencing**: Use the TBX command in a phrase to run an auxiliary table alongside the instrument's main table
- **Command chaining**: Place related commands in succession for compound effects (e.g., filter sweep + volume fade)
- **Pitch modulation**: Create arpeggios, vibrato, and pitch bends by modulating the transpose column

#### Creative Applications
- Create complex multi-stage envelopes beyond what's possible with the built-in envelope generators
- Design rhythmic gate effects by modulating volume
- Generate algorithmic melodies using the randomize (RND) and probability (CHA) commands
- Simulate chord progressions on a single track using note transposition
- Create evolving sound textures with automated filter sweeps

### Using the Groove Feature

Grooves allow timing manipulation per track, creating more organic rhythmic patterns or complex polyrhythms.

- A standard 16th note is 6 ticks (at 24 ticks per quarter note)
- Adjust groove values to create swing (e.g., 7,5 or 8,4)
- Create uneven grooves for unusual time signatures
- Set values to 00 to skip steps entirely

### MIDI Integration

The M8 can both receive and send MIDI, allowing it to control external gear or be controlled by external controllers.

- Use the MIDI Settings view to configure sync, transport, and channel assignments
- MIDI Out instruments can send up to 10 user-defined CCs
- External Instruments combine MIDI output with audio input processing
- Map MIDI CCs to parameters in the MIDI Mapping view

### Mastering the FM Synth

The FM Synth is one of the M8's most powerful synthesis engines, capable of creating a wide range of sounds from classic digital tones to complex textures. It features 4 operators with 12 algorithm configurations.

#### FM Synth Architecture
- **4 Operators (A, B, C, D)**: Each operator can be thought of as a simple sine wave generator that can modulate or be modulated by other operators
- **12 Algorithms**: Different configurations of how operators connect to each other
- **Versatile waveforms**: Each operator can use different waveforms beyond just sine waves
- **Feedback**: Each operator can have feedback applied, creating more complex timbres

#### Understanding FM Synthesis Concepts
- **Frequency Ratio**: Each operator has a frequency ratio value that determines its pitch relative to the note being played. Standard values include:
  - 1.00: Same as the played note
  - 2.00: One octave higher
  - 0.50: One octave lower
  - Non-integer values: Create detuned or inharmonic sounds

- **Level and Feedback**: 
  - The level controls the amplitude of each operator
  - Feedback routes an operator's output back into itself, creating more complex, sometimes chaotic sounds
  - The combination of these parameters dramatically shapes the timbre

- **Modulation Slots**: 
  - Each operator has two modulation slots that can control level, ratio, pitch, or feedback
  - These can be assigned to one of the four global modulation sources (MOD1-4)
  - This creates dynamic, evolving sounds without using external modulation

#### Creating Classic FM Sounds
1. **Basic Bell Tone**:
   - Use algorithm 0 (A>B>C>D)
   - Set operator A's ratio to 1.00, with high level and feedback
   - Set operators B, C, and D to higher ratios (3.00, 5.00, etc.)
   - Use an AHD envelope to modulate the levels

2. **Classic FM Piano**:
   - Use algorithm 2 ([A>B+C]>D)
   - Set ratios to create harmonics (1.00, 2.00, 3.00, etc.)
   - Configure envelopes with fast attack and moderate decay
   - Add slight feedback to operator A for more character

3. **Bass Sound**:
   - Use algorithm 4 ([A+B+C]>D)
   - Set ratios for low frequencies (1.00, 1.01, 0.99, 2.00)
   - Apply moderate feedback to create harmonics
   - Use envelope to control the punch (fast attack, medium decay)

#### Advanced FM Techniques
- **Creating movement**: Assign MOD sources to ratio parameters for vibrato or sweeping effects
- **Morphing sounds**: Use tables to automate operator levels, creating evolving textures
- **Stack operators**: Use multiple modulating operators for complex waveforms
- **Additive approach**: Use algorithm 11 (A+B+C+D) for additive synthesis rather than FM

### Harnessing the Hypersynth

The Hypersynth was introduced in firmware 3.0 as a solution to the M8's monophonic limitation, offering a way to play chords on a single track.

#### Hypersynth Architecture
- **6 Sawtooth Oscillators**: These form the basis of the sound, arranged into chord structures
- **16 Chord Banks**: User-definable chord configurations
- **Suboscillator**: Additional square wave 1-2 octaves below the root note

#### Setting Up the Hypersynth
1. **Configuring Chord Banks**:
   - Each bank can hold up to 6 intervals defining a chord type
   - Values are semitone offsets from the root note (e.g., major triad: 0, 4, 7)
   - Create your chord library in banks 1-16

2. **Key Parameters**:
   - **SCALE**: Select which scale from the Scale View to use for note quantization
   - **CHORD**: Select the chord bank and view/edit the intervals
   - **SHIFT**: Crossfades between the first 3 and last 3 intervals of the chord
   - **SWARM**: Detunes oscillators for a richer, wider sound
   - **WIDTH**: Controls stereo spread of the oscillators
   - **SUBOSC**: Adds sub-bass (2 octaves below when <80, 1 octave when >80)

#### Creative Applications
- **Pad Sounds**: Use moderate SWARM and WIDTH settings with slow attack/release envelopes
- **Chord Progressions**: Sequence different chords by using different notes to trigger different transpositions of your chord banks
- **Bass + Chord**: Use high SUBOSC values to create both bass and chord elements in one track
- **Moving Textures**: Automate the SHIFT parameter to create evolving pad sounds

#### Integration Techniques
- **Split Approach**: Use one track for bass (with SUBOSC) and another for chords
- **Layer with FM**: Use multiple tracks to layer Hypersynth chords with FM leads
- **Scale Matching**: Ensure your Scale settings match across tracks for harmonic consistency

### Combining FM and Hypersynth
- Use Hypersynth for chord foundations and FM Synth for detailed melodic elements
- Create complementary sounds by designing FM timbres that sit well with Hypersynth chords
- Use similar modulation patterns across both instrument types for cohesive movement
- Consider using Internal MIDI routing to have one track control both types of instruments

### Creating Cinematic Sound Effects with FM Synth

The FM Synth's complex modulation capabilities make it ideal for creating evolving cinematic sound effects, from subtle ambient textures to dramatic risers and impacts.

#### Cinematic Texture Design

1. **Ambient Drone Technique**:
   - Use algorithm 0B (A+B+C+D) for additive synthesis approach
   - Set operators with slightly detuned ratios (1.00, 0.99, 1.01, 2.00)
   - Apply minimal feedback to operators A and C
   - Use slow ADSR envelopes with long attack and release times
   - Add subtle vibrato with a slow LFO assigned to pitch

2. **Evolving Pad Technique**:
   - Use algorithm 04 ([A+B+C]>D) 
   - Set operator D to ratio 1.00 as the carrier
   - Set operators A, B, C to different harmonic ratios (1.00, 2.00, 3.00)
   - Assign MOD1 to slowly modulate the levels of operators A, B, C
   - Apply reverb and chorus effects for spaciousness

3. **Cinematic Riser**:
   - Use algorithm 01 ([A+B]>C>D)
   - Start with low ratios and increase them using a table or REP command
   - Set operators with increasing feedback values via automation
   - Use a slow attack envelope that reaches peak at the climax point
   - End with high resonance filter sweep for dramatic effect

#### Using Tables for Evolving FM Textures

Tables are crucial for creating sophisticated dynamic movement in FM sounds. Here are practical examples:

##### Example 1: Atmospheric Texture with Harmonic Evolution

```
Step | N   | V   | FX1    | FX2    | FX3
-----|-----|-----|--------|--------|--------
00   | +00 | 60  | RAT100 | RAT200 | LEV20
01   | +00 | 60  | RAT102 | RAT205 | LEV25
02   | +00 | 60  | RAT104 | RAT210 | LEV30
03   | +00 | 60  | RAT106 | RAT215 | LEV35
04   | +00 | 60  | RAT108 | RAT220 | LEV40
05   | +00 | 60  | RAT110 | RAT225 | LEV45
06   | +00 | 60  | RAT112 | RAT230 | LEV50
07   | +00 | 60  | RAT110 | RAT235 | LEV55
08   | +00 | 60  | RAT108 | RAT240 | LEV60
09   | +00 | 60  | RAT106 | RAT235 | LEV55
0A   | +00 | 60  | RAT104 | RAT230 | LEV50
0B   | +00 | 60  | RAT102 | RAT225 | LEV45
0C   | +00 | 60  | RAT100 | RAT220 | LEV40
0D   | +00 | 60  | TIC20  | FB040  | HOP00
```

This table creates a constantly shifting texture by:
- Gradually modifying the frequency ratios of operators A and B (RAT commands)
- Simultaneously changing the level of operator C (LEV command)
- Setting a slow table tick rate at row 0D (TIC20)
- Adding subtle feedback modulation (FB040)
- Looping back to the beginning (HOP00) for continuous evolution

The resulting sound will have a breathing, organically shifting quality perfect for atmospheric backgrounds.

##### Example 2: Cinematic Impact with Dramatic Decay

```
Step | N   | V   | FX1    | FX2    | FX3
-----|-----|-----|--------|--------|--------
00   | +00 | 7F  | LEV7F  | RAT100 | FB070
01   | +00 | 7D  | LEV7D  | RAT101 | FB068
02   | +00 | 7A  | LEV7A  | RAT102 | FB060
03   | +00 | 76  | LEV76  | RAT104 | FB058
04   | +00 | 70  | LEV70  | RAT108 | FB050
05   | +00 | 68  | LEV68  | RAT110 | FB048
06   | +00 | 60  | LEV60  | RAT120 | FB040
07   | +00 | 58  | LEV58  | RAT130 | FB038
08   | +00 | 50  | LEV50  | RAT140 | FB030
09   | +00 | 48  | LEV48  | RAT150 | FB028
0A   | +00 | 40  | LEV40  | RAT160 | FB020
0B   | +00 | 38  | LEV38  | RAT180 | FB018
0C   | +00 | 30  | LEV30  | RAT1A0 | FB010
0D   | +00 | 28  | LEV28  | RAT1C0 | FB008
0E   | +00 | 20  | LEV20  | RAT1E0 | FB000
0F   | +00 | 00  | TIC06  | ---    | ---
```

This table creates a cinematic impact sound that transforms as it decays:
- Starts with maximum volume and operator levels (7F)
- Gradually decreases volume and levels over time
- Simultaneously increases frequency ratios for harmonic evolution (RAT commands)
- Decreases feedback amount (FB commands) for a changing timbre
- Uses a moderately fast table speed (TIC06) for a dramatic but not too abrupt decay

This works particularly well with algorithm 02 ([A>B+A>C]>D) as it creates complex spectral movement during the decay. Trigger this with a low note for dramatic effect.

#### Advanced FM Sound Design Techniques

1. **Layered Cross-Modulation**:
   - Use two FM instruments on separate tracks
   - Create complementary modulation patterns
   - Use the TBX command to run auxiliary tables for additional complexity
   - Offset the tables slightly to create evolving phase relationships

2. **Morphing Technique**:
   - Start with a simple configuration (algorithm 00)
   - Create a phrase that changes the ALGO parameter over time
   - Use complementary tables to adjust operator parameters for each algorithm
   - This creates dramatic transformations perfect for transitions

3. **Randomized Textures**:
   - Use probability commands (CHA) in your tables
   - Apply small random modulations to ratios and feedback
   - This creates organic variation that prevents repetitive sounds
   - Particularly effective for ambient and atmospheric elements

### Mastering the Macrosynth

The Macrosynth in the M8 is based on the Mutable Instruments Braids module, offering 44 different synthesis models in a compact format. It includes synthesis methods covering classic analog, ring modulation, unison, hard-sync, vowel synthesis, FM, physical modeling, and drum synthesis. With just two main parameters (TIMBRE and COLOR) controlling different aspects depending on the selected shape, the Macrosynth is deceptively powerful.

#### Understanding the Macrosynth Architecture

1. **SHAPE Selection**: 
   - 44 different synthesis algorithms (called "shapes")
   - Each algorithm offers a unique synthesis method
   - Organized by categories (analog, FM, physical modeling, etc.)

2. **TIMBRE and COLOR Parameters**:
   - Functions change depending on the shape selected
   - TIMBRE typically controls spectral content or primary characteristic
   - COLOR typically controls harmonic structure or secondary characteristic

3. **Additional Processing**:
   - DEGRADE: Sample rate reduction for bit-crushing effects
   - REDUX: Bit depth reduction for digital artifacts
   - Standard filter, limiter, and effects routing

#### Advanced Macrosynth Techniques

1. **Shape Exploration Strategy**:
   - Group similar models for easier navigation (analog, percussion, vocal, etc.)
   - Create templates with different favorite shapes
   - Use TIMBRE and COLOR automation for dramatic transformations

2. **Unique Timbral Techniques**:
   - **Plucked Model Extreme**: Set the PLUCKED model to extremely low notes for unique percussion and glitch sounds
   - **Vocal Formants**: Use the VOWEL and VOWEL FOF models with subtle LFO modulation for eerily human textures
   - **Physical Modeling Manipulation**: The BOWED, BLOWN, and FLUTED shapes respond dramatically to different modulations

3. **Wave Paraphonic Mode**:
   - Use WAV PARAPHONIC shape for chord sounds on a single track
   - COLOR parameter selects between different chord types
   - Combine with slight detuning for rich pad sounds

4. **Percussive Sound Design**:
   - The KICK, SNARE, and CYMBAL models offer specialized drum synthesis
   - STRUCK BELL and STRUCK DRUM are excellent for metallic percussion
   - Layer these with samples for hybrid drum sounds

5. **Experimental Techniques**:
   - Use DIGITAL MOD model for glitchy, data-like textures
   - VOSIM and FORMANT models create unique vocal-like sounds
   - GRANULAR models produce evolving textures perfect for ambient music

#### Enhancing Macrosynth with Tables and Modulation

1. **Multi-stage Sound Evolution**:
   - Create tables that slowly adjust TIMBRE and COLOR values
   - Add filter sweeps synchronized with shape parameter changes
   - Use different tick rates for asynchronous modulation

2. **Morphing Between Models**:
   - Set up phrases that change the SHAPE parameter gradually
   - Use complementary tables that adjust parameters for smooth transitions
   - Particularly effective between related models (e.g., SAW SWARM to TRIPLE SAW)

3. **Macrosynth Strike Command**:
   - For percussive shapes like PLUCKED and KICK, use the Strike command to trigger without needing note retriggers
   - Useful for creating complex rhythmic patterns with sustained notes

#### Sample Macrosynth Table for Evolving Texture

```
Step | N   | V   | FX1      | FX2      | FX3
-----|-----|-----|----------|----------|--------
00   | +00 | 60  | TIM30    | COL40    | CUT80
01   | +00 | 60  | TIM35    | COL45    | CUT78
02   | +00 | 60  | TIM40    | COL50    | CUT76
03   | +00 | 60  | TIM45    | COL55    | CUT74
04   | +00 | 60  | TIM50    | COL60    | CUT72
05   | +00 | 60  | TIM55    | COL65    | CUT70
06   | +00 | 60  | TIM60    | COL70    | CUT68
07   | +00 | 60  | TIM65    | COL75    | CUT66
08   | +00 | 60  | TIM70    | COL80    | CUT64
09   | +00 | 60  | TIM75    | COL78    | CUT62
0A   | +00 | 60  | TIM80    | COL76    | CUT60
0B   | +00 | 60  | TIM75    | COL74    | CUT58
0C   | +00 | 60  | TIM70    | COL72    | CUT56
0D   | +00 | 60  | TIM65    | COL70    | CUT54
0E   | +00 | 60  | TIM60    | COL68    | CUT52
0F   | +00 | 60  | TIC10    | ---      | HOP00
```

This table creates a slowly evolving sound by:
- Gradually modifying the TIMBRE and COLOR parameters
- Simultaneously applying a subtle filter sweep
- Setting a moderate table tick rate (TIC10)
- Looping back to the beginning (HOP00) for continuous evolution

### Mastering Limiter Settings and DJ Filter Automation

The M8 offers comprehensive mixing and mastering capabilities through its mixer, limiter, and DJ filter systems.

#### Understanding the Instrument and Global Limiters

The M8 has two levels of limiters that work together to shape your sound:

1. **Per-Instrument Limiter (LIM Parameter)**:
   - Found in each instrument's settings
   - Controls how an individual instrument handles amplitude clipping
   - Multiple modes available:
     - **CLIP**: Hard clipping (digital distortion)
     - **SIN**: Sine waveshaper (smoother clipping)
     - **FOLD**: Wavefolding (harmonically rich distortion)
     - **WRAP**: Wraparound (digital artifact effect)
     - **POST**: Apply after filter stage with hard clipping
     - **POST:AD**: Post-filter soft clipping/analog drive
     - **POST:W1-W2**: Post-filter folding distortions

2. **Global Mixer Limiter**:
   - Found in the Mixer View and Limiter & Mix Scope View
   - Protects the master output from clipping
   - Features variable attack and release parameters
   - Shows visual feedback of compression activity

#### Proper Instrument Limiter Usage

1. **Creative Sound Design**:
   - Use FOLD and WRAP modes for experimental textures
   - SIN provides smoother distortion for bass sounds
   - POST modes allow filtering before distortion for controlled results

2. **Gain Staging Strategy**:
   - Start with conservative AMP values (40-80)
   - Choose limiter modes based on instrument type:
     - Bass: CLIP or SIN for controlled low end
     - Leads: FOLD for harmonically rich sustain
     - Percussion: POST for punchy attacks
   - Adjust volume in the mixer view after setting instrument levels

3. **Layer-Specific Approaches**:
   - For drum sounds, use CLIP for punchy transients
   - For melodic content, SIN or FOLD provides musical distortion
   - For atmospheric effects, WRAP creates unique textures

#### Optimizing the Global Limiter

The global limiter is crucial for achieving professional loudness without distortion. Access its detailed settings through the Limiter & Mix Scope View.

1. **Setting Appropriate Thresholds**:
   - Start with modest limiting (LIM values of 20-40)
   - Watch the white line on the MIX meter to monitor compression
   - Aim for occasional limiting on peaks rather than constant compression

2. **Attack and Release Timing**:
   - For punchy drums: Fast attack (ATK 10-20), medium release (REL 30-50)
   - For smooth mixes: Medium attack (ATK 20-40), slow release (REL 50-80)
   - Auto release mode (REL 00) works well for varied material

3. **Monitoring Best Practices**:
   - Use the PEAK meter to check maximum levels
   - Regular visual monitoring of the Mix Scope helps avoid excessive compression
   - Clear the peak display ([EDIT]+[OPTION] on PEAK) to check new maximum levels after adjustments

#### DJ Filter Techniques and Automation

The DJ filter is a powerful performative and compositional tool that can be controlled in several ways:

1. **DJ Filter Basics**:
   - Found in the Mixer View (DJF parameter)
   - Value of 80 is neutral (no filtering)
   - Values below 80 engage lowpass filtering (gradually cutting high frequencies)
   - Values above 80 engage highpass filtering (gradually cutting low frequencies)
   - Can be set to different filter types (lowpass/highpass, lowpass/bandstop, bandstop/highpass)

2. **Automation Methods**:
   - **Command-based**: Use the DJF command in phrase or table for precise pattern-locked automation
   - **MIDI Mapping**: Assign external MIDI CC to the DJF parameter for live control
   - **Touchscreen**: Map the X or Y axis of the touchscreen to DJF for tactile control
   - **Table-based**: Create elaborate filter sweeps using tables with gradual value changes

3. **Creative Applications**:
   - **Buildups**: Gradually increase from 80 toward FF (highpass) to remove bass before drops
   - **Breakdowns**: Gradually decrease from 80 toward 00 (lowpass) for mellow sections
   - **Transitions**: Create smooth movement between sections with synchronized filter sweeps
   - **Rhythmic effects**: Use rapid filter changes on specific beats for dynamic variation

4. **DJF Automation Example (16-step buildup)**:

```
Step | FX Column Command
-----|------------------
00   | DJF80 (Neutral)
01   | ---
02   | DJF88
03   | ---
04   | DJF90
05   | ---
06   | DJF98
07   | ---
08   | DJFA0
09   | ---
0A   | DJFA8
0B   | ---
0C   | DJFB0
0D   | ---
0E   | DJFC0
0F   | DJFF0 (Maximum highpass)
```

This creates a gradual filter sweep that removes low frequencies over 16 steps, perfect for buildups before drops or transitions between sections.

#### Integration with Performance Workflows

1. **Live Mode Techniques**:
   - Create dedicated filter control sections in your song
   - Use mute groups with filter automation for dramatic breakdowns
   - Combine filter sweeps with volume automation for complete transitions

2. **Song Snapshot with Filter States**:
   - Use [SHIFT]+[OPTION] in the Mixer View to create snapshots of different filter settings
   - Recall with [SHIFT]+[EDIT] during performance
   - Useful for quick transitions between different mix states

3. **Multi-parameter Automation**:
   - Combine DJF automation with VCH/VDE/VRE (effect volume) commands
   - Automate both cutoff and resonance for more dramatic filter sweeps
   - Link filter movement with bass volume for cohesive mix changes

### Final Tips

- **CPU optimization**: Convert stereo samples to mono when possible, especially for sounds without important stereo information
- **Boot template**: Save a template song to `/System/TEMPLATE.m8s` to start with your preferred settings
- **Table efficiency**: Tables can be shared between instruments to create modulation libraries
- **Instrument organization**: Group instruments by type or function for easier navigation
- **Modulation routing**: Configure modulators to control other modulators for complex parameter evolution

## Resources

For further exploration:
- Official M8 manual and firmware from the [DirtyWave website](https://dirtywave.com/pages/resources-downloads)
- Community documentation at [team.indiedemos.com](https://team.indiedemos.com/@tom-avatars/dirtywave-m8-ressources/community-documentation-4)
- Tutorial videos by [RedMeansRecording](https://youtu.be/QYeM4Dx2kGU?si=L0KEUb5fpicQo3LC)
- Official [Discord server](https://discord.gg/WEavjFNYHh)
