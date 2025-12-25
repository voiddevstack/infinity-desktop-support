# Infinity Desktop Support

Welcome to the Infinity Desktop support repository! This repository is your go-to place for getting help, reporting issues, and learning how to use the Infinity Desktop IDE.

## What is Infinity Desktop?

Infinity Desktop is a powerful, multi-language code editor and execution environment built with Electron. It provides a VSCode-like experience with integrated code execution capabilities for multiple programming languages.

## Getting Started

### Installation

1. Download the latest release from the [releases page](https://stackhub.app/)
2. Install the application for your operating system (we only support macOS currently)
3. Launch Infinity Desktop

### Creating Your First Workspace

1. Click the **"Create Workspace"** button or select "New" from the workspace dropdown
2. Enter a workspace name (e.g., "My First Project")
3. Select a programming language:
   - **JavaScript/TypeScript**: Node.js projects with package.json
   - **Python**: Python projects with requirements.txt
   - **Golang**: Go modules with proper package structure
4. Choose a template (optional) - templates provide starter code and project structure
5. Select a runtime version (Free tier: LTS versions only, Pro tier: All versions)
6. Click **"Create Workspace"**

The IDE will automatically:
- Download the required runtime if needed
- Create the project structure
- Set up configuration files
- Open the entry file in the editor

### Running Your Code

1. Open the file you want to execute (or set it as the entry file)
2. Write your code in the Monaco editor
3. Click the **"Run"** button (▶️) in the toolbar
4. View the output in the output panel at the bottom

**Keyboard Shortcuts:**
- `Cmd/Ctrl + S`: Save current file
- `Cmd/Ctrl + R`: Run code
- `Cmd/Ctrl + Shift + P`: Command palette
- `Cmd/Ctrl + ,`: Open settings

## Common Features

### File Explorer

The file explorer provides a VSCode-style tree view of your workspace:

- **Create Files/Folders**: Use the "+ New File" or "+ New Folder" buttons, or right-click in the explorer
- **Rename**: Right-click a file/folder → "Rename" or press `F2`
- **Delete**: Right-click → "Delete" or press `Delete` key
- **Set Entry File**: Right-click a file → "Set as Entry File" (marked with ⭐)
- **Search**: Use the search bar at the top to filter files
- **Keyboard Navigation**: Use arrow keys to navigate, Enter to open files

### Tabbed Editor

- **Open Multiple Files**: Click files in the explorer to open them in tabs
- **Switch Between Files**: Click tabs or use `Cmd/Ctrl + Tab`
- **Close Tabs**: Click the X button on a tab, or use `Cmd/Ctrl + W`
- **Unsaved Changes**: Files with unsaved changes show a dot (•) indicator
- **Save All**: `Cmd/Ctrl + K, S` (or use File menu)

### Code Execution

- **Entry File**: The entry file (marked with ⭐) is executed when you click Run
- **Auto-Save**: Current file is automatically saved before execution
- **Output Panel**: Execution results, errors, and logs appear in the output panel
- **Stop Execution**: Click the "Stop" button (🛑) to cancel running code
- **Execution Time**: Shows how long the code took to execute

### Database Connections

Infinity Desktop supports connecting to external databases:

1. Open the database connection dialog (Settings → Database Connections)
2. Configure your connection:
   - **PostgreSQL**: Host, port, database, username, password
   - **MySQL**: Host, port, database, username, password
   - **SQL Server**: Host, port, database, username, password, encryption
3. Test the connection
4. Save and use in your projects

### Settings

Customize your IDE experience:

- **Theme**: Light or Dark mode
- **Font Size**: Adjust editor font size
- **Runtime Preferences**: Default runtime versions per language

## Frequently Asked Questions (FAQs)

### General Questions

**Q: What operating systems are supported?**
A: Infinity Desktop supports macOS.

**Q: Is Infinity Desktop free?**
A: Yes! Infinity Desktop has a free tier with access to LTS (Long Term Support) runtime versions. A Pro tier is available with access to all runtime versions and additional features.

**Q: Do I need to install programming languages separately?**
A: No! Infinity Desktop automatically downloads and manages language runtimes. You don't need to install Node.js, Python or Go separately.

**Q: Can I use Infinity Desktop offline?**
A: Yes, once runtimes are downloaded, you can work offline. However, you'll need internet access for:
- Initial runtime downloads
- Creating new workspaces with templates
- App updates

### Workspace Questions

**Q: Where are my workspaces stored?**
A: Workspaces are stored in `~/.infinity-desktop/workspaces/` (or `%APPDATA%\infinity-desktop\workspaces` on Windows). Each workspace has a unique ID and contains all your project files.

**Q: Can I import existing projects?**
A: Currently, you need to create a new workspace and copy your files into it. We're working on import functionality for future releases.

**Q: How do I delete a workspace?**
A: You can delete workspace files manually from the file system, or use the workspace management features in the IDE (coming soon).

**Q: Can I share workspaces between computers?**
A: Yes! You can copy the workspace folder from `~/.infinity-desktop/workspaces/{workspace-id}/` to another computer. Make sure both computers have the same runtime versions installed.

### Code Execution Questions

**Q: Why is my code not running?**
A: Common issues:
- Make sure you've set an entry file (marked with ⭐)
- Check that the entry file has valid code for the selected language
- Verify the runtime is downloaded (check Settings → Runtimes)
- Look at the output panel for error messages

**Q: How do I stop a running program?**
A: Click the "Stop" button (🛑) in the toolbar, or use `Cmd/Ctrl + C` in the output panel.

**Q: Can I run code with command-line arguments?**
A: Currently, code execution doesn't support command-line arguments. This feature is planned for future releases.

**Q: How do I see console output?**
A: All `console.log()` (JavaScript), `print()` (Python) and `fmt.Println()` (Go) output appears in the output panel at the bottom of the IDE.

### File Management Questions

**Q: How do I create a new file?**
A: Click the "+ New File" button in the file explorer, or right-click a folder → "New File". You can also use `Cmd/Ctrl + N`.

**Q: How do I rename a file?**
A: Right-click the file → "Rename", or select the file and press `F2`.

**Q: Can I drag and drop files?**
A: Yes! Pro tier users can drag and drop files and folders to reorganize their workspace structure.

**Q: How do I set which file runs when I click "Run"?**
A: Right-click any file → "Set as Entry File". The entry file is marked with a ⭐ indicator.

### Language-Specific Questions

**Q: Can I use npm packages in JavaScript projects?**
A: Yes! JavaScript workspaces include a `package.json` file. You can add dependencies, but you'll need to install them manually using the terminal or by adding them to `package.json`.

**Q: How do I use Python packages?**
A: Python workspaces include a `requirements.txt` file. Add your dependencies there and install them using `pip install -r requirements.txt` in a terminal.

**Q: Can I use Go modules?**
A: Yes! Golang workspaces are set up as Go modules with a `go.mod` file. You can use `go get` to add dependencies.

### Troubleshooting Questions

**Q: The app won't start. What should I do?**
A: 
1. Check if you have the latest version installed
2. Try restarting your computer
3. Check the application logs (location varies by OS)
4. Create an issue in this repository with details

**Q: Code execution is slow. Why?**
A: 
- First-time execution may be slower as the runtime initializes
- Large projects may take longer to start
- Check your system resources (CPU, memory)
- Try restarting the IDE

**Q: I'm getting "Runtime not found" errors.**
A: 
1. Go to Settings → Runtimes
2. Check if the runtime is downloaded
3. If not, click "Download" to install it
4. Verify you have internet connectivity

**Q: My files disappeared!**
A: 
- Files are stored in `~/.infinity-desktop/workspaces/`
- Check if you switched workspaces (files are workspace-specific)
- Verify the workspace folder exists on disk
- If files are truly missing, check your system's trash/recycle bin

**Q: The editor is not showing syntax highlighting.**
A: 
- Make sure the file has the correct extension (.js, .py, .go, .java)
- Check that the workspace language matches the file type
- Try closing and reopening the file
- Restart the IDE if the issue persists

## Reporting Issues

We want to help you! When reporting an issue, please provide as much information as possible.

### Before Creating an Issue

1. **Check existing issues**: Search this repository to see if your issue has already been reported
2. **Update the app**: Make sure you're using the latest version
3. **Try troubleshooting**: Review the troubleshooting section below

### Creating a Good Issue Report

When creating a new issue, please include:

#### Required Information

- **Operating System**: macOS, Windows, or Linux (include version)
- **App Version**: Found in Settings → About or Help → About
- **Description**: Clear description of what happened
- **Steps to Reproduce**: Step-by-step instructions to reproduce the issue
- **Expected Behavior**: What you expected to happen
- **Actual Behavior**: What actually happened

#### Optional but Helpful Information

- **Screenshots**: Visual evidence of the issue
- **Error Messages**: Copy the full error message from the output panel
- **Workspace Type**: Language and template used
- **Runtime Version**: Version of the language runtime (e.g., Node.js 20.19.5)
- **Console Logs**: Any errors from the developer console (Help → Toggle Developer Tools)

#### Issue Template

Use this template when creating an issue:

```markdown
**Operating System:**
- OS: [e.g., macOS 14.0, Windows 11, Ubuntu 22.04]

**App Version:**
- Version: [e.g., 0.1.75]

**Description:**
[Brief description of the issue]

**Steps to Reproduce:**
1. [First step]
2. [Second step]
3. [Third step]

**Expected Behavior:**
[What you expected to happen]

**Actual Behavior:**
[What actually happened]

**Screenshots:**
[If applicable, add screenshots]

**Error Messages:**
```
[Paste error messages here]
```

**Additional Context:**
[Any other information that might be helpful]
```

### Issue Categories

When creating an issue, use appropriate labels if available:

- **Bug**: Something isn't working as expected
- **Feature Request**: Suggest a new feature or enhancement
- **Question**: Ask a question about how to use the IDE
- **Documentation**: Issues with documentation or help content

## Troubleshooting

### Common Issues and Solutions

#### App Won't Launch

**Symptoms**: App doesn't start or crashes immediately

**Solutions**:
1. Check if you have the latest version
2. Try deleting app data and restarting:
   - macOS: `~/Library/Application Support/infinity-desktop`
   - Windows: `%APPDATA%\infinity-desktop`
   - Linux: `~/.config/infinity-desktop`
3. Check system requirements (macOS 10.13+, Windows 10+, modern Linux)
4. Check available disk space
5. Create an issue with crash logs

#### Runtime Download Fails

**Symptoms**: "Failed to download runtime" error

**Solutions**:
1. Check your internet connection
2. Verify firewall/antivirus isn't blocking downloads
3. Check available disk space (runtimes can be 50-200MB)
4. Try downloading manually from the runtime provider's website
5. Check if your subscription tier allows the requested version

#### Code Execution Fails

**Symptoms**: Code doesn't run or shows errors

**Solutions**:
1. Verify the entry file is set (marked with ⭐)
2. Check for syntax errors in your code
3. Verify the runtime is downloaded and available
4. Check the output panel for specific error messages
5. Try running a simple "Hello World" program to test
6. Verify file permissions (especially on Linux)

#### Files Not Saving

**Symptoms**: Changes aren't saved or files disappear

**Solutions**:
1. Check if you have write permissions to the workspace directory
2. Verify disk space is available
3. Check if the workspace folder exists: `~/.infinity-desktop/workspaces/`
4. Try saving manually with `Cmd/Ctrl + S`
5. Check for file system errors

#### Performance Issues

**Symptoms**: App is slow or unresponsive

**Solutions**:
1. Close unnecessary files/tabs
2. Restart the IDE
3. Check system resources (CPU, memory, disk)
4. Disable language server features if not needed (Settings)
5. Reduce workspace size (move large files outside)
6. Check for background processes consuming resources

### Getting More Help

If you've tried the troubleshooting steps and still need help:

1. **Search Issues**: Check if someone else has the same problem
2. **Create an Issue**: Use the issue template above
3. **Check Documentation**: Review the main project README
4. **Community**: Join our community discussions (if available)

## Contributing

Found a bug or have a feature request? We welcome contributions! Please:

1. Search existing issues first
2. Create a detailed issue report
3. Follow the issue template
4. Be patient - we'll respond as soon as possible

---

**Thank you for using Infinity Desktop!** We're here to help make your coding experience as smooth as possible. If you have any questions or need assistance, don't hesitate to create an issue in this repository.

