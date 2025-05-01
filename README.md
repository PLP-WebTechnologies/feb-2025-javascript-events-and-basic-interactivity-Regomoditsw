# 🎯 JavaScript Event Handling & Interactive Elements Assignment

Welcome to the **ultimate JavaScript playground**! 🎉 This assignment is where we turn boring web pages into dynamic, responsive, *alive* experiences. Get ready to master **event handling**, build **interactive components**, and validate forms like a pro! 💪

## 📁 Assignment Structure

```
📂 js-event-assignment/
├── index.html         # Your playground – where it all comes together
├── style.css          # Keep it cute (optional but encouraged)
└── script.js          # The JavaScript wizardry happens here
```

---

## 🧪 What to Build

Here’s what your interactive bundle of joy should include:

### 1. Event Handling 🎈  
- Button click ✅  
- Hover effects ✅  
- Keypress detection ✅  
- Bonus: A secret action for a *double-click* or *long press* 🤫

### 2. Interactive Elements 🎮  
- A button that changes text or color  
- An image gallery or slideshow  
- Tabs or accordion-style content  
- Bonus: Add some animation using JS or CSS ✨

### 3. Form Validation 📋✅  
- Required field checks  
- Email format validation  
- Password rules (e.g., min 8 characters)  
- Bonus: Real-time feedback while typing

---

## 🧙‍♂️ Pro Tips

- Keep your code clean and commented – your future self will thank you!
- Think about **user experience** – what makes your site more *fun* to use?
- Don’t be afraid to **Google and experiment** – that’s how real developers roll!

---

## 🎉 Now Go Make It Fun!

Remember – this isn't just code. It's your **first step toward creating magical user experiences**. So play around, break stuff (then fix it), and most of all, have FUN! 😄

Happy Coding! 💻✨  

### Index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive JavaScript Playground</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>JavaScript Interactive Playground</h1>
    </header>

    <main>
        <!-- Event Handling Section -->
        <section id="event-handling">
            <h2>Event Handling 🎈</h2>
            
            <div class="event-box">
                <button id="click-button">Click Me!</button>
                <p id="click-output">Button not clicked yet</p>
            </div>
            
            <div class="event-box hover-box">
                <p>Hover over me!</p>
                <p id="hover-output">Waiting for hover...</p>
            </div>
            
            <div class="event-box">
                <input type="text" id="keypress-input" placeholder="Type something...">
                <p id="keypress-output">No keypress detected yet</p>
            </div>
            
            <div class="event-box secret-box">
                <p>Double click or long press me for a secret!</p>
            </div>
        </section>

        <!-- Interactive Elements Section -->
        <section id="interactive-elements">
            <h2>Interactive Elements 🎮</h2>
            
            <div class="interactive-box">
                <button id="color-changer">Change My Color</button>
            </div>
            
            <div class="interactive-box">
                <div class="image-gallery">
                    <img src="https://picsum.photos/id/237/400/300" alt="Gallery image" class="active">
                    <img src="https://picsum.photos/id/238/400/300" alt="Gallery image">
                    <img src="https://picsum.photos/id/239/400/300" alt="Gallery image">
                    <div class="gallery-controls">
                        <button id="prev-btn">Previous</button>
                        <button id="next-btn">Next</button>
                    </div>
                </div>
            </div>
            
            <div class="interactive-box">
                <div class="tabs">
                    <div class="tab-buttons">
                        <button class="tab-btn active" data-tab="tab1">Tab 1</button>
                        <button class="tab-btn" data-tab="tab2">Tab 2</button>
                        <button class="tab-btn" data-tab="tab3">Tab 3</button>
                    </div>
                    <div class="tab-content">
                        <div class="tab-pane active" id="tab1">
                            <h3>Content for Tab 1</h3>
                            <p>This is the first tab's content.</p>
                        </div>
                        <div class="tab-pane" id="tab2">
                            <h3>Content for Tab 2</h3>
                            <p>Here's some content for the second tab.</p>
                        </div>
                        <div class="tab-pane" id="tab3">
                            <h3>Content for Tab 3</h3>
                            <p>Final tab content goes here.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Form Validation Section -->
        <section id="form-validation">
            <h2>Form Validation 📋✅</h2>
            
            <form id="user-form">
                <div class="form-group">
                    <label for="username">Username (required)</label>
                    <input type="text" id="username" required>
                    <span class="error-message" id="username-error"></span>
                </div>
                
                <div class="form-group">
                    <label for="email">Email (must be valid)</label>
                    <input type="email" id="email">
                    <span class="error-message" id="email-error"></span>
                </div>
                
                <div class="form-group">
                    <label for="password">Password (min 8 chars)</label>
                    <input type="password" id="password">
                    <span class="error-message" id="password-error"></span>
                </div>
                
                <button type="submit">Submit</button>
            </form>
        </section>
    </main>

    <script src="script.js"></script>
</body>
</html>

### styles.css
/* Base Styles */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

header {
    text-align: center;
    margin-bottom: 40px;
}

h1, h2, h3 {
    color: #2c3e50;
}

section {
    margin-bottom: 40px;
    padding: 20px;
    border-radius: 8px;
    background-color: #f9f9f9;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

/* Event Handling Styles */
.event-box {
    padding: 15px;
    margin: 15px 0;
    border: 1px solid #ddd;
    border-radius: 5px;
    background-color: white;
}

.hover-box {
    transition: all 0.3s ease;
}

.hover-box:hover {
    background-color: #e3f2fd;
    transform: scale(1.02);
}

.secret-box {
    cursor: pointer;
    background-color: #fff8e1;
}

/* Interactive Elements Styles */
.interactive-box {
    padding: 15px;
    margin: 15px 0;
    border: 1px solid #ddd;
    border-radius: 5px;
    background-color: white;
}

#color-changer {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.image-gallery {
    position: relative;
    text-align: center;
}

