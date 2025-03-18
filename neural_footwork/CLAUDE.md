# Neural Footwork Project Configuration

## Common Commands
- Open main patch: `open neural_footwork_v2.pd`
- Audio setup: In Pure Data, go to Media > Audio Settings and set buffer size to 256-512

## Code Style Preferences
- Namespace prefixes:
  - Main patch: `$0-` (local to patch)
  - ambient: `ambient-`
  - hihat: `hihat-`
  - snare: `snare-`
  - tom: `tom-`
  - mixer: `mixer-`
  - fx: `fx-`
  - neural: `neural-`

## Project Structure
- **neural_footwork_v2.pd**: Main patch
- **abstractions/**: Contains all reusable modules
- **instrument patches**: ambient_v2.pd, hihat_v2.pd, snare_v2.pd, tom_v2.pd
- **processing**: neural_mixer.pd, brain.pd, gen_fx.pd

## Common Issues & Fixes
- "multiply defined" - Use proper namespace prefixes
- "audio signal outlet connected to nonsignal inlet" - Fix signal routing
- "noise~: no method for 'bang'" - Add line~ or metro objects before noise~
- "error opening audio: Internal PortAudio error" - Adjust buffer size in Media > Audio Settings