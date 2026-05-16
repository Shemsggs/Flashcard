# Flashcard App

A web-based flashcard study application for learning various subjects including history, science, literature, and more.

## 🚀 Live Demo

Visit the app at: [https://flashcard-hanna-ten.vercel.app](https://flashcard-hanna-ten.vercel.app)

## 📚 How to Use

### Getting Started
1. Open the flashcard app in your browser
2. The app will automatically load with all available categories

### Main Features

#### 1. **Select Categories**
   - Use the checkboxes on the left sidebar to select which subjects you want to study
   - Check the categories you're interested in (e.g., History, Science, Literature, etc.)
   - Uncheck categories to exclude them from your study session
   - Click **"Build Deck"** button to load cards from selected categories

#### 2. **Study Cards**
   - Each card displays a question on the front
   - Click on the card or press **Space** to flip and see the answer
   - Read the answer to check if you got it right

#### 3. **Mark Your Progress**
   After flipping to see the answer, use one of these buttons:
   - **✓ Correct** - Mark the card as correctly answered
   - **✗ Wrong** - Mark the card as incorrectly answered (card goes to end of deck)
   - **» Skip** - Skip the card and move to the next one (card goes to end of deck)

#### 4. **Track Statistics**
   - View your progress at the top of the screen:
     - **Cards Studied**: Total cards reviewed in this session
     - **Correct**: Number of cards marked correct
     - **Wrong**: Number of cards marked wrong
     - **Percentage**: Your current accuracy rate

#### 5. **Restart or Switch Categories**
   - Click **"Restart"** to reset your statistics and start over with the current categories
   - Select different categories and click **"Build Deck"** to start a new study session

### Keyboard Shortcuts
- **Space** - Flip card to see answer
- **Arrow Keys or Click Buttons** - Navigate through answers

### Available Categories

The app includes flashcards for:
- **Philippine History** (Presidents, Historical Events, Rizal Works)
- **Science** (Biology, Chemistry, Physics, Earth Science, Science History)
- **Literature** (Novels, Authors, Pen Names, World Literature, Literary Devices, Poetry)
- **Economics & Taxation**
- **Philosophy & Religion** (Acts, Missionaries, Martyr Priests)
- **Language** (Grammar, Morphology, Language Theories, Folk Songs)
- **General Knowledge** (Idioms, Figures of Speech, Mnemonics, Vocabulary)
- **And more!**

## 💾 Local Development

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/shemene22/Flashcard.git
   cd Flashcard
   ```

2. Open the app locally:
   - Double-click `docs/index.html` or `flashcards/index.html`
   - Or serve using a local server:
     ```bash
     python -m http.server 8000
     ```
   - Then visit `http://localhost:8000/docs/`

### Project Structure
```
Flashcard/
├── docs/                    # Production app (served by Vercel)
│   ├── index.html          # Main HTML file
│   ├── css/style.css       # Styling
│   ├── js/
│   │   ├── app.js          # Main app logic
│   │   └── cards.js        # Card data merger
│   └── data/               # Category data files
└── flashcards/             # Development/backup app
    └── (same structure)
```

### Adding New Flashcards

1. Create a new data file in `docs/data/` and `flashcards/data/`:
   ```javascript
   const CATEGORY_NAME_CARDS = [
     { q: "Question 1?", a: "Answer 1", cat: "Category Name" },
     { q: "Question 2?", a: "Answer 2", cat: "Category Name" },
   ];
   ```

2. Add a script import in `docs/index.html` and `flashcards/index.html`:
   ```html
   <script src="data/category_name.js"></script>
   ```

3. Add the category to the merger in `docs/js/cards.js` and `flashcards/js/cards.js`:
   ```javascript
   ...CATEGORY_NAME_CARDS,
   ```

4. Commit and push changes

## 🎯 Tips for Studying

- **Focus on weak areas**: Mark "Wrong" to move difficult cards to the end for extra practice
- **Mix categories**: Study multiple subjects together to build connections
- **Regular sessions**: Short, frequent study sessions are more effective than cramming
- **Review statistics**: Check your percentage to track improvement over time

## 📝 Contributing

To contribute new flashcards or categories:

1. Fork the repository
2. Create a new branch for your changes
3. Add or modify flashcard data files
4. Test locally to ensure cards load correctly
5. Submit a Pull Request to the main repository

## 📄 License

This project is open source and available for educational purposes.