# Cisco Quiz Answer Script README

## Overview
This TypeScript script is designed to assist students, particularly those in Dev IT programs, with answering Cisco networking quiz questions by automatically displaying correct answers when a question is selected on a webpage. The script is meant to be used discreetly in the browser's DevTools console, as it provides a quick way to bypass the tedious process of memorizing Cisco networking concepts, which many Dev IT students find irrelevant to their career goals.

### Why This Script Exists
Let's be real: Cisco networking and *réseaux* in general can feel like a soul-crushing slog for Dev IT students. We're here to code apps, build systems, or work on cutting-edge tech, not to memorize VLAN configurations or Spanning Tree Protocol minutiae. Unfortunately, passing these Cisco-heavy courses is often a mandatory hurdle to move forward in our academic or professional journey. This script is a rebellion against that grind—a tool to help you get through the quizzes quickly so you can focus on what actually matters to you, like coding or literally anything else.

## How to Use the Script

### Prerequisites
- A modern web browser (e.g., Chrome, Firefox, Edge) with DevTools support.
- Basic knowledge of how to open and use the browser's DevTools console.
- The quiz webpage containing Cisco networking questions (e.g., from a learning platform).

### Steps to Use
1. **Open the Quiz Webpage**:
   - Navigate to the webpage containing the Cisco quiz questions.

2. **Open DevTools**:
   - Right-click anywhere on the page and select **Inspect** or press `Ctrl + Shift + I` (Windows/Linux) or `Cmd + Option + I` (Mac) to open DevTools.
   - Go to the **Console** tab in DevTools.

3. **Copy and Paste the Script**:
   - Copy the entire TypeScript code provided.
   - Paste it into the DevTools console and press **Enter** to run it.

4. **Select a Question**:
   - Highlight the text of a question on the quiz page by clicking and dragging over it.
   - If the selected text matches a question in the script's database, a **small white rectangle** will appear at the bottom of the page displaying the correct answer(s).
   - The rectangle disappears after **1 second** to avoid detection by instructors or proctors.

5. **Disabling the Script (If Caught)**:
   - If you suspect you're being monitored or want to disable the script for any reason, select the word **"question"** (case-insensitive) on the page.
   - This will disable the script, clear the console, and remove any visual elements it created.
   - To re-enable the script, you must paste it into the DevTools console again and run it.

### Example Workflow
1. You’re on a Cisco quiz page with a question like: *"Dans quelle situation un technicien utilise-t-il la commande de commutateur show interfaces ?"*
2. You select the question text by highlighting it.
3. A white box briefly appears at the bottom of the page with the answer: *"Lorsque des paquets sont reçus d’un hôte donné qui est directement connecté"*
4. If a proctor is nearby, select the word "question" to disable the script instantly.

## Features
- **Answer Lookup**: Matches selected question text to a predefined database of Cisco quiz questions and displays the correct answer(s).
- **Discreet Operation**: The answer display is temporary (1 second) to minimize the risk of detection.
- **Anti-Detection Mechanism**: Selecting the word "question" disables the script, clears the console, and removes any visual traces.
- **Shadow DOM Support**: Works with modern web pages that use shadow DOM, ensuring compatibility with various quiz platforms.
- **Transparent Selection**: Removes the default text selection highlight to make your actions less noticeable.

## Why We Hate Cisco and Réseaux
As Dev IT students, we're often more passionate about software development, cloud computing, or cybersecurity than about configuring routers and switches. Cisco's networking curriculum feels like a relic from another era, forcing us to learn arcane commands and protocols that seem disconnected from modern development workflows. Here’s why this stuff drives us nuts:
- **Irrelevant to Our Goals**: Most of us want to build apps, work with APIs, or dive into DevOps, not troubleshoot VLAN misconfigurations.
- **Overly Complex**: Cisco’s command-line interface and endless acronyms (VTP, DTP, STP, HSRP, etc.) feel like unnecessary gatekeeping.
- **Time Sink**: Hours spent memorizing Cisco trivia could be better spent on learning frameworks, algorithms, or real-world coding skills.
- **Mandatory Hurdle**: Despite our disinterest, passing these courses is often required to graduate or move on to more relevant topics.

This script is our way of saying, "We’re done with this nonsense." It’s a tool to help you pass the Cisco gauntlet with minimal frustration so you can get back to what you love.

## Limitations
- **Question Database**: The script only works for questions included in its predefined `questions` array. If a quiz has different questions, you’ll need to update the script with the new question-answer pairs.
- **Webpage Compatibility**: The script assumes the quiz questions are displayed as selectable text. If the quiz uses images or locked text, it won’t work.
- **Detection Risk**: While the script is designed to be discreet, using it in a proctored environment carries risks. Always be cautious and use the disable feature if needed.
- **No Answer Marking**: The script avoids permanently marking answers on the page to reduce detection risk, so you’ll need to manually note the answers.

## How to Update the Question Database
If you encounter new quiz questions, you can add them to the `questions` array in the script. The format is:
```typescript
{
  question: "Your question text here",
  options: ["Option 1", "Option 2", "Option 3", "Option 4"],
  answer: ["Correct answer"] // or ["Answer 1", "Answer 2"] for multiple answers
}
