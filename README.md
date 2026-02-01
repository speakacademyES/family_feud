# Family Feud - Enhanced Classroom Edition

A fully-featured Family Feud game designed specifically for ESL classroom use with customizable questions, flexible game settings, live statistics tracking, and enhanced Final Round scoring.

## 🎮 Features

### Core Gameplay
- **Dynamic JSON Question Loading** - Use built-in questions or upload custom JSON files for different themes
- **Configurable Game Settings** - Customize every aspect of gameplay before starting
- **Answer Range Filter** - Select questions by number of answers (2-8 answers per question)
- **Sound Controls** - Mute/unmute and volume control for all sound effects
- **Live Statistics** - Track accuracy, timing, and performance in real-time
- **Enhanced Final Round** - Any correct answer scores points (not just #1!), with answer rank indicators
- **Responsive Design** - Works perfectly on desktop, tablet, and mobile devices

### Teaching Features
- **Show All Answers** button - Reveal remaining answers for educational review
- **Team Name Customization** - Personalize team names for your class
- **Flexible Timing** - Adjust question time from 15 to 120 seconds
- **Strike System** - Control difficulty with 1-5 strikes per question
- **Settings Memory** - All preferences save automatically via localStorage

## 📁 Files

- **family-feud-enhanced.html** - Main game file (self-contained)
- **allQuestions.json** - Default question set (1,826+ General Knowledge questions)
- **README.md** - This documentation file

## 🚀 How to Use

### Option 1: GitHub Pages (Recommended for Sharing)
1. Fork or upload files to a GitHub repository
2. Go to **Settings → Pages**
3. Enable GitHub Pages from the `main` branch
4. Access your game at: `https://YOUR-USERNAME.github.io/REPO-NAME/family-feud-enhanced.html`
5. Share the link with students!

### Option 2: Local Testing with Web Server
Due to browser CORS restrictions, you need a local web server:

**Using Python (easiest):**
```bash
# Navigate to the folder with your files
cd /path/to/folder

# Start server
python3 -m http.server 8000

# Open browser to:
# http://localhost:8000/family-feud-enhanced.html
```

**Using Node.js:**
```bash
npx http-server
# Then open: http://localhost:8080/family-feud-enhanced.html
```

**Using VS Code:**
1. Install "Live Server" extension
2. Right-click `family-feud-enhanced.html`
3. Select "Open with Live Server"

### Option 3: Upload to Your Web Server
Upload both HTML and JSON files to any web hosting and access via your domain.

## ⚙️ Game Settings Explained

When you start the game, you'll see these configuration options:

### 📁 Select Question Set

**Built-in Questions (General Knowledge)**
- Default option with 1,826+ pre-loaded questions
- Covers general knowledge, pop culture, everyday topics
- Perfect for mixed-level ESL classes

**Drop JSON file here or click to upload**
- Upload your own custom question files
- Great for themed lessons (holidays, grammar topics, vocabulary)
- See "Creating Custom Question Sets" below for format

### ⚙️ Game Settings

| Setting | Range | Default | Description |
|---------|-------|---------|-------------|
| **Number of Rounds** | 1-5 | 3 | How many regular rounds before Final Round |
| **Questions per Round** | 1-6 | 2 | Questions each round (teams alternate) |
| **Time per Question (sec)** | 15-120 | 45 | Countdown timer for each question |
| **Strikes Allowed** | 1-5 | 3 | Wrong answers before question ends |
| **Final Round Multiplier** | 1-5x | 2x | Points multiplier for Final Round |
| **Answer Range (Min-Max)** | 2-8 | 2-8 | Filter questions by number of answers |

#### Answer Range Examples:
- **2-4 answers**: Easier questions, good for beginners (A1-A2)
- **3-5 answers**: Medium difficulty (B1-B2)
- **5-8 answers**: Harder questions with more options (C1-C2)
- **2-2 answers**: Only questions with exactly 2 answers (very easy)
- **8-8 answers**: Only questions with exactly 8 answers (very challenging)

All settings save automatically and restore when you reload the page.

## 📝 Creating Custom Question Sets

Create a JSON file with this structure:

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
  ],
  "Name something you find in a classroom": [
    ["Desk", 40],
    ["Chair", 25],
    ["Whiteboard", 20],
    ["Books", 10],
    ["Teacher", 5]
  ]
}
```

### Format Rules:
- Each question is a key (string)
- Each answer is an array: `["answer text", points]`
- Questions should have 2-8 answers
- Points typically range from 1-100 (higher = more common answer)
- Top answers should have the highest points
- Use the Answer Range filter to select appropriate difficulty

### Themed Question Set Ideas:
- **Grammar Topics**: "Name a past tense irregular verb", "Name a modal verb"
- **Vocabulary**: "Name a type of weather", "Name a fruit"
- **Holidays**: "Name something associated with Christmas"
- **Cultural**: "Name a famous landmark in [country]"
- **Business English**: "Name something you find in an office"

## 🎯 How to Play

### Game Flow

1. **Setup Screen** → Configure settings and select question file
2. **Round Transitions** → Brief pause between rounds showing upcoming round info
3. **Regular Rounds** → Teams alternate answering questions
4. **Final Round** → One team faces 5 rapid-fire questions
5. **Game Over** → Final scores and statistics

### Regular Rounds

1. **Question appears** with all answer slots hidden
2. **Active team** has the timer duration to answer
3. **Type answer** and press Enter or click ✓
4. **Correct answer** → Reveals that slot, awards points, continues
5. **Wrong answer** → Adds a strike (⚠️)
6. **Three strikes** → Question ends, move to next question
7. **Reveal all answers** → Board shows remaining answers before moving on
8. **Teams alternate** each question

#### During Gameplay:
- Click team cards to switch active team manually
- Edit team names directly in the team cards
- Use **Pass** button to skip question
- Use **Show All** button (teacher) to reveal remaining answers

### Final Round ⭐ NEW SCORING!

The Final Round has been significantly improved:

1. **5 rapid-fire questions** (15 seconds each)
2. **Any correct answer scores points!** (not just #1)
3. **Points are multiplied** by your Final Round Multiplier
4. **Visual feedback** shows which answer you matched:
   - ✅ **#1 answer** → "ANSWER" + gold points + star celebration
   - ✅ **Other answers** → "✓ ANSWER (#3)" + gold points + success sound
   - ❌ **Wrong** → Shows #1 answer + gray points + wrong sound

#### Example:
Question: "Name something sharp"
- You answer: **"knife"** 
- Knife is answer #3 worth 25 points
- Multiplier is 2x
- **Result**: ✓ KNIFE (#3) - **50 points!** 🎉

This makes the Final Round more rewarding and less frustrating!

### Statistics Tracking

Click the **📊 Stats** button (bottom right) to view live statistics:
- Questions answered
- Correct answers
- Accuracy percentage
- Average time per answer

At game end, you'll see:
- Total questions played
- Correct answers per team
- Each team's #1 answer count
- Overall accuracy rate

## 🔧 Controls & Features

### In-Game Controls

**Bottom Right Panel:**
- **🔊 Mute Button** - Toggle all sound effects on/off
- **📊 Stats Button** - Show/hide live statistics overlay

**Volume Control:**
- Click mute button to reveal volume slider
- Drag slider to adjust sound effect volume
- Settings persist across sessions

**Answer Input:**
- Type answer and press **Enter** to submit
- Click **✓** button to submit
- Click **Pass** to skip question
- Click **Show All** to reveal remaining answers (teacher feature)

**Team Management:**
- Click team cards to switch active team
- Click team name to edit it
- Scores update automatically

### Keyboard Shortcuts

- **Enter** on overlay screens → Advance to next screen
- **Enter** in answer input → Submit answer
- All major actions have clickable buttons as well

## 🎨 Visual Feedback

### Answer Reveals
- Blue glow effect when answer is revealed
- Points displayed in gold on each answer
- Progress counter shows "Revealed: X / Y"

### Strikes
- Red ✕ appears in strike circles
- Big red ✕ flashes on screen at 3 strikes
- Animation and sound effects provide clear feedback

### Final Round
- Green checkmark for #1 answers (highlighted with celebration)
- Answer rank shown for non-#1 correct answers: "✓ ANSWER (#3)"
- Gold points for correct, gray for incorrect
- Star burst celebration for #1 answers
- Regular success sound for other correct answers

## 📱 Browser Compatibility

Tested and working in:
- ✅ Chrome/Edge (desktop & mobile)
- ✅ Firefox (desktop & mobile)
- ✅ Safari (desktop & mobile)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

Requires JavaScript enabled.

## 👨‍🏫 Educational Use Cases

### ESL Classroom Applications

**Vocabulary Building**
- Create custom questions for current vocabulary unit
- Filter by answer range for appropriate difficulty
- Use as warm-up or review activity

**Grammar Practice**
- Questions about verb forms, tenses, parts of speech
- "Name an irregular past tense verb"
- "Name a modal verb"

**Speaking Practice**
- Students must articulate answers clearly
- Encourages quick thinking in English
- Team discussion promotes conversation

**Cultural Knowledge**
- Questions about English-speaking countries
- Holidays, customs, idioms
- Build cultural awareness alongside language skills

**Exam Preparation**
- Cambridge exam-style questions
- IELTS/TOEFL topic vocabulary
- Review before tests in game format

### Difficulty Management

Use Answer Range settings to match student level:
- **Beginners (A1-A2)**: 2-3 answers, longer timer (60-90 seconds)
- **Intermediate (B1-B2)**: 3-5 answers, standard timer (45 seconds)  
- **Advanced (C1-C2)**: 5-8 answers, shorter timer (30 seconds)

### Classroom Tips

1. **Pre-teach vocabulary** from questions if needed
2. **Allow team discussion** before answering
3. **Use "Show All"** to review remaining answers
4. **Discuss why** certain answers have more points
5. **Create themed games** for upcoming lessons
6. **Let students create** their own question sets

## 🔄 Recent Updates

### Latest Changes (February 2025)

✅ **Enhanced Final Round Scoring**
- Any correct answer now scores points (not just #1)
- Visual indicators show which answer was matched
- Different celebrations for #1 vs other answers
- Makes Final Round more rewarding and educational

✅ **Answer Range Filter**
- Filter questions by number of answers (2-8)
- Allows difficulty customization per game
- Perfect for different proficiency levels
- Console logging shows filtered question count

✅ **Improved Error Handling**
- Robust JSON validation
- Helpful error messages
- Skips malformed questions automatically
- Console warnings for debugging

✅ **Settings Persistence**
- All settings save to localStorage
- Automatically restore on page reload
- No need to reconfigure each time

## 🐛 Troubleshooting

**Game won't start / "Failed to fetch" error:**
- Make sure both HTML and JSON files are in the same folder
- Use a web server (see "How to Use" section)
- Or upload to GitHub Pages
- Or upload a custom JSON file on the start screen

**No sound effects:**
- Check mute button isn't active (should show 🔊 not 🔇)
- Check device volume
- Some browsers require user interaction before playing sound

**Questions not appearing:**
- Check Answer Range settings - try 2-8 to include all questions
- Verify JSON file format is correct
- Check browser console (F12) for errors
- Ensure JSON has questions with your selected answer range

**Settings not saving:**
- Enable localStorage in browser settings
- Don't use private/incognito mode
- Clear browser cache and try again

## 📄 License

Free for educational use. Created for ESL classroom instruction.

## 🤝 Contributing

Found a bug? Have a suggestion? 
- Report issues on GitHub
- Share your custom question sets!
- Suggest new features

## 📧 Contact

**Created by Eric @ Speak Academy**  
*Teaching English in the Basque Country, Spain*

---

## 🎓 About Speak Academy

This game was created for use at Speak Academy, an ESL school in the Basque Country focusing on Cambridge exam preparation and practical English skills for students from A1 to C2 levels.

**Happy Teaching! 🎉**
