# Cineflicks Media

Cinema · News · Events: website with slot booking and an order-aware chat assistant.

## Run in VS Code
1. File > Open Folder... and choose this folder.
2. Install the recommended extension **Live Server** when VS Code asks.
3. Right-click `index.html` > **Open with Live Server** (http://127.0.0.1:5500).

## Structure
```
index.html        page markup
css/style.css     all styles (black and white theme, dark mode)
js/config.js      services, slots, business details, refund/reschedule POLICY
js/app.js         services grid, booking form, slot buttons
js/chatbot.js     orders, 5-step workflow, notifications, chat assistant
assets/           logo.jpg, background.jpg
```
Script order in `index.html` matters: config.js, app.js, chatbot.js.

## Chat workflow
1. Retrieve order ID  2. Check form details  3. If delayed, check refund / reschedule eligibility
4. Replace time  5. In-app notification

Orders and notifications are stored in the browser (localStorage). A backend is needed
for the studio to receive them and for Excel storage.
