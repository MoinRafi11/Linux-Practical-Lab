# Linux `vi` Editor Commands

The `vi` editor is a command-line text editor available on Linux systems. It works using different modes for editing and executing commands.

---

## 1. Open a File

```bash
vi filename.txt

Opens an existing file or creates a new file if it does not exist.



## 2. Vi Editor Modes

The main modes are:

Mode	        Purpose

Normal Mode	Navigate and perform commands
Insert Mode	Insert or edit text
Command Mode	Save, exit, and execute editor commands

When vi opens, it starts in Normal Mode.


## 3. Enter Insert Mode

Press:

i

This allows text to be inserted at the current cursor position.

Other useful insert commands:

i   → Insert before cursor
a   → Insert after cursor
o   → Open a new line below
O   → Open a new line above


## 4. Return to Normal Mode

Press:

Esc

This exits Insert Mode and returns to Normal Mode.


## 5. Save a File

From Normal Mode, press:

Esc
:w

Then press Enter.

: enters Command Mode and w means write/save.



## 6. Save and Exit
Esc
:wq

Then press Enter.

This saves the file and exits vi.



## 7. Exit Without Saving
Esc
:q!

Then press Enter.

The ! forces the editor to exit without saving changes.



## 8. Navigation Commands

Common navigation commands in Normal Mode:

h   → Move left
j   → Move down
k   → Move up
l   → Move right

Other useful commands:

0   → Beginning of line
$   → End of line
gg  → Beginning of file
G   → End of file


## 9. Delete Text

In Normal Mode:

x

Deletes the character under the cursor.

dd

Deletes the current line.


## 10. Copy and Paste

In Normal Mode:

yy

Copies the current line.

p

Pastes the copied content below the current line.



## 11. Undo and Redo
u

Undo the last change.

Ctrl + r

Redo the undone change.

🧪 Basic Vi Workflow

A simple workflow for editing a file:

vi filename.txt
      ↓
Normal Mode
      ↓
Press i
      ↓
Insert/Edit text
      ↓
Press Esc
      ↓
:wq
      ↓
Enter
      ↓
File saved and editor closed



