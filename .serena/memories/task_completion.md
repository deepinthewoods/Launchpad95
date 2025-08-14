# Task Completion Guidelines

## When a Development Task is Completed

### 1. Code Quality Check
- Ensure Python syntax is valid using `python -m py_compile <modified_files>`
- Verify imports are correct and follow the project's compatibility patterns
- Check that new code follows the established naming conventions

### 2. Integration Testing
Since this is an Ableton Live remote script, testing must be done in the target environment:

1. **Deploy to Ableton Live**:
   - Copy the modified script to the Remote Scripts directory
   - Path: `%USERPROFILE%\\AppData\\Roaming\\Ableton\\Live [version]\\Preferences\\User Remote Scripts\\Launchpad95\\`

2. **Restart Ableton Live**:
   - Close Ableton Live completely
   - Restart to reload the remote script

3. **Configure Hardware**:
   - Connect Launchpad hardware
   - In Live Preferences > Link/MIDI, set Launchpad as Control Surface
   - Set script to "Launchpad95"

4. **Manual Testing**:
   - Test core functionality (session view, step sequencer, device control)
   - Verify new features work as expected
   - Check that existing functionality wasn't broken

### 3. Debugging Support
If issues are encountered:

1. **Enable Logging**:
   - Set `Settings.LOGGING = True`
   - Restart Ableton Live
   - Reproduce the issue

2. **Check Log File**:
   - Location: `%USERPROFILE%\\Documents\\Ableton\\User Library\\Remote Scripts\\log.txt`
   - Use `type` command to view: `type "%USERPROFILE%\\Documents\\Ableton\\User Library\\Remote Scripts\\log.txt"`

3. **Debug Steps**:
   - Check for Python errors in log
   - Verify MIDI communication
   - Test with different Launchpad models if available

### 4. Documentation Updates
- Update relevant comments in code
- If new settings are added, document them in `Settings.py`
- Consider updating the manual if significant features are added

### 5. Version Control
```bash
git add .
git status  # Review changes
git commit -m "Descriptive commit message"
git push    # If working with a remote repository
```

## No Automated Testing
- This project doesn't have unit tests or automated testing
- All testing is manual and requires Ableton Live + hardware
- Focus on thorough manual testing across different use cases

## Deployment Notes
- Changes take effect only after restarting Ableton Live
- Multiple Launchpad models may behave differently
- Test with actual MIDI hardware when possible
- Consider backwards compatibility with older Ableton Live versions
