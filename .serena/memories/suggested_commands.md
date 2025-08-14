# Suggested Shell Commands for Windows

## Basic File Operations
- `dir` - List directory contents (equivalent to `ls` on Unix)
- `cd <directory>` - Change directory
- `type <file>` - Display file contents (equivalent to `cat` on Unix)
- `findstr <pattern> <file>` - Search for patterns in files (equivalent to `grep` on Unix)
- `copy <source> <destination>` - Copy files
- `move <source> <destination>` - Move/rename files
- `del <file>` - Delete files
- `rmdir <directory>` - Remove empty directories
- `rmdir /s <directory>` - Remove directories recursively

## Git Commands
- `git status` - Check repository status
- `git add .` - Stage all changes
- `git commit -m "message"` - Commit changes
- `git push` - Push to remote repository
- `git pull` - Pull from remote repository
- `git log --oneline` - View commit history
- `git diff` - View changes

## Project Specific Commands

### Installation/Deployment
Since this is an Ableton Live remote script, there are no build or install commands. The script is deployed by:
1. Copying the entire project folder to Ableton Live's Remote Scripts directory
2. Typical path: `%USERPROFILE%\\AppData\\Roaming\\Ableton\\Live [version]\\Preferences\\User Remote Scripts\\`

### Testing
- No automated testing framework is configured
- Testing is done manually in Ableton Live with actual hardware

### Debugging
- Enable logging by setting `Settings.LOGGING = True`
- Log file location: `%USERPROFILE%\\Documents\\Ableton\\User Library\\Remote Scripts\\log.txt`
- Use `type "%USERPROFILE%\\Documents\\Ableton\\User Library\\Remote Scripts\\log.txt"` to view logs

### Development Workflow
1. Edit Python files in the project
2. Save changes
3. Restart Ableton Live to reload the script
4. Test with Launchpad hardware

## Python Commands (if needed)
- `python -c "import sys; print(sys.version)"` - Check Python version
- `python -m py_compile <file>` - Check syntax of Python file

## Notes
- This project doesn't use standard Python development tools
- No pip, virtualenv, or package management needed
- Development is done directly in Ableton Live environment
- File operations should be done carefully as this affects a live music production environment
