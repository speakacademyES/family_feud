# Family Feud Game Generator Prompt

Use this prompt to generate Family Feud-style quiz games from vocabulary lists or grammar concepts for your ESL students.

---

## PROMPT TEMPLATE:

```
I need you to create a Family Feud game JSON file for my ESL students. Here's what I need:

**Topic/Theme:** [e.g., "Irregular Verbs - Past Simple", "Food Vocabulary B1 level", "Phrasal Verbs with 'get'"]

**CEFR Level:** [A1, A2, B1, B2, C1, C2]

**Vocabulary/Grammar Items:**
[Paste your list here - can be a simple list, CSV, or any format]

**Number of Questions:** [e.g., 15-20 questions]

**Special Instructions (optional):**
- [e.g., "Focus on British English variations"]
- [e.g., "Include common student errors as acceptable answers"]
- [e.g., "Make questions suitable for teenagers"]
- [e.g., "Include Spanish cognates as variations"]

## REQUIREMENTS:

1. **JSON Structure:**
   - Each question should have 5-8 possible answers
   - Each answer should be an array of variations (not just a single string)
   - Include point values (higher points for more common/important answers)
   - Format: `{"Question text": [[["answer1", "variation1", "variation2"], points], ...]}`

2. **Answer Variations Must Include:**
   - Original answer
   - Singular/plural forms
   - Common misspellings students make
   - British vs American English variants (where applicable)
   - With/without articles (the, a, an)
   - Synonyms and related terms
   - Common abbreviations
   - Alternative phrasings
   - Compound word variations (e.g., "homework" vs "home work")
   - For Spanish speakers: Include common Spanish-influenced errors

3. **Question Types Should:**
   - Be clear and appropriate for the CEFR level
   - Use natural, authentic English
   - Cover different aspects of the vocabulary/grammar topic
   - Be engaging and relevant to student interests
   - Include context when helpful

4. **Point Distribution:**
   - Most common/important answers: 40-60 points
   - Secondary answers: 15-30 points
   - Less common but valid answers: 5-15 points
   - Ensure total roughly equals 100 per question

Please generate the complete JSON file ready to use in my Family Feud game application.
```

---

## EXAMPLE USAGE:

### Example 1: Irregular Verbs

```
I need you to create a Family Feud game JSON file for my ESL students. Here's what I need:

**Topic/Theme:** Irregular Verbs - Past Simple Forms

**CEFR Level:** B1

**Vocabulary/Grammar Items:**
go, eat, drink, see, make, take, come, think, know, get, give, find, tell, become, leave, feel, bring, begin, keep, write

**Number of Questions:** 12 questions

**Special Instructions:**
- Include common student errors (e.g., "goed" for "went")
- Focus on the most frequently used irregular verbs
- Make questions practical and relatable to daily life

Please generate the complete JSON file ready to use in my Family Feud game application.
```

### Example 2: Food Vocabulary

```
I need you to create a Family Feud game JSON file for my ESL students. Here's what I need:

**Topic/Theme:** Food and Cooking Vocabulary

**CEFR Level:** A2

**Vocabulary/Grammar Items:**
breakfast, lunch, dinner, vegetables, fruits, meat, chicken, fish, rice, pasta, bread, cheese, milk, eggs, water, juice, coffee, tea, sugar, salt

**Number of Questions:** 10 questions

**Special Instructions:**
- Include both British and American English (e.g., "courgette"/"zucchini")
- Make questions about meals, shopping, and restaurants
- Include plural/singular variations
- Add common food-related phrases

Please generate the complete JSON file ready to use in my Family Feud game application.
```

### Example 3: Phrasal Verbs

```
I need you to create a Family Feud game JSON file for my ESL students. Here's what I need:

**Topic/Theme:** Phrasal Verbs with "take"

**CEFR Level:** B2

**Vocabulary/Grammar Items:**
take off, take out, take up, take after, take over, take in, take back, take down, take on, take away

**Number of Questions:** 8 questions

**Special Instructions:**
- Questions should test understanding of meaning, not just form
- Include sentences with context
- Add variations without pronouns (e.g., "take it off" vs "take off")
- Include both separable and inseparable uses

Please generate the complete JSON file ready to use in my Family Feud game application.
```

---

## TIPS FOR BEST RESULTS:

1. **Be specific about your target audience** - mention if they're teenagers, adults, business English, etc.

2. **Provide context** - if the vocabulary comes from a specific textbook unit or theme, mention it

3. **Specify any cultural adaptations** - especially important for Spanish speakers in Basque Country

4. **Include error patterns** - if you know common mistakes your students make, tell Claude to include them as acceptable variations

5. **Request preview** - ask Claude to show you a sample question before generating the full file

6. **Mix question types** - request different formats like:
   - "Name a verb that means..." (definitions)
   - "Complete the phrase: take ___" (collocations)
   - "Name something you would ___ at a restaurant" (context)

---

## QUALITY CHECKLIST:

After receiving the generated JSON, verify:

- [ ] All answers have multiple variations (minimum 3-5 per answer)
- [ ] Variations include common student errors
- [ ] British/American variants included where relevant
- [ ] Points distributed appropriately (totaling ~100 per question)
- [ ] Questions are clear and appropriate for CEFR level
- [ ] Grammar/spelling is correct in all variations
- [ ] JSON format is valid and ready to use

---

## CUSTOMIZATION OPTIONS:

You can also request:

- **Themed questions** (e.g., "Christmas vocabulary", "Business presentations")
- **Cambridge exam focus** (e.g., "B2 First speaking topics")
- **Grammar patterns** (e.g., "Present Perfect vs Past Simple")
- **Pronunciation focus** (include phonetic spellings as variations)
- **Mixed skills** (combine multiple grammar points or vocabulary sets)

---

## FOLLOW-UP REQUESTS:

If you need adjustments after generation:

- "Add more variations for [specific answer]"
- "Make the questions easier/harder"
- "Add more questions about [topic]"
- "Include more Spanish-influenced variations"
- "Adjust point values - make [answer] worth more"
- "Add questions that test [specific grammar point]"

---

**Save this prompt template and modify the sections in [brackets] for each new game you want to create!**
