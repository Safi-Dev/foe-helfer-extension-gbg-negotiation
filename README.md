## FoE Helper

##### A small extension for the Online Browser-Game Forge of Empire to install in all Chromium based Browsers like Google Chrome, Opera, Chromium or Microsoft Edge, much more and FireFox

## Installation Instructions

1. Download Source Code (click the green button in the top right labelled "Code" and select download as .zip from the menu
   
3. Unpack the .zip file into a folder (make sure the file path is similar to the following "C:\Users\X\X\foe-helfer-extension-master" (ensure there is no doubled folders))
   
4. Open your Chromium-based browser.
   
5. Go to the browser's extensions page by either:
   - Typing `chrome://extensions/` in the address bar and pressing Enter.
   - Clicking on the menu icon (three dots) in the top right corner of the browser, selecting "More tools," and then "Extensions."
   - 
6. Enable "Developer mode" by toggling the switch in the top right corner of the extensions page.

7. Click the "Load unpacked" button that appears after enabling Developer mode.

8. A file dialog will open. Navigate to the folder where you downloaded this GitHub repository, and select the folder containing the extension's source code.

9. Click the "Select Folder" button to load the extension.

8. Your extension should now be installed and visible on the extensions page.

9. Optionally, you can pin the extension icon to the browser's toolbar for easy access.

## Changes
##### foe-helfer-extension-master\js\web\negotiation\js\negotiation.js

```
if (responseData.context === Negotiation.CONST_Context_GBG) {
    if (!$('#negotiation-Btn').hasClass('hud-btn-red')) {
        $('#negotiation-Btn').addClass('hud-btn-red');
        _menu.toolTipp('#negotiation-Btn', i18n('Menu.Negotiation.Title'), '<em id="negotiation-Btn-closed" class="tooltip-error">' + i18n('Menu.Negotiation.Warning') + '<br></em>' + i18n('Menu.Negotiation.Desc'));
    }

    // If contxt is 'GBG' return will be executed preventing GBG use
    return
```

```
if (responseData.context === Negotiation.CONST_Context_GBG) {
    if (!$('#negotiation-Btn').hasClass('hud-btn-red')) {
        $('#negotiation-Btn').addClass('hud-btn-red');
        _menu.toolTipp('#negotiation-Btn', i18n('Menu.Negotiation.Title'), '<em id="negotiation-Btn-closed" class="tooltip-error">' + i18n('Menu.Negotiation.Warning') + '<br></em>' + i18n('Menu.Negotiation.Desc'));
    }

    // Set the context to 'GE' instead of 'GBG'
    responseData.context = Negotiation.CONST_Context_GE;
```

## FAQ

For questions and answers please use the FOE Helper Forum [forum](https://discuss.foe-helper.com/) or discuss with us on the [Discord](https://discord.gg/z97KZq4) server.

## Bugs & Wishes

If you find an error or have a request that is not yet available as a ticket, please raise an issue in the github source code.

_This is an Open Source Projekt under the [AGPLv3 License](LICENSE.md)._
