# Algo Infinity Verse

**Master Data Structures & Algorithms and Crack Technical Interviews**

A modern, interactive web application for learning and practicing DSA concepts with a gamified learning experience.

![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

---

## Features

### Core Learning Resources

#### DSA Topics
- **6 Comprehensive Topics**: Arrays, Strings, Linked Lists, Trees, Graphs, Dynamic Programming
- Each topic includes:
  - Detailed theory explanations
  - Key concepts and properties
  - Common problem patterns
  - Difficulty ratings (Easy-Medium-Hard)
  - Sample problem lists

#### Practice Problems
- **15+ curated problems** spanning all DSA topics
- Filterable by difficulty (Easy, Medium, Hard)
- Real-time search functionality
- Problem tags for quick identification
- Acceptance rate tracking
- Visual completion badges

### Quiz System

**60 Topic-Specific Questions** (10 per topic covering key concepts)

- **Arrays**: Time complexity, operations, Two Sum, Kadane's algorithm, rotation techniques
- **Strings**: Pattern matching (KMP), palindrome detection, anagrams, sliding window
- **Linked Lists**: Pointer manipulation, cycle detection, reversal, merging
- **Trees**: Traversals, BST properties, height calculation, LCA, heaps
- **Graphs**: Representations, BFS/DFS, topological sort, Dijkstra, MST algorithms
- **Dynamic Programming**: Memoization, tabulation, classic problems (Fibonacci, Knapsack, LIS, Edit Distance)

**Quiz Features:**
- Interactive modal interface
- Progress bar tracking
- Instant answer feedback (correct/incorrect highlighting)
- Detailed explanations for each question
- Score calculation (percentage)
- **XP rewards**: 10 XP per correct answer
- Best score tracking per topic
- Attempt counter
- Randomized question order

### Profile & Gamification

**Customizable Profile:**
- Edit display name
- Choose from 12 avatar emojis
- View join date
- Track level progression

**Progress Tracking:**
- Total XP accumulation
- Problems solved counter
- Day streak monitoring
- Badge earning system

**Levels:**
- 8 levels from Beginner to Legend
- XP thresholds: 0, 1,000, 2,500, 5,000, 10,000, 20,000, 50,000, 100,000
- Automatic level-up notifications

**Badges:**
- 🌟 First Steps (solve 1 problem)
- 🔥 On Fire (7-day streak)
- 💎 Diamond (5,000 XP)
- 🚀 Rocket (50 problems)
- 👑 Master (100 problems)
- 🎯 Sharpshooter (25 problems + 2,500 XP)

### Dashboard
- Complete statistics overview
- Recent activity feed
- Achievement badges display
- Leaderboard comparison
- Roadmap progress visualization

### Interactive Code Editor
- Multi-language support (JavaScript, Python, Java, C++)
- Line numbers and syntax highlighting
- Code snippets insertion
- Auto-formatting
- Line comment toggling
- Run and submit simulation
- Test case validation

### AI Chatbot Assistant
- Instant DSA concept explanations
- Time/space complexity queries
- Problem-solving strategy hints
- Quick question buttons
- Context-aware responses

### User Experience

**Visual Design:**
- Dark/Light theme toggle
- Glassmorphism UI elements
- Gradient accents
- Animated transitions
- Starfield background effect
- Responsive layout (mobile, tablet, desktop)

**Navigation:**
- Sticky navbar with smooth scrolling
- Mobile hamburger menu
- Scroll-to-top button
- Section-based navigation

---

## Technology Stack

- **HTML5**: Semantic markup
- **CSS3**: Custom properties, Flexbox, Grid, animations
- **JavaScript (ES6+)**: Vanilla JS, no frameworks
- **LocalStorage**: Persistent user data
- **Font Awesome**: Icon library
- **Google Fonts**: Orbitron, Poppins, Fira Code

---

## Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Local web server (optional, can open directly)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Algo-Infinity-Verse.git
   cd Algo-Infinity-Verse
   ```

2. **Open the application**
   - Simply open `index.html` in your browser
   - Or use a local server:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve
   ```
   Then visit `http://localhost:8000`

3. **Start learning!**
   - Create your profile
   - Browse DSA topics
   - Take quizzes
   - Practice problems
   - Track your progress

---

## Project Structure

```
Algo-Infinity-Verse/
├── index.html          # Main HTML structure
├── styles.css          # All CSS styles and responsive design
├── script.js           # JavaScript logic, data, and interactivity
└── README.md           # Project documentation
```

---

## Key Scripts

### Data Structures

**`dsaTopics`** - Topic information including:
- ID, name, icon, description
- Difficulty level
- Theory explanation
- Related problems

**`quizQuestions`** - Quiz database:
- 60 questions across 6 topics
- Multiple-choice format (4 options)
- Correct answer indices
- Detailed explanations

**`practiceProblems`** - Problem catalog:
- Title, difficulty, tags
- Acceptance rates
- Category associations

**`chatbotResponses`** - Knowledge base:
- DSA concept explanations
- Complexity definitions
- Algorithm overviews

### State Management

`userProgress` object tracks:
- User name and avatar
- Completed problem IDs
- Total XP and current level
- Day streak count
- Earned badges
- Quiz scores per topic
- Last active date

Persisted to `localStorage` under key `algoInfinityVerse`.

---

## Quiz Architecture

### Flow
1. User clicks "Start Quiz" on topic card
2. Questions are shuffled randomly
3. Modal displays one question at a time
4. User selects an answer → immediate feedback
5. Correct answer highlighted in green; user's wrong choice in red
6. Auto-advance after 1.2 second delay
7. After 10 questions: score calculation
8. Results modal shows percentage, XP earned, performance message
9. Progress bars and statistics update

### Scoring
- 10 XP per correct answer
- Best score saved per topic (max percentage)
- Total attempts tracked
- Progress bar fills on first attempt

---

## Extending the Project

### Adding New Quiz Questions

Edit `script.js` and add to `quizQuestions` object:

```javascript
const quizQuestions = {
    arrays: [
        {
            id: "arrays-11", // unique ID
            question: "Your question here?",
            options: ["Option A", "Option B", "Option C", "Option D"],
            correct: 0, // 0-indexed correct answer
            explanation: "Detailed explanation of why the answer is correct"
        },
        // ... more questions
    ],
    // ... other topics
};
```

### Adding New Topics

1. Add to `dsaTopics` array with icon, description, theory
2. Add corresponding `quizQuestions[topicKey]` array with 10 questions
3. The UI auto-generates topic cards and quiz cards

### Customization

**Colors**: Edit CSS variables in `:root`:
```css
:root {
    --primary: #7c3aed;      /* Main purple */
    --secondary: #3b82f6;    /* Blue accent */
    --accent: #06b6d4;       /* Cyan highlight */
    /* ... */
}
```

**Fonts**: Update Google Fonts links in `index.html` and CSS `font-family` declarations.

**XP Values**: Modify `getXPForDifficulty()` function for practice problems or quiz XP calculation.

---

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

Uses modern ES6+ features and CSS Grid/Flexbox.

---

## Future Enhancements

Potential features for expansion:
- Database backend for multi-user support
- Real code execution sandbox
- Social features (friends, groups, competitions)
- Advanced analytics and learning insights
- Video tutorials and explanations
- Mobile app (React Native)
- Interview simulation mode
- Company-specific question banks

---

## Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## Acknowledgments

- Inspired by LeetCode, HackerRank, and freeCodeCamp
- Built with ❤️ for the DSA learning community
- Icons by Font Awesome
- Fonts by Google Fonts

---

**Start your DSA journey today and level up your coding skills!** 🚀
