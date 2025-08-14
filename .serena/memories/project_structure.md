# Project Structure

## Directory Layout
```
Launchpad95/
├── .serena/                    # Serena configuration
├── M4LDevice/                  # Max for Live device (optional)
│   └── Launchpad95OSDHelper.amxd
├── web/                        # Documentation and images
│   ├── index.html
│   ├── Manual_Launchpad95_FR.pdf
│   └── *.png                   # Setup instruction images
├── __init__.py                 # Entry point
├── Launchpad.py               # Main controller class
├── Settings.py                # Configuration settings
├── Log.py                     # Logging utility
└── [Component Files]          # Various component implementations
```

## Core Files
- **`__init__.py`** - Entry point defining device capabilities and creating controller instance
- **`Launchpad.py`** - Main controller class coordinating all functionality
- **`Settings.py`** - Centralized configuration with feature flags and parameters

## Component Categories

### Session Components
- `SpecialSessionComponent.py` - Enhanced session view functionality
- `SpecialProSessionComponent.py` - Professional session features  
- `SpecialProSessionRecordingComponent.py` - Recording enhancements
- `ClipSlotMK2.py` - Clip slot implementations for MK2

### Step Sequencer
- `StepSequencerComponent.py` - Main step sequencer implementation
- `StepSequencerComponent2.py` - Alternative/enhanced step sequencer
- `NoteEditorComponent.py` - Note editing functionality

### Controllers
- `DeviceControllerComponent.py` - Device parameter control
- `DeviceControllerStrip.py` - Parameter strip management
- `DeviceControllerStripProxy.py` - Strip proxy functionality
- `DeviceControllerStripServer.py` - Strip server implementation
- `InstrumentControllerComponent.py` - Instrument mode controller
- `TrackControllerComponent.py` - Track control functionality

### UI Elements
- `ButtonSliderElement.py` - Custom button slider implementation
- `PreciseButtonSliderElement.py` - High-precision button slider
- `ConfigurableButtonElement.py` - Configurable button functionality

### Selectors and Navigation
- `MainSelectorComponent.py` - Main mode selection
- `SubSelectorComponent.py` - Sub-mode selection
- `NoteSelectorComponent.py` - Note selection for editing
- `LoopSelectorComponent.py` - Loop region selection
- `TargetTrackComponent.py` - Track targeting

### Utilities and Styling
- `SkinMK1.py` / `SkinMK2.py` - Visual styling for different models
- `ColorsMK1.py` / `ColorsMK2.py` - Color definitions
- `ScaleComponent.py` - Musical scale support
- `NoteRepeatComponent.py` - Note repeat functionality
- `SpecialMixerComponent.py` - Enhanced mixer functionality

### Other Components
- `DefChannelStripComponent.py` - Default channel strip
- `M4LInterface.py` - Max for Live integration interface
- `consts.py` - Constants and shared definitions

## External Resources
- **M4LDevice/**: Optional Max for Live device for enhanced functionality
- **web/**: Documentation, manual, and setup instruction images
