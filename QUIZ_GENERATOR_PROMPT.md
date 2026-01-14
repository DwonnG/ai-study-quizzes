# Interactive Study Quiz Generator Prompt

Generate interactive HTML study quizzes using AI! Works with Claude, ChatGPT, Cursor, Copilot, or any AI assistant.

---

## 🚀 HOW TO USE (4 Easy Steps):

### Step 1: Copy the Prompt
Copy everything inside the ``` code blocks in the **"THE PROMPT"** section below (or use the **"QUICK VERSION"** at the bottom for a shorter option).

### Step 2: Paste into Your AI
Open your AI assistant and paste the prompt:
- **Cursor** - Paste in chat or Composer
- **Claude** - Paste in conversation
- **ChatGPT** - Paste in chat
- **Copilot** - Paste in chat

### Step 3: Add Your Study Material
At the end where it says `[PASTE YOUR STUDY GUIDE CONTENT HERE]`:
- **Option A**: Paste text directly from the study guide
- **Option B**: Attach/upload images of the study guide (most AI can read images!)
- **Option C**: Type out the key concepts and topics

### Step 4: Send & Save
- Send the message - the AI will generate a complete HTML file
- Save the output as `quiz_name.html`
- Open in any web browser to use!

💡 **Pro Tip**: You can just pass in images of the study guide - the AI will extract the content!

---

## 📋 THE PROMPT (Copy Everything Below)

```
Create an interactive HTML quiz for the following study material. Include ALL of these features:

## REQUIRED FEATURES:

1. **Vocabulary Flashcard Section**
   - Show key terms BEFORE the quiz starts
   - Tap-to-flip cards with term on front, definition + example on back
   - Color-coded by topic/category

2. **Question Bank**
   - Create 3-5x MORE questions than needed (e.g., 50+ questions for a 15-question quiz)
   - Include alternate wordings of similar concepts
   - Group questions by topic/category

3. **Balanced Topic Coverage**
   - Define quotas per category (e.g., 4 questions from Topic A, 3 from Topic B)
   - GUARANTEE all topics appear in every quiz
   - Use a categoryQuotas object like:
     ```javascript
     const categoryQuotas = {
         "Topic A": 4,
         "Topic B": 3,
         "Topic C": 3
     };
     ```

4. **Anti-Memorization**
   - Shuffle question ORDER each quiz
   - Shuffle answer OPTIONS within each question
   - Track correct answer by VALUE not position

5. **Timer System**
   - Per-question countdown (25-30 seconds)
   - Visual countdown circle that changes color (green → yellow → red)
   - Total elapsed time tracking
   - Auto-submit when time runs out

6. **Instant Feedback**
   - Show correct answer immediately after each question
   - Include explanation of WHY it's correct
   - Speed bonus indicator for fast answers (under 15 seconds)

7. **Results Screen with Review Recommendations**
   - Percentage score with letter grade
   - Total time and average time per question
   - "Topics to Review" section showing categories with missed questions
   - Score breakdown by category (e.g., "Irregular Verbs: 4/5")
   - Color-coded scores: green (100%), orange (50%+), red (<50%)

8. **Buttons**
   - "Try Again" to restart quiz
   - "Review Vocab" to go back to flashcard section

## QUESTION FORMAT:
Each question should follow this structure:
```javascript
{
    category: "Topic Name",
    categoryClass: "topicCssClass",
    question: "Your question here?",
    options: ["A", "B", "C", "D"],
    correctAnswer: "B",  // Must exactly match one option
    explanation: "Why this answer is correct."
}
```

## STYLING:
- Dark gradient background
- Color-coded category badges on questions
- Smooth animations for card transitions
- Mobile-responsive design
- Visual timer with circular progress indicator

## HERE IS MY STUDY MATERIAL:

[PASTE YOUR STUDY GUIDE CONTENT HERE]
```

---

## 🔢 FOR MATH QUIZZES - Additional Requirements:

Add these specifications when creating math quizzes (fractions, multiplication, etc.):

```
## MATH-SPECIFIC FEATURES:

