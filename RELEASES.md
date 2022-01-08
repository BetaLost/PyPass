## Version 1.0 - 13 August 2020
  * Basic features released

## Version 1.1 - 15 August 2020
  * Added new security features:
    - Passwords are hidden when adding new accounts
    - Passwords are encrypted and only get decrypted when searching for an individual account or deleting an account
  * Database files from Version 1.0 will not work on Version 1.1+
 
 ## Version 2.0 - 16 August 2020
  * Program re-written (credits to hankhank10 - https://github.com/hankhank10/PyPass)
  * Fixed a major security flaw
  * Removed the `atexit` library
  * Added "PyPass" title text on program start
  * Fixed a few typos
  * Website names are no longer saved in lowercase
  * Fixed all notes being saved as "User did not enter notes."
  * Causing a Keyboard Interrupt in any of the information prompts of the "Add Account" feature will now send you back to the select operation menu
  * Causing a Keyboard Interrupt in the confirm to delete account prompt will now send you back to the select operation menu
  * Causing a Keyboard Interrupt in the select operation menu no longer throws an error, instead it will exit the program

## Version 2.1 - 20 August 2020
  * Added dates to new builds in the `README.MD` file
  * Added confirm password prompt when adding new account
  * Better exit handling implemented
  * "#"s are no longer hardcoded

## Version 2.2 - 21 August 2020
  * Cleaned up the code to make it more consistent
  * Added an option to generate passwords when adding an account
  * Fixed a bug regarding multiple choice selection
  * Replaced "#"s with "—"s
  * Added the following libraries: `secret`, `string`, `pyperclip`
  * Decrypted passwords will automatically be copied to clipboard when searching for a specific account (This feature requires `pyperclip`)
  * When adding a new account, if the user accepted a generated password, the password will be copied to clipboard (This feature requires `pyperclip`)

## Version 2.3 - 2 September 2020
  * Added "Edit Account" feature that allows you to edit username, password, and notes
  * Created "Assets" directory
  * Imported 2 features from 2 libraries: `move()` from `shutil`, `urlopen()` from `urllib.request`
  * Cleaned up the code slightly
  * Database file is now stored in the Assets directory
  * If the `database.json` file is still in the main directory, it will be moved automatically
  * If the `Assets/text.txt` file is not found, it will be automatically retrieved from this repo. If the internet is disconnected then this process will fail.

## Version 3.0 - 24 February 2021
  * Imported `filedialog` from `tkinter`
  * Replaced the inconvenient cut-and-paste key system. Now, when you open the program and the `database.json` file exists, you will be prompted with a GUI to browse to and open the `key.key` file.
  * Reformatted and slighty modified the `README.MD` file
  * Added option to "Reset Data" in the main menu (option X)
  * Minor modifications to the "Main Loop" code
  * Updated instructions
  * Fixed the "PYPASS" title text appearing as irrelevant characters by changing the encoding to "utf-8" when opening the `text.txt` file
  * Fixed the "PYPASS" title text failing to download when the `text.txt` file is missing
  * Major bug fixes within first-time setup code
  * Improved program consistency
  * Switched between Search or Delete account options (C was delete and D was search)

## Version 3.1 - 5 September 2021
  * Modified the `README.MD` file. Dates are now written in the British format
  * Updated instructions

## Version 3.2 - 28 November 2021
  * Added a feature to allow you to generate a random password without changing the password of an existing account
  * Instructions have been rewritten
  * Revamped and reformatted the `README.md` file
  * Program no longer fails to launch if `pyperclip` library is not installed
  * Other bug fixes

## Version 4.0 - 29 November 2021
  * Program has been completely rewritten from scratch and restructured so that it is split into multiple files
  * A master key is now used (hashed with salt using SHA-256, key is derived using PBKDF2)
  * Fixed inconsistencies and bugs
  * Patched serious security vulnerabilities
  * PyPass title text is now hard coded into the main PyPass file
  * Multiple unnecessary modules were dropped
  * Better Pyperclip exception handling
  * Better KeyboardInterrupt exception handling
  * Databases and keys generated before v4.0 will no longer work on newer versions
  * Rewrote instructions and `README.md` file
  * Changelog is now stored in the `RELEASES.md` file