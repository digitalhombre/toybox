# Conversation Viewer Web App

A simple, elegant web application for viewing conversational turns from text files.

## Features

- Upload and parse conversation text files
- Display one conversation turn at a time
- Navigate between turns using:
  - Previous/Next buttons
  - Left/Right arrow keys
- Beautiful, gradient-themed UI
- Responsive design

## Usage

1. Open `conversation-viewer.html` in a web browser
2. Click "Choose File" to upload a conversation text file
3. Use the navigation buttons or arrow keys to move between turns
4. Click "Back to Upload" to load a different file

## File Format

The conversation text file should follow this format:

```
name-of-first-speaker said: something...
name-of-second-speaker said: something...

name-of-first-speaker said: another thing...
name-of-second-speaker said: a response...
```

Each turn consists of two lines:
- First line: First speaker's name + " said: " + their message
- Second line: Second speaker's name + " said: " + their message

Speaker names can be different in each file, but the format must include " said: " after the name.

## Example

See `sample-conversation.txt` for an example conversation file.

## Technical Details

- Pure HTML/CSS/JavaScript (no dependencies)
- Works offline - just open in a browser
- Uses FileReader API for file processing
- Keyboard event listeners for arrow key navigation
