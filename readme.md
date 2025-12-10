Modal Window Project

A simple, responsive, and interactive Modal Window component built using HTML, CSS, and Vanilla JavaScript. This project focuses on DOM manipulation and handling various types of user events.

🌟 Features

Multiple Triggers: Can be opened by clicking any of the three "Show Modal" buttons.

Keyboard Accessibility: The modal closes instantly when the Escape key is pressed.

Overlay Interaction: Clicking outside the modal (on the blurred overlay) closes the window.

Close Button: Includes a dedicated "X" button to close the modal.

Clean Transitions: Uses CSS classes to manage visibility for smooth performance.

🛠️ Technologies Used

HTML5: Semantic structure for the modal and overlay.

CSS3: Styling for the hidden/visible states and the blurred backdrop effect.

JavaScript (ES6+):

DOM Manipulation (querySelector, querySelectorAll).

Event Listeners (click, keydown).

Class Manipulation (classList.remove, classList.add).

DRY Principle: Refactored logic into reusable openModal and closeModal functions.

📂 Project Structure

modal-window/
├── prettierrc
├── index.html # Main HTML structure
├── readme.md #Modal Window Documentation
├── style.css # Styling for modal and hidden classes
└── script.js # Event handling logic

🧠 Logic Highlight

I focused on keeping the code DRY (Don't Repeat Yourself). Instead of writing the close logic three times (for the button, the overlay, and the Esc key), I created a single function:

const closeModal = function () {
modal.classList.add('hidden');
overlay.classList.add('hidden');
};

// Closing the modal with the Esc key
document.addEventListener('keydown', function (e) {
if (e.key === 'Escape' && !modal.classList.contains('hidden')) {
closeModal();
}
});

🚀 How to Run

Clone this repository or download the files.

Open the index.html file in your web browser.

Click the buttons to test the modal interactions!
