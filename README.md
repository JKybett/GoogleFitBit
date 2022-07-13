# GoogleFitBit
A script for Google Sheets that connects a FitBit account to a Google Sheet.

As of 2022-07-13 this script is being actively maintained, but is considered stable and presently in need of changes/fixes. Additional features may be added in future, but this is not a priority and while feature requests are welcome, they are not guaranteed.

- Original script by John McLaughlin (loghound@gmail.com)
- Modifications - Simon Bromberg (http://sbromberg.com)
- Modifications - Mark Leavitt (PDX Quantified Self organizer) www.markleavitt.com
- Modifications 2020 - Jozef Jarosciak - [joe0.com](https://www.joe0.com/)
- Modifications 2022 - Josh Kybett - [JKybett.uk](https://JKybett.uk)
  - Replaced discontinued UiApp code to use HtmlService instead.
  - Replace deprecated v1 FitBit API with current standard v2 FitBit API
  - Now fetches data using daily summaries rather than per-item ranges to avoid hitting API limits when getting single-day data.
  - Adapted to get data for more features of FitBit.
  - Friendlier setup UI.

## Setup
1. Open the Google Sheet you would like to store your data in. This version of the script cannot be expected to behave with other versions, but is designed so that future variants of the script can be made to work with this one with little to no effort.
2. Open the "Extensions" toolbar at the top of the page and open "Apps Script" (this should appear in a new tab). Paste the code from the FitBit.gs file into the editor and click the save icon to save the project. You should know that it has saved successfully as there will be no orange circle beside the file name on the left side of the editor.
3. On the left side of the editor, click the + next to the Libraries section, type the key below into the box that appears and click "Look Up" to add the OAuth2 library to the script (This is necessary for the script to communicate with FitBit). Make sure you pick the latest version and keep the identifier for the library as "OAuth2", then click "add". To find out more about this library, you can visit [its GitHub page](https://github.com/googleworkspace/apps-script-oauth2 "apps-script-oauth2").
   - OAuth2 key: `1B7FSrk5Zi6L1rSxxTDgDEUsPzlukDsi4KGuTMorsTQHhGBzBkMun4iDF`
4. Go back to your spreadsheet and refresh the page (this will likely close the Apps Script tab. This is fine). After a few seconds a "FitBit" option should appear in the toolbar at the top of the page. The "Setup" option will walk you through the remaining setup.

## Copyright & License

This is a free script: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.

Copyright (c) 2022 JKybett
