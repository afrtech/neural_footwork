NEURAL FOOTWORK GENERATIVE SYSTEM v2.0
=====================================

An advanced Pure Data patch with 4 neural network-controlled channels (ambient + 3 drums),
generative techniques, mutable mixer, and Digitakt sampling prep.

INSTALLATION
-----------
1. Extract this zip to any location on your computer
2. Open the file 'neural_footwork_v2.pd' with Pure Data (Pd) version 0.51+ (vanilla)
3. Connect your Digitakt or other MIDI controller via USB or MIDI interface
4. Configure your audio settings in Pure Data (Media > Audio Settings)
   - Recommended: 44.1kHz sample rate, buffer size 64-256 samples
   - Check "start DSP" or click the "compute audio" toggle in Pd

OPERATING INSTRUCTIONS
--------------------

BASICS:
- The system starts automatically when opening the main patch
- The mixer section displays VU meters for each channel
- Click the channel name toggles to mute/unmute channels manually
- Green lights indicate active neural activity
- The main UI is divided into channels, mixer, effects, and brain sections

NEURAL CONTROLS:
1. Brain State:
   - The brain module processes all neural interactions
   - Neural activity is visible through the flashing lights
   - Cross-inhibition causes channels to interact rhythmically
   - Use Program Change 2 to randomize the neural weights for new patterns

2. Channel Control:
   - Each channel has its own neural network
   - Adjust feedback gain with CC1 for ambient, or manual sliders
   - Threshold controls determine when neurons "fire"
   - Observe inhibition patterns between channels

3. Generative Controls:
   - DNA mutation rate affects rhythm evolution speed (more = faster changes)
   - Fractal mode (PC1) activates chaotic oscillators
   - Apply more feedback for more unpredictable patterns
   - Chaos rate (CC5) controls the chaotic behavior of the snare

PERFORMANCE TECHNIQUES:
1. Manual Operation:
   - Start by enabling all channels
   - Use mouse clicks on channel toggles for basic muting
   - Adjust sliders manually to control feedback levels
   - Watch the neural activity and respond to emergent patterns

2. Digitakt Integration:
   - Connect your Digitakt via MIDI USB or interface
   - Ensure MIDI channel matches (default = all channels)
   - Use Trigs 1-4 to control channel mutes (C1-D#1 notes)
   - Hold FUNC (note 64) and press Trig 1 to activate mute group 1
   - Hold FUNC and press Trig 2 to activate mute group 2
   - Use Program Changes for special functions:
     * PC1: Toggle fractal mode (affects all oscillators)
     * PC2: Randomize neural weights (creates new patterns)
     * PC3: Freeze delay buffers (creates stutter/freeze effects)

3. Parameter Control:
   - Map Digitakt knobs to the following CCs:
     * Knob A (CC1): Ambient feedback gain
     * Knob B (CC2): Delay time
     * Knob C (CC5): Chaos rate (affects snare/percussion)
     * Knob D (CC64): Plasticity amount (neural connections)
   - Experiment with parameter locks on the Digitakt to create variations

4. Mute Groups:
   - Group 1 (FUNC+Trig1): Mutes ambient + hihat for drops
   - Group 2 (FUNC+Trig2): Mutes snare + tom for breakdowns
   - Combine with parameter changes for dramatic transitions

SAMPLING WORKFLOW
---------------
1. Design your sound with the neural networks:
   - Create interesting patterns through neural interactions
   - Use CC control to find sweet spots in the system
   - Utilize mute groups to create arrangement variations

2. Record to Digitakt:
   - Method 1 - Direct Sampling:
     * Connect audio output to Digitakt's inputs
     * Sample directly into Digitakt tracks
     * Use Digitakt's sampling workflow

   - Method 2 - Export Rack:
     * Press Trig 5 (E1) on Digitakt to trigger recording
     * The system will record all channels separately
     * Files are saved in the 'samples' folder as WAV files
     * Load these files into Digitakt

3. Export Options:
   - Full mix: stereo file with all channels
   - Individual channels: separate files for each voice
   - Use the files directly or as source material
   - Auto-sliced files can be loaded into Digitakt's slice mode

ADVANCED TECHNIQUES
-----------------
1. Neural Plasticity:
   - The system features evolving neural connections
   - Control plasticity rate with CC64
   - Higher values create more variation over time
   - Lower values maintain stable patterns

2. Cross-Inhibition:
   - Channels can inhibit each other through neural connections
   - This creates emergent rhythmic relationships
   - Watch for patterns where one channel "gates" another
   - Use this for complex interlocking rhythms

3. DNA Mutations:
   - Rhythm patterns evolve over time using DNA algorithms
   - Control mutation rate with dedicated control
   - Each channel has its own genetic rhythm pattern
   - Allow to run for extended periods to observe evolution

4. Neural Effects:
   - Effects parameters are controlled by neural activity
   - Delay times adjust dynamically based on neural state
   - Reverb characteristics respond to system activity
   - Bitcrusher depth varies with neural patterns

TROUBLESHOOTING
-------------
- If no sound, check audio settings and DSP is enabled
- If MIDI doesn't work, verify MIDI settings and connections
- If patterns seem stuck, use PC2 to randomize neural weights
- If CPU usage is high, increase buffer size or disable channels
- If neurons aren't firing, increase feedback or threshold values

SYSTEM ARCHITECTURE
-----------------
- 4 independent channels with neural networks and generative algorithms
- Advanced neural brain with inhibitory connections and plasticity
- DNA-based rhythm generators that mutate over time
- Fractal LFOs using Mandelbrot/Julia formulas
- Channel 1: Ambient textures with Markov chain melodies and granular processing
- Channels 2-4: Percussion voices with DNA/generative rhythm generators
- Neural feedback matrix connecting all channels with cross-inhibition
- Effects section with neuroverb, bitnuke, and gen_fx processors
- Enhanced mixer with mute groups and stereo rivalry
- Per-channel export with auto-slicing for Digitakt

NEURAL NETWORK FEATURES
---------------------
- Static-weight neurons with nonlinear response
- Inhibitory connections between channels 
- Self-oscillating neurons for ambient textures
- Neural plasticity that modulates connections over time
- Brain section with cortex, synapses, and plasticity modules

GENERATIVE FEATURES
-----------------
- Stochastic sequencers with Markov chains
- DNA-based rhythms with mutation properties
- Logistic map chaos generators
- Fractal LFOs using Mandelbrot/Julia set formulas
- Granular cloud processor with neural modulation

MIDI MAPPING REFERENCE
--------------------
DIGITAKT MAPPINGS:
- Trig 1 (Note C1/36): Mute/unmute Channel 1 (Ambient)
- Trig 2 (Note C#1/37): Mute/unmute Channel 2 (Hihat)
- Trig 3 (Note D1/38): Mute/unmute Channel 3 (Snare)
- Trig 4 (Note D#1/39): Mute/unmute Channel 4 (Tom)
- Trig 5 (Note E1/40): Record audio buffer
- FUNC (Note 64) + Trig 1: Activate Mute Group 1 (Ambient + Hihat)
- FUNC (Note 64) + Trig 2: Activate Mute Group 2 (Snare + Tom)

CC CONTROLS:
- CC1: Ambient channel feedback gain
- CC2: Delay time
- CC5: Chaos LFO rate
- CC64: Modulation 1 (Plasticity)
- CC65: Modulation 2 (unused)
- CC66: Modulation 3 (unused)
- CC67: Modulation 4 (unused)

PROGRAM CHANGES:
- PC1: Activate fractal LFOs
- PC2: Randomize all neural weights
- PC3: Freeze delay buffers

For updates and questions, contact the author.

© 2025