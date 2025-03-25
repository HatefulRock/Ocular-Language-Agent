# Ocular-Language-Agent

I am creating this because I love learning languages and when reading a text I found it bothersome to have to check in the dictionary for a word I didn't know. This is especially bothersome when studying Chinese or Japanese because if a word is not known the only way to look it up is to use a picture translation app or draw the character on a dictionary app. This breaks the flow when reading the text and is also pretty time consuming. Therefore, I want to have a way to automatically translate words when reading a text with as little human interaction as possible, in order to keep the reading experience smooth. This app will be centered around the Chinese language since it is the one I am studying at the moment. 

## Overview
An application that uses an eye tracker to follow the text a user is reading. Based on cues or the time spent on a specific word, the app will provide translations or additional information. This could be done via:
- A popup appearing near the word.
- A white text box replacing the word with a translation or pinyin.
- A line-based indicator with a popup appearing outside the page.

### Additional Features:
- **Word Tracking:** Keep track of words the user needed translations for.
- **Flashcards:** Users can review and add translated words to a deck (similar to Anki).
- **Active Recall:** Implement spaced repetition to reinforce learned words.
- **Sentence-Wise Translation:** If the user focuses on the start and end of a sentence, the app translates the in-between portion. A special cue can activate this feature.
- **AI-Generated Sentences:** Create interactive quizzes using words the user has learned in the session.

## Feasibility Check
- Verify if eye-tracking technology is accurate and stable enough to focus on a single word.
- If eye tracking is not viable, use a **mouse cue** method to select words and sentences for translation.

## Technical Implementation
### Required Components:
1. **OCR Model:** Extract text from PDFs.
2. **PDF Modification:** Allow drawing/marking on PDFs to indicate user intent.
3. **Eye Tracker Integration:** If accurate enough, use it for word selection. If not, explore blink-based cues.
4. **Orchestration System:** Manage app state, analyze user intent, and provide translations.
5. **LLM Agent for Translation & Analysis:**
   - Process eye-tracker data or user markings.
   - Handle word/sentence translations.
   - Potentially fine-tune a small LLM (e.g., **Gemma 3**) for specific languages.

## Future Considerations
- Fine-tune an LLM for more accurate and context-aware translations.
- Investigate using Google Colab for model fine-tuning.
- Explore ways to improve user engagement via gamification and interactive learning experiences.
