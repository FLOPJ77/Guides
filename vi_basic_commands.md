# VI Commands Guide


### Basic Navigation
   - `h`, `j`, `k`, `l`: Move left, down, up, and right respectively.
   - `w` / `b`: Move word by word forward / backward.
   - `0` (zero): Go to the beginning of the line.
   - `$`: Go to the end of the line.

### Editing Text

- **Insert Mode (`a`, `i`, `o`, `O`)**:
  - `a` - Append after the cursor.
  - `i` - Insert before the cursor.
  - `o` - Open a new line below the cursor for editing.
  - `O` - Open a new line above the cursor for editing.

- **Delete Text (`x`, `Xd`)**:
  - `x` - Delete the character under the cursor.
  - `Xd` - Delete from the cursor to the end of the word.

### Cutting and Copying

- **Cut Line (`dd`)**: Deletes the current line.
- **Copy Line (`yyp` or `yw` + `p`)**:
  - `yyp` - Yanks (copies) the entire current line and puts it after the cursor.
  - `yw` followed by `p` - Yanks a word under the cursor and appends it after the cursor.
  
### Replacing Text

- **Replace (`r`)**: Replace a single character under the cursor with another character (e.g., `rX` replaces 
'Y' with 'X').
- **Global Replace (`:%s/original/replacement/g`)**:
  - `%` - Operates on all lines.
  - `/s/` - Search for 'original'.
  - `/replacement/` - Replace with 'replacement'.
  - `/g/` - Global replace, not just the first occurrence.

### Saving and Quitting

- **Save File (`:w`)**: Write changes to disk.
- **Quit Without Saving (`:q!`)**: Exit Vi without saving any unsaved changes.
- **Save and Quit (`:x` or `:wq`)**: Save all changes and exit.

### Moving Around in Text

- **Jump Between Tags (`gi`)**:
  - When inside a tag (e.g., `<p>`), press `gi` to jump to the matching closing tag.
  
- **Move by Words (`wa`, `wb`)**:
  - `wa` - Move forward by words.
  - `wb` - Move backward by words.