.image-gallery img {
    display: none;
    max-width: 100%;
    height: auto;
    border-radius: 4px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.2);
}

.image-gallery img.active {
    display: block;
    margin: 0 auto;
}

.gallery-controls {
    margin-top: 10px;
}

.gallery-controls button {
    padding: 8px 16px;
    margin: 0 5px;
    background-color: #2196F3;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

/* Tabs Styles */
.tabs {
    margin-top: 20px;
}

.tab-buttons {
    display: flex;
    margin-bottom: 10px;
}

.tab-btn {
    padding: 10px 20px;
    background-color: #f1f1f1;
    border: none;
    cursor: pointer;
    transition: background-color 0.3s;
}

.tab-btn.active {
    background-color: #ddd;
}

.tab-btn:hover:not(.active) {
    background-color: #e9e9e9;
}

.tab-pane {
    display: none;
    padding: 15px;
    border: 1px solid #ddd;
    border-top: none;
    border-radius: 0 0 4px 4px;
}

.tab-pane.active {
    display: block;
}

/* Form Validation Styles */
#user-form {
    max-width: 500px;
    margin: 0 auto;
}

.form-group {
    margin-bottom: 15px;
}

.form-group label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

.form-group input {
    width: 100%;
    padding: 8px;
    border: 1px solid #ddd;
    border-radius: 4px;
    box-sizing: border-box;
}

.form-group input:focus {
    outline: none;
    border-color: #2196F3;
    box-shadow: 0 0 5px rgba(33, 150, 243, 0.5);
}

.error-message {
    color: #e74c3c;
    font-size: 0.8em;
    height: 20px;
    display: block;
}

button[type="submit"] {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 1em;
}

button[type="submit"]:hover {
    background-color: #45a049;
}

/* Animation Classes */
@keyframes shake {
    0%, 100% { transform: translateX(0); }
    20%, 60% { transform: translateX(-5px); }
    40%, 80% { transform: translateX(5px); }
}

.shake {
    animation: shake 0.5s;
}

@keyframes celebrate {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}

.celebrate {
    animation: celebrate 0.5s;
}

.secret-revealed {
    background-color: #ffecb3 !important;
    transform: rotate(1deg);
    transition: all 0.5s ease;
}

### script.js

/* Base Styles */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

header {
    text-align: center;
    margin-bottom: 40px;
}

h1, h2, h3 {
    color: #2c3e50;
}

section {
    margin-bottom: 40px;
    padding: 20px;
    border-radius: 8px;
    background-color: #f9f9f9;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

/* Event Handling Styles */
.event-box {
    padding: 15px;
    margin: 15px 0;
    border: 1px solid #ddd;
    border-radius: 5px;
    background-color: white;
}

.hover-box {
    transition: all 0.3s ease;
}

.hover-box:hover {
    background-color: #e3f2fd;
    transform: scale(1.02);
}

.secret-box {
    cursor: pointer;
    background-color: #fff8e1;
}

/* Interactive Elements Styles */
.interactive-box {
    padding: 15px;
    margin: 15px 0;
    border: 1px solid #ddd;
    border-radius: 5px;
    background-color: white;
}

#color-changer {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.image-gallery {
    position: relative;
    text-align: center;
}

.image-gallery img {
    display: none;
    max-width: 100%;
    height: auto;
    border-radius: 4px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.2);
}

.image-gallery img.active {
    display: block;
    margin: 0 auto;
}

.gallery-controls {
    margin-top: 10px;
}

.gallery-controls button {
    padding: 8px 16px;
    margin: 0 5px;
    background-color: #2196F3;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

/* Tabs Styles */
.tabs {
    margin-top: 20px;
}

.tab-buttons {
    display: flex;
    margin-bottom: 10px;
}

.tab-btn {
    padding: 10px 20px;
    background-color: #f1f1f1;
    border: none;
    cursor: pointer;
    transition: background-color 0.3s;
}

.tab-btn.active {
    background-color: #ddd;
}

.tab-btn:hover:not(.active) {
    background-color: #e9e9e9;
}

.tab-pane {
    display: none;
    padding: 15px;
    border: 1px solid #ddd;
    border-top: none;
    border-radius: 0 0 4px 4px;
}

.tab-pane.active {
    display: block;
}

/* Form Validation Styles */
#user-form {
    max-width: 500px;
    margin: 0 auto;
}

.form-group {
    margin-bottom: 15px;
}

.form-group label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

.form-group input {
    width: 100%;
    padding: 8px;
    border: 1px solid #ddd;
    border-radius: 4px;
    box-sizing: border-box;
}

.form-group input:focus {
    outline: none;
    border-color: #2196F3;
    box-shadow: 0 0 5px rgba(33, 150, 243, 0.5);
}

.error-message {
    color: #e74c3c;
    font-size: 0.8em;
    height: 20px;
    display: block;
}

button[type="submit"] {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 1em;
}

button[type="submit"]:hover {
    background-color: #45a049;
}

/* Animation Classes */
@keyframes shake {
    0%, 100% { transform: translateX(0); }
    20%, 60% { transform: translateX(-5px); }
    40%, 80% { transform: translateX(5px); }
}

.shake {
    animation: shake 0.5s;
}

@keyframes celebrate {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}

.celebrate {
    animation: celebrate 0.5s;
}

.secret-revealed {
    background-color: #ffecb3 !important;
    transform: rotate(1deg);
    transition: all 0.5s ease;
}

