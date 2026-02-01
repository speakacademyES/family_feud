# Family Feud - Enhanced Classroom Edition

A fully-featured Family Feud game for ESL classroom use with customizable questions, game settings, and statistics tracking.

## 🎮 Features

- **Dynamic JSON Question Loading** - Use built-in questions or upload custom JSON files
- **Configurable Game Settings** - Customize rounds, time limits, strikes, and multipliers
- **Sound Controls** - Mute/unmute and volume control
- **Live Statistics** - Track accuracy, timing, and performance
- **Final Round** - Fast-paced bonus round with multiplied points
- **Responsive Design** - Works on desktop, tablet, and mobile

## 📁 Files

- `family-feud-enhanced.html` - Main game file
- `allQuestions.json` - Default question set (General Knowledge)

## 🚀 How to Use

### Option 1: GitHub Pages (Recommended)
1. Fork this repository
2. Go to Settings → Pages
3. Enable GitHub Pages from the `main` branch
4. Access your game at: `https://your-username.github.io/repository-name/family-feud-enhanced.html`

### Option 2: Local Use with Web Server
```bash
# Python
python3 -m http.server 8000

# Node.js
npx http-server
```
Then open: `http://localhost:8000/family-feud-enhanced.html`

### Option 3: Download and Open
Due to browser CORS restrictions, you'll need to upload a custom JSON file on the start screen if opening directly from your file system.

## 📝 Creating Custom Question Sets

Create a JSON file with this format:

```json
{
  "What is the capital of France?": [
    ["Paris", 85],
    ["London", 10],
    ["Berlin", 3],
    ["Rome", 2]
  ],
  "Name a popular sport": [
    ["Football", 45],
    ["Basketball", 30],
    ["Tennis", 15],
    ["Baseball", 10]
  ]
}
```

Each question has an array of answers with `[text, points]` format.

## ⚙️ Game Settings

- **Number of Rounds**: 1-5 (default: 3)
- **Questions per Round**: 1-6 (default: 2)
- **Time per Question**: 15-120 seconds (default: 45)
- **Strikes Allowed**: 1-5 (default: 3)
- **Final Round Multiplier**: 1-5x (default: 2x)

Settings are saved automatically to localStorage.

## 🎯 Gameplay

1. **Regular Rounds**: Teams alternate answering questions to reveal all answers
2. **Strikes**: Get 3 wrong answers and the question ends
3. **Final Round**: 5 rapid questions - only #1 answers count, points are multiplied
4. **Stats**: View live statistics during gameplay

## 🔧 Controls

- **🔊 Mute Button**: Toggle sound effects on/off
- **📊 Stats Button**: Show/hide live game statistics
- **Show All Button**: Reveal all remaining answers (useful for teachers)

## 📱 Browser Compatibility

Works in all modern browsers:
- Chrome/Edge
- Firefox
- Safari
- Mobile browsers

## 👨‍🏫 Educational Use

Perfect for:
- ESL/Language classrooms
- Review sessions
- Vocabulary practice
- Grammar reinforcement
- Cultural knowledge games

## 📄 License

Free for educational use. Created for Speak Academy ESL students.

---

**Created by Eric @ Speak Academy**
*Teaching English in the Basque Country*
