# Non-Adjacent Text Selection
Allows non-adjacent text selections in Chrome. Text can be copied to clipboard through the right-click copy option or ctrl-c.
You can also Google search the text through the right click selection menu.

## Getting Started

### Installing
Enable Developer Mode at chrome://extensions. Select 'Load unpacked' and choose the directory of this project. 

You can also install the extension directly from the Chrome Web Store at: 

### Usage
Make each selection while holding down ctrl. Clear all selections by clicking without holding ctrl. Undo with ctrl-z.

Right click the final selection (dark blue) for search options.
Select MultiSearch to open a search tab for each selection.
Select CombinedSearch to open a single search tab for each selection separated by a space.

Select the extension icon in the Chrome toolbar (top-right of the browser) to toggle copy options.
If 'Copy With Newline' is selected, each selection will be separated by a newline when copying.
If 'Copy With Spaces' is selected, each selection will be separated by spaces when copying.

### Notes
- Selections are sent to the clipboard and searched in the order they are selected
- Newlines when selecting multiple bullets or lines of text will be automatically removed.
- This extension is intended to be used on text. Selections on non-text areas such as hyperlinks will fail.

### Known Bugs
- Toggling copy options will sometimes not take effect. Toggling again will fix this.
- When undoing multiple selections on the same line or paragraph, if something after the last selection(in position) in the same line or paragrah is ctrl-clicked, random words will be highlighted with each undo. It is not clear why this happens.
- When making overlapping selections, ctrl-z will remove the combined selection. The clipboard will only remove the most recent selection. This is due to how the removeHighlight() function works.
- Selecting text will rarely remove spaces between words.
- Selections are rarely not cleared after clicking. Refresh the page if this happens.

## License
This project is licensed under GNU GPLv3.