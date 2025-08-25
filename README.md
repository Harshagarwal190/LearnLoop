<img width="1584" height="396" alt="image" src="https://github.com/user-attachments/assets/28ad69d9-14a9-46ae-805d-ae3646c4e6a3" />

<div align="center">
  <h1 align="center">LearnLoop 🧠🔁</h1>
  <p align="center">
    An automated n8n workflow that creates a continuous learning cycle by delivering daily, AI-generated practice questions for technical interviews directly to your email.
    <br />
    <br />
    <a href="#about-the-project"><strong>Workflow of Automation</strong></a>
    <br />
    <br />
    <img width="1100" height="539" alt="image" src="https://github.com/user-attachments/assets/c89e2d72-2481-455c-8416-6b82468aafa3" />
    <a href="#about-the-project"><strong>Output</strong></a>
    <br />
    <br />
    <img width="1435" height="793" alt="image" src="https://github.com/user-attachments/assets/e0639a02-cc2b-4cc8-8125-5b82881322db" />
    <img width="1169" height="755" alt="image" src="https://github.com/user-attachments/assets/91add168-f9e5-45a9-a312-2a536e3c9d7f" />


  </p>
</div>

-----

### **Table of Contents**

1.  [Why LearnLoop?](https://www.google.com/search?q=%23-why-learnloop)
2.  [Key Features](https://www.google.com/search?q=%23-key-features)
3.  [How It Works](https://www.google.com/search?q=%23-how-it-works)
4.  [Getting Started](https://www.google.com/search?q=%23-getting-started)
5.  [Customization](https://www.google.com/search?q=%23-customization)

-----

## 🤔 Why LearnLoop?

In the competitive landscape of tech placements, consistent practice is the key to success. However, the daily grind of searching for high-quality, relevant interview questions is a time-consuming chore that breaks your focus.

> **LearnLoop** solves this by putting your preparation on autopilot. It acts as a personal learning agent, delivering a fresh set of practice questions directly to your inbox every morning. Stop searching and start solving.

-----

## ✨ Key Features

  * **🤖 AI-Powered Content**: Leverages a **Large Language Model (LLM)** to generate unique and challenging questions on topics like DSA, OS, DBMS, and more.
  * **⏰ Fully Automated**: A "set it and forget it" **daily schedule** ensures you never miss a day of practice.
  * **🎨 Beautifully Formatted Emails**: Delivers questions in a clean, responsive HTML email that's easy to read on any device.
  * **🔧 Highly Customizable**: Easily tweak the topics, schedule, difficulty, and recipients to perfectly match your study plan.
  * **✅ Structured & Reliable**: The AI prompt is engineered to return a predictable **JSON output**, ensuring the workflow is robust and error-free.

-----

## 🛠️ How It Works

The workflow is a simple yet powerful pipeline composed of three main stages:

1.  **🗓️ The Pacemaker (Schedule Trigger)**

      * The workflow is initiated by a **Schedule Trigger** node. It's configured to run at a specific time every day (e.g., 7:00 AM), ensuring a consistent delivery schedule.

2.  **🧠 The Brains (AI Agent)**

      * This is where the magic happens. A carefully crafted prompt is sent to an LLM (like GPT-4).
      * The prompt instructs the AI to act as an expert tutor and generate a structured **JSON output** containing questions, options, answers, and detailed explanations.

3.  **📨 The Messenger (Gmail Sender)**

      * The final node takes the structured data from the AI Agent.
      * It dynamically formats this data into a clean HTML email body.
      * Finally, it sends the email to your specified address, completing the daily loop.

-----

## 🚀 Getting Started

Get your own instance of LearnLoop running in minutes.

### Prerequisites

  * A running **n8n instance** (cloud or self-hosted).
  * An **OpenAI API Key** with available quota.
  * **Gmail credentials** configured in your n8n instance.

### Installation & Configuration

1.  **Download & Import**: Clone this repository and import the `LearnLoop-Workflow.json` file into your n8n instance.
2.  **Configure Credentials**:
      * In the **"Question Generator Agent"** node, select your pre-configured OpenAI credentials.
      * In the **"Send Email"** node, select your pre-configured Gmail credentials.
3.  **Set Your Details**:
      * Update the **"Send Email"** node with your desired recipient email address.
      * Customize the schedule in the **"Daily Trigger"** node.
4.  **Activate**: Click the **"Active"** toggle at the top-right of the screen. You're all set\!

-----

## 🔧 Customization

One of the best features of LearnLoop is its flexibility.

  * **Change Topics**: Open the **"Question Generator Agent"** node and edit the prompt to add or remove subjects like "System Design" or "Cloud Computing".
  * **Adjust Difficulty**: Modify the prompt to ask for `"beginner-friendly"` or `"expert-level"` questions.
  * **Change Schedule**: Click the **"Schedule Trigger"** node to change the time or frequency (e.g., weekdays only).
  * **Use a Different Email Service**: Swap the **Gmail** node for another email node like Outlook or SendGrid by re-wiring the connections.

-----

## 🤝 Contributing
Contributions, issues, and feature requests are welcome\! Feel free to check the [issues page](https://github.com/your-username/LearnLoop/issues).

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.
