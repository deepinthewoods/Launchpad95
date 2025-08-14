# Code Style and Conventions

## Python Style
The codebase follows a mix of Python 2/3 compatibility patterns:

### Import Style
```python
from __future__ import absolute_import, division, print_function, unicode_literals
```

### Compatibility Handling
- Uses `past.utils.old_div` for Python 2/3 division compatibility
- Graceful fallback for missing dependencies

### Class Structure
- Components inherit from Ableton's _Framework base classes
- Use of SlotManager pattern for event handling
- Component-based architecture with clear separation of concerns

### Naming Conventions
- **Classes**: PascalCase (e.g., `ButtonSliderElement`, `StepSequencerComponent`)
- **Variables**: snake_case (e.g., `_last_sent_value`, `button_slots`)
- **Constants**: UPPER_SNAKE_CASE (e.g., `SESSION__STOP_BUTTONS`, `VELOCITY_THRESHOLD_MAX`)
- **Private attributes**: Leading underscore (e.g., `_buttons`, `_parameter_value_slot`)

### Configuration Style
- Settings organized in a single `Settings` class
- Boolean flags with descriptive comments
- Experimental features clearly marked
- Tunable parameters with sensible defaults

### Documentation
- Minimal docstrings (following Ableton Live script conventions)
- Inline comments for complex logic
- Configuration options well-documented in Settings.py

### Error Handling
- Graceful handling of optional dependencies
- Try/except blocks for OS-specific operations
- Fallback implementations when possible

## File Organization
- One class per file (generally)
- Related functionality grouped in components
- Separate skin/color files for different hardware models
- Utilities separated into dedicated modules

## No Formal Style Guidelines
The project doesn't use formal Python style tools like Black, flake8, or pylint, following Ableton Live's remote script conventions instead.
