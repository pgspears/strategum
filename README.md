# Strategem: The Game Theory Learning Hub



**Strategem** is an elaborate, single-page web application designed to be a comprehensive resource for learning and exploring the principles of Game Theory. It combines theoretical knowledge with interactive simulations, real-world case studies, and gamified learning to help users build a strong, intuitive understanding of strategic thinking.

This project is built with vanilla **HTML, CSS, and JavaScript**, demonstrating how a complex, stateful application can be created without external frameworks. It is self-contained in a single `index.html` file for maximum portability and ease of use.

## ✨ Features

*   **Interactive Dashboard:** A personalized hub that tracks user progress with **Strategy Points (XP)** and showcases unlocked **Achievements**.
*   **State Persistence:** User progress is automatically saved to the browser's `localStorage`, so you can pick up where you left off.
*   **Comprehensive Learning Hub:**
    *   **Foundations:** Detailed explanations of the history, pioneers, and core concepts of Game Theory.
    *   **Dynamic Glossary:** An in-app, searchable glossary of key terms. Terms within the learning content are automatically highlighted with tooltips for quick reference.
*   **Interactive Scenarios:**
    *   Explore classic games like the **Prisoner's Dilemma**, **Game of Chicken**, **Stag Hunt**, and **Battle of the Sexes**.
    *   **Quantitative Analysis:** Instantly calculate and visualize the Nash Equilibrium for any scenario. The UI highlights best responses and equilibria directly on the payoff matrix.
    *   **Play vs. AI:** Engage directly with the scenarios by playing against an AI with multiple, selectable strategies (e.g., Tit-for-Tat, Always Defect, Random).
*   **Real-World Case Studies:** A curated collection of articles showing how Game Theory applies to:
    *   **Business:** Cola Wars, Auction Theory (Google Ads), Network Effects.
    *   **Foreign Policy:** The Cuban Missile Crisis.
    *   **Biology:** Vampire Bat food sharing.
*   **Sandbox Game Creator:** Design your own 2x2 strategic games! Define the players, actions, and payoffs, and use the app's engine to analyze your creation for equilibria.
*   **Test Your Knowledge:** A multi-level quiz section (Beginner, Intermediate, Advanced) to test your understanding, complete with instant feedback and explanations.

## 🛠️ Tech Stack

*   **HTML5:** For the core structure and content.
*   **CSS3:** For modern styling, including Flexbox, Grid, custom properties (variables), and subtle animations.
*   **JavaScript (ES6+):** For all application logic, state management, interactivity, and dynamic rendering.
*   **No Frameworks/Libraries:** This project is intentionally built with "vanilla" technologies to demonstrate core web development principles.

## 🚀 Getting Started

There are no build steps or dependencies required.

### Option 1: Quick Launch
Simply download the `index.html` file and open it in any modern web browser (like Chrome, Firefox, or Edge).

### Option 2: Clone the Repository
1.  Clone this repository to your local machine:
    ```bash
    git clone https://github.com/your-username/strategem.git
    ```
2.  Navigate to the project directory:
    ```bash
    cd strategem
    ```
3.  Open the `index.html` file in your browser.

## 🏛️ Code Architecture

The application is encapsulated within a single Immediately Invoked Function Expression (IIFE) to avoid polluting the global namespace. The core logic is organized into a main `App` object with a flat structure for clarity and to prevent `this` context issues.

*   **`Data` Object:** A static data store containing all the text content, scenario definitions, quiz questions, etc. This separates content from logic.
*   **`App` Object:**
    *   **`state`:** Holds the dynamic state of the application, including the current page, user XP, achievements, and game history.
    *   **`init()`:** The entry point that loads saved state, binds all event listeners, and renders the initial page.
    *   **Event Listeners:** A single, delegated event listener on the `#main-content` area handles all dynamic UI interactions efficiently.
    *   **State Management (`saveState`, `loadState`):** Methods for persisting and retrieving user data from `localStorage`.
    *   **Page Renderers (`renderDashboard`, `renderScenarios`, etc.):** Functions responsible for generating the HTML for each section of the application.
    *   **Event Handlers (`handleAnalysis`, `handleQuizSubmit`, etc.):** Functions that contain the logic for what happens when a user interacts with the application.
    *   **Templates (`templateScenarioCard`, etc.):** Functions that generate reusable HTML strings for complex components like the scenario cards.
    *   **Utilities (`analyzeMatrix`, `grantAchievement`, etc.):** Helper functions for common tasks like calculating equilibria or managing user progress.

This architecture ensures a clear separation of concerns while remaining lightweight and framework-free.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

&copy; 2025 Accelerate Solutions, LLC. All rights reserved.
