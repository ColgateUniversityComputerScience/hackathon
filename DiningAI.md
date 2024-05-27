# DiningAI Chrome Extension
**Created by Matthew Szypula**

## Introduction
Hi! I'm Matthew Szypula, a sophomore at Colgate majoring in Computer Science and Mathematical Economics.

### [Pitch & Demo Video](https://youtu.be/TxKR5SOE8AA)

## Purpose & Motivation
Everyone knows how sometimes there's not much variety in the dining halls, or if you have any dietary restrictions it is hard to find creative and unique meals... That is where Dining AI helps! Dining AI uses the power of AI to generate unique meal options based on any dining restrictions and the current menu in the dining halls! No more wandering around the dining halls looking for something good to eat, make it yourself with the help of Dining AI.

## How it Works
Dining AI is a Chrome extension that, when a user presses the generate button, tells the Chrome messaging API to send a message to the `content.js` file to inject a content script into the Colgate Dine on Campus Website. From there, it scrapes the site for the current menu offerings by looking for items with the `menu-item` class. It then prepares and cleans the data to send to the ChatGPT API on a proxy server (to ensure no client-facing API keys are exposed). The data is then sent back to the extension, and through HTML injection, each recipe, including ingredients and instructions, is intuitively displayed on the Colgate Dine on Campus website. The user can then save their favorite recipes, which get stored in Chrome local storage and displayed in the extension popup (from which the user can choose to delete any already saved recipes).

## Development Process
- **Initial Design:** Designed the popup for the extension and scraped and printed the current menu offerings in the dining hall.
- **API Integration:** Progressed to calling the ChatGPT API to generate a JSON detailing recipes that could be made using the given ingredients.
- **HTML Injection:** Dynamically added HTML elements to the webpage through the content script.
- **Saving Recipes:** Developed the saving ability, allowing users to save and delete their favorite recipes in the extension.
- **UI Design:** Ensured a seamless user experience through comprehensive UI design.
- **Proxy Server:** Built a proxy server to handle API requests and ensure API security.

## How to Use
1. Navigate to [Colgate Dine On Campus](https://dineoncampus.com/colgate/whats-on-the-menu)
2. Open the Dining AI Extension in Chrome.
3. Select any dietary restrictions or none.
4. Press "Generate Recipes".
5. The recipes will appear at the top of the Dine On Campus webpage.
6. Click the star at the bottom of each recipe to save it to the extension.
7. Open the extension again to see/delete any saved recipes.
8. Click "More Details" to see ingredients and instructions.

## Difficulties & Challenges
- **File Communication:** Ensuring different JavaScript files communicated effectively using the Chrome messaging API and storage API.
- **Content Security Policy:** Adhering to Chrome's content security policy by creating a proxy server in Heroku to manage calls to the ChatGPT API.
- **Consistent Output Formatting:** Ensuring ChatGPT consistently outputs the same format for parsing and display, achieved through fine-tuning and prompt engineering.

## Go-to-Market Strategy
This extension is scalable due to the scalable Heroku Flask server the ChatGPT API is implemented on. It adheres to all Chrome Extension policies, including its CSP, allowing it to be published on the Chrome Web Store. The API keys are securely stored in a `.env` file on the proxy server. This also works on any Dine On Campus site, making it scalable to other colleges and universities with Dine On Campus access.

## How to Install This Extension
1. Clone this GitHub repo.
2. Go to `chrome://extensions/`.
3. Click 'Load Unpacked' in the top left corner.
4. Select the folder of this repo (DiningAI).
5. Go to the extension bar in the Chrome tab and pin the extension, then click the DiningAI icon to use.

## Contact Information
- **GitHub:** [DiningAI GitHub Repo](https://github.com/mszy123/DiningAI.git)
- **Email:** [mszypula@colgate.edu](mailto:mszypula@colgate.edu)
