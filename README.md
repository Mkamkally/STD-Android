# Study Progress Tracker (SPT) + AI Academic Advisor

**Study Progress Tracker (SPT)** is a modern, offline-first Android application built with **Kotlin**, **Jetpack Compose (Material 3)**, and **Room Database**. It helps students organize their academic semesters, courses, lectures, labs, study notes, and reminders while featuring an intelligent **AI Academic Advisor & Data Controller** with voice dictation and multi-provider API support.

---

## 📥 Download & Install

- **[Download `SPT-v1.0.0.apk`](./SPT-v1.0.0.apk)**

> **Requirements:** Android 8.0 (API 26) or higher. Enable *"Install from unknown sources"* if prompted when installing the APK directly.

---

## ✨ Key Features

### 1. Academic Hierarchy & Study Progress Tracking
- **Semesters & Courses:** Create, rename, edit descriptions, reorder, and delete semesters and courses with persistent local Room storage.
- **Auto-Generated Lectures & Labs:** Automatically generate numbered lectures and practical labs (`Lecture 1..N`, `Lab 1..M`) when creating or updating a course.
- **Compact Difficulty & Completion Tracking:** Track completion status, estimated study duration, and difficulty levels (`Easy`, `Medium`, `Hard`).
- **Study Workspace:** Write notes per study item, organize with default and custom tags (`Exam`, `Important`, `Need Revision`, `Assignment`, `Quiz`, `Project`), and attach local device folders via Android's Storage Access Framework (`SAF`).
- **Analytics Dashboard:** Real-time calculation of overall progress percentage, completed vs. pending items, **Most Completed**, **Weakest / Least Completed**, and **Hardest** courses, plus a recent activity log.
- **Global Search:** Quickly search across semesters, courses, study items, notes, and tags.
- **Smart Reminders:** Schedule study notifications with repeat options (`Never`, `Daily`, `Weekly`, `Monthly`, `Yearly`).
- **JSON Backup & Restore:** Export your entire database to a `.json` file and restore anytime using either **Merge** or **Full Replace**.

### 2. AI Academic Advisor & Interactive Data Control
- **Weakness & Skill-Gap Diagnosis:** Analyzes your live local academic data to pinpoint weak courses, identify missing skills, and suggest tailored career paths.
- **Interactive Preview & Confirmation Cards:** Ask the AI to generate multi-semester learning roadmaps, create/rename/delete semesters or courses, or mark specific lectures and labs as completed/uncompleted—review everything in a clear preview card before applying with one tap.
- **Voice Input (Speech-to-Text):** Dedicated microphone button next to the send button for hands-free Arabic or English voice dictation directly into the chat box.
- **Flexible AI Provider Support (Built-in + BYOK):**
  - Powered out of the box by **Groq (`openai/gpt-oss-120b`)**.
  - Full **Bring Your Own Provider** support in **Settings**: enter any custom **Base URL**, **Model Name**, and **API Key** (supports Groq, OpenAI, OpenRouter, DeepSeek, Google Gemini, or any OpenAI-compatible endpoint) with a built-in **Test Connection** button.

### 3. Bilingual Interface & Custom Theming
- **Arabic & English Support:** Arabic (RTL) by default with an instant in-app toggle to switch between **العربية** and **English** in Settings.
- **Two-Tone Material 3 Design & Custom Color Picker:** Clean light/dark/system themes with **Emerald**, **Blue**, and an interactive **HSV + Hex Custom Color Picker** so you can choose any accent shade.
