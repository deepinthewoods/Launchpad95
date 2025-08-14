# Tech Stack and Architecture

## Technology Stack
- **Language**: Python 2/3 (compatible with Ableton Live's Python interpreter)
- **Framework**: Ableton Live _Framework modules
- **Platform**: Cross-platform (Windows, macOS)
- **Deployment**: Ableton Live Remote Scripts folder

## Architecture
The project follows Ableton Live's Component-based remote script architecture:

### Core Files
- `__init__.py` - Entry point with device capabilities and instance creation
- `Launchpad.py` - Main controller class
- `Settings.py` - Configuration settings

### Component Structure
- **Button Elements**: Custom button and slider implementations
- **Session Components**: Enhanced session view functionality 
- **Step Sequencer**: MIDI clip editing components
- **Device Controller**: Parameter control components
- **Instrument Controller**: Push-like instrument functionality
- **Scale Components**: Musical scale support

### Key Components
- `SpecialSessionComponent.py` - Enhanced session view
- `StepSequencerComponent.py` / `StepSequencerComponent2.py` - Step sequencing
- `DeviceControllerComponent.py` - Device parameter control
- `InstrumentControllerComponent.py` - Instrument mode
- `ScaleComponent.py` - Musical scales
- `NoteEditorComponent.py` - Note editing functionality

### Utilities
- `Log.py` - Logging functionality for debugging
- `SkinMK1.py` / `SkinMK2.py` - Color schemes for different models
- `ColorsMK1.py` / `ColorsMK2.py` - Color definitions

## No Traditional Build System
This project doesn't use typical Python development tools like pip, setuptools, or requirements.txt because it's designed to run within Ableton Live's environment.
