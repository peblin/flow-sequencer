  # Flow - 7-pattern, multi-channel, 16x8 step midi looper & sequencer for Mozaic by peblin.
  Featuring:

  - 16 steps with 8 subdivisions (parts) each
  - 6 voice polyphony per part
  - 7 patterns, with midi channel configurable per pattern
  - From 1/32 to 2 bar step length giving 1/2 to 16 bar patterns
  - Live & step recording
  - Live recording stores note duration and timing for (almost) exact playback
  - Individual step / part editing, including voices, probability and duration
  - Note probability & duration can be set per part
  - Transpose mode
  - Patterns play solo or multi - easily toggle patterns ON/OFF for live performance
  - 3 quantization modes for live recording - None (as played), per part, per step

-- Basics --

Flow's sequencer consists of 16 steps per pattern. Each step is divided into 8 parts - so each part is 1/8 of step length. For example, setting step length using the Step knob to 1 bar, makes each part of the step a 1/8th note.

To get started, just start the host and start playing - the sequencer records whatever you play into the appropriate part and plays is back just as you played it. Double-tap to erase steps & parts, and single-tap on a step to edit its parts.

The sequencer has 4 views;
- Steps; each pad is a step. When a step has parts with notes, the pad will show the number of voices allocated per part in the step. T
- Step edit; shows one row of steps and the other row the parts of the step being edited. Accessed by tapping or holding a pad in Steps view.
- Part edit; shows faders for all voices, note time and probability of a part. Accessed by tapping ⬆️SHIFT when in step edit view.
- Control panel; top row of pads are sequencer controls, bottom row are ARM/ON/OFF toggles for the 7 patterns. Accessed by tapping SHIFT in the Steps view. Exit by tapping SHIFT again.

-- Recording --

Record into the sequencer using either live recording or step recording.

--- Live recording & Quantization ---

In this mode the sequencer records notes, velocities and (optionally) duration into the corresponding part. Live recording has three quantization modes - None, Part and Step. Set the quantisation mode by tapping the Quant button in Control Panel - it cycles between the modes.

- None; This aims to reproduce what you played as close to the original as possible. It keeps the timing of your playing by keeping track of the delay of the "note on" message to when the part started and will delay any playback with the same amount. The accuracy of the delay is 5 milliseconds for now.
- Part; This will quantize to nearest part (pushing note forward to next part if that is closer in time)
- Step; This will quantize to nearest step (pushing note forward to next step if its within 25% of the next step in time)

The sequencer has 6 voice polyphony per part, but only stores timing latency "per step", not "per voice" so any additional voices will play in sync with the first voice of the part.

--- Step recording ---

In this mode you select which step/part to edit, then play up to 6 notes for it. When editing a step, you're actually editing the first part of the step. 

The sequencer supports both "latched" and "hold pad" editing. 
- Latched; Simply tap the step you want to edit, then tap the part from all parts showing on the row above or below the chosen step. Finish recording/editing by tapping the step again, which is now labeled "✅ Done".
- Hold pad; Hold the step you want to edit, then tap the part from all parts showing on the row above or below the chosen step. Finish by releasing the held pad. 

Latched is really helpful on iPhone, while "hold pad" might be quicker on the iPad.

-- Deleting parts or full steps --

To delete a part or all parts in a step, double-tap the step or part pad. 

-- Editing part contents --

When in step edit mode, if you select a part and then press SHIFT you will enter "part edit" mode. Part edit mode shows all 6 voices, note duration and probability.

Drag faders to adjust notes. If you drag a previously unused voice it'll be added to the part - so you can for example add a seventh to a triad chord after recording. Or, tap a bass rythm and then afterwards dial in the desired notes.

It's not super-easy to hit the right note when dragging the fader - suggestions for improved UX welcome.

-- Part durations --

The knob "note time" sets the default note duration both for live and step recording. Note duration is measured as "percentage of step length". Thus, a note duration of 200% with the sequencer set to "1/8" will give 1/4th notes. This also means that if you change step length for the sequencer, the note durations will scale accordingly.

Note duration knob defaults to "As played", meaning that the sequencer will use your playing (converted to a percentage of step length) as duration.

-- Part probabilities --

The probability knob sets the default probability for step-sequenced parts. You can also change the part probability using either the probability knob when step recording, or the probability fader in part edit view.

-- Pattern Midi Channel --

Each pattern can have its own midi channel for sending notes. Set the channel using the Midi CH knob and enjoy.

-- Play modes --

The sequencer can play each pattern SOLOed, or multiple patterns simultaneously. Toggle play mode with the "Play" button in the Control Panel.

--- Play: Solo ---

Only one pattern plays at a time and the playing pattern is also armed for recording. Change to the desired pattern in the Control Panel.

--- Play: Multi ---

Multiple patterns can play simultaneously, either on the same midi channel or using several depending on the midi channel setting for each pattern.

Toggle patterns ON/OFF in the Control Panel. Single-tapping on a pattern will toggle it ON/OFF and make it the armed pattern. Long-pressing on a pattern (tap and hold for approx 200ms+) will arm it, but not toggle the ON/OFF state. This way you can switch between editing different playing patterns without interrupting playback.

-- Transpose mode --

With transpose active, the sequencer will stop live recording and treat incoming midi notes as "pitch offset", with C3/midi note 48 as base pitch. So, playing G3 will transpose +7 semitones, while a B2 will transpose -1.

Transpose is applied to all outgoing notes - so in Play:Multi all playing patterns will be transposed. This behaviour might change in the future - suggestions welcome.

-- Copying patterns --

To copy a pattern, first make sure it's the armed pattern then press "Copy Pattern" in Control Panel. Then select the pattern to copy to. Everything except midi channel will be copied.

-- Clearing patterns --

"Clear armed" will clear the currently armed pattern, except for midi channel.
"Clear all" will clear all patterns. To prevent accidental disaster, both clear buttons requires you to long-press on the button.

- THANKS -

  Inspired by OP-Z and https://patchstorage.com/infinity
  Thanks to -ki for https://patchstorage.com/pad-manager-include and great contributions to the community

  And most of all thanks to Bram Bos for creating one of the most game-changing iOS music apps ever.