1. **Extended Timer**
   - Use 90-120 seconds per question (math problems take longer to solve!)
   - Keep visual countdown but adjust color thresholds accordingly
   - Speed bonus for answers under 60 seconds instead of 15

2. **Fraction/Math Display**
   - Use proper fraction notation (superscript/subscript like ³⁄₄)
   - For mixed numbers, show whole number + fraction clearly (2³⁄₄)
   - Use × for multiplication, ÷ for division
   - Consider using HTML fraction display or Unicode fractions

3. **Step-by-Step Explanations**
   - Explanations should show HOW to solve, not just the answer
   - Example: "First find a common denominator (12), then convert: ³⁄₄ = ⁹⁄₁₂ and ²⁄₃ = ⁸⁄₁₂, then add: ⁹⁄₁₂ + ⁸⁄₁₂ = ¹⁷⁄₁₂ = 1⁵⁄₁₂"

4. **Bilingual Math (if Spanish)**
   - Questions in Spanish with hover translations for math vocabulary
   - Keep results/feedback section in ENGLISH for parent review
   - Key terms to translate: numerador, denominador, fracción equivalente, número mixto

5. **Math Vocabulary Flashcards**
   - Include visual representations where helpful
   - Show fraction bars or pie charts in examples
   - Define: numerator, denominator, equivalent, mixed number, improper fraction
```

### Example Math Quiz Prompt:

```
Create an interactive HTML quiz for this 4th grade fractions study guide.

MATH-SPECIFIC: Use 120-second timer (2 minutes per question).
Questions are in Spanish - add hover translations for vocabulary.
Results section should be in ENGLISH.
Show step-by-step solutions in explanations.

Topics:
- Adding & Subtracting Fractions (Sumar y Restar)
- Comparing Fractions (Comparar Fracciones)  
- Equivalent Fractions (Fracciones Equivalentes)
- Decomposing Fractions (Descomponer Fracciones)
- Mixed Numbers (Números Mixtos)

[PASTE STUDY MATERIAL HERE]
```

---

## 💡 TIPS FOR BEST RESULTS:

1. **Paste the entire study guide** - The more content you provide, the better the questions will be.

2. **Specify the grade level** - Add "This is for a 4th grader" or "9-year-old" so the AI uses appropriate language.

3. **List the topics** - Tell the AI what categories/topics are in the material.

4. **Specify number of questions** - Say "Create a quiz with 15-20 questions per session" or similar.

5. **Request bilingual if needed** - Add "Include Spanish translations" or "Add hover translations for vocabulary words."

---

## 📝 EXAMPLE USAGE:

```
Create an interactive HTML quiz for the following study material. Include ALL of these features:

[... all the features listed above ...]

This is for a 4th grader (9 years old).

Topics covered:
- Irregular Verbs (past tense)
- Homophones (to/too/two, their/there/they're)
- Irregular Plurals
- Quotation Marks
- Helping Verbs
- Linking Verbs

Create 50+ questions total, showing 18 per quiz session.

HERE IS MY STUDY MATERIAL:

[paste study guide here]
```

---

## 🎯 QUICK VERSION (Shorter Prompt):

If you want a shorter prompt, use this:

```
Create an interactive HTML study quiz from this material:

Features needed:
- Vocabulary flashcards before quiz (tap to flip)
- 3x more questions than shown per quiz for variety
- Shuffle questions AND answers each time
- Guarantee all topics appear (use categoryQuotas)
- 25-second timer per question with visual countdown
- Instant feedback with explanations
- Results show "Topics to Review" based on missed questions
- Score breakdown by category

[PASTE STUDY MATERIAL HERE]
```

---

Created for generating study quizzes like: grammar_quiz.html, social_studies_quiz.html, science_sound_light_quiz.html, fractions_quiz.html




