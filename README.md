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

### Simple format (single-line messages):
```
name-of-first-speaker said: something...
name-of-second-speaker said: something...

name-of-first-speaker said: another thing...
name-of-second-speaker said: a response...
```

### Multi-line format (messages on following lines):
```
Alice said:
This is a multi-line message
that spans several lines
and preserves line breaks

Bob said:
This is the response
also multi-line
```

### Mixed format (text after "said:" or on next line):
```
Alice said: This message is on the same line
Bob said:
This message starts on the next line
and continues here
```

### Key Points:
- Each speaker statement begins with: `name said:`
- Message text can appear on the same line after "said:" or on following lines
- Multi-line messages are supported and line breaks are preserved
- Blank lines between messages are handled gracefully
- Carriage returns (`\r\n`) and different line endings are normalized
- Speaker names can vary between files
- Messages can contain the word "said:" without breaking the parser

## Examples

- `sample-conversation.txt` - Simple single-line format
- `test-multiline.txt` - Comprehensive multi-line examples
- `test-said-in-message.txt` - Messages containing "said:" within them

## Technical Details

- Pure HTML/CSS/JavaScript (no dependencies)
- Works offline - just open in a browser
- Uses FileReader API for file processing
- Keyboard event listeners for arrow key navigation
- Robust parsing handles:
  - Multiple line ending formats (CRLF, LF, CR)
  - Multi-line messages with preserved formatting
  - Blank lines and variable whitespace
  - Messages containing "said:" text
  - Mixed single-line and multi-line formats
- HTML escaping prevents XSS vulnerabilities
- Line breaks preserved with `<br>` tags in display
