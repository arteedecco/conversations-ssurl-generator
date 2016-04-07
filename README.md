# conversations-ssurl-generator
A standalone web-based app to generate perfectly formatted submission links ("ssURLs") for Bazaarvoice Conversations

## Current Scope:
- Hosted Authentication
- Ratings & Reviews

## How to use this app (Mac and *nix users, assuming you have `git` installed):
1. Simply clone the project (i.e. "repo" or "repository") to a local directory
2. drag-n-drop the index.html file into your favorite browser
3. Enjoy!
\* note for Windows users. Step 1: Get a Mac or a Linux machine! :) Or see below for alternative steps.

## _Alternative_ How to use this app (the dreaded Windows user):
This can work for either Mac or Windows, but it's easiest to just download a free `git` desktop manager. That way you can forego needing to run commands from a terminal window.
- Github offers one: https://desktop.github.com/
- Atlassian also offers one: https://www.sourcetreeapp.com/

## How to clone the repo?
From your terminal (command line)
```
git clone https://github.com/arteedecco/conversations-ssurl-generator.git
```

Please report any bugs.

## To-Do's
- [ √ ] Add generic review submission support
- Add deep linking support

## Revisions
- Added a 50px margin to the bottom of the .container div. Didn't like that the last form element rested right on the bottom of the browser window (style. "meh").
- Corrected typo in label for Product Family ID in generic review submission section of form
- Added prevent close option to generic review submission (doesn't look like it's functional for regular submission)
- Added generic review submission capability
- Fixed bug with `bvproductId` parameter which had a typo previously in the generated URL: `vproductId` (missing the leading 'b' char)
- Added detection of empty fields for data injection pairs, only enable the "Add" button if both Question and Answer text input fields contain content (not blank)
- Fixed form element labels
- Only allow users to enter unique data pairs to inject. In other words we don't want users entering duplicate `question=value` combinations since all submission form quesiton ids are unique
- Added validation to the add new question / answer input boxes by adding an inline alert warning if a duplicate combination is entered
- Disable the "Add" button if duplicate combination is entered
