# c64-markdown-printer
Commodore 64 MarkDown file printer program

# The purpose of this program

With the help of this program you can print a MarkDown file with your Commodore 64 and printer (tested with Citizen 120D, but since the API of Commodore printers are essentially the same, it should be compatible with any printer with a Commodore Serial IEEE-488 interface).

# How to use

1. Build the source code with [Turbo Macro Pro (TMP)](http://turbo.style64.org/)
2. Run the program with `SYS xxxxxx`
3. Enter (SEQ) file name (the file must be located on Drive 4)
4. The file will be printed

# Supported syntax

The following syntax elements are currently implemented:
- **bold text** (with `**stars only**`)
- *italic text* (with `*stars only*`)
- headers h1, h2, h3 (with `#`, `##`, `###` respectively)
- block quotes (lines starting with `>`), currently nesting is not supported
- ordered lists (lines starting with numbers), currently nesting not supported
- unordered lists (lines starting with `-` only)
- horizontal rules (lines starting with `---` only)
- escaping characters (with `\`)

# Working principle of the program

The program implements a state machine.
