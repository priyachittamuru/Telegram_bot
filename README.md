# Telegram_bot
This Telegram bot is a friendly AI assistant for Team Chirag, designed to answer user questions naturally and contextually. It remembers past conversations, provides quick replies to FAQs, and maintains a helpful, human-like tone — making learning and communication seamless for students and community members.

This repository demonstrates how to build a **context-aware Telegram bot** using **Zapier**, **OpenAI**, and **Telegram Bot API**. The bot can remember conversations, answer FAQs, and provide natural, real-time responses.

## Links to Telegram Bot and Zap Workflow
1. [Test_bot](http://t.me/Train_nov1_bot)
2. [Zap Link](https://zapier.com/shared/bba25443fcd3a02e331c9c6b39a7b163df87d948)

---

## ⚙️ What It Does

This Zap allows your Telegram bot to:  
- Receive user messages in real time  
- Remember past conversations using **Zapier Storage**  
- Generate natural, context-based replies via **OpenAI (GPT-3.5-Turbo-Instruct)**  
- Instantly send responses back to the Telegram chat  

---

## 🛠 Workflow Summary

1. **Trigger:** Telegram Bot → *New Message Received*  
2. **Retrieve Memory:** Fetch prior conversation from Zapier Storage  
3. **Combine Messages:** Merge old memory and new message using Formatter by Zapier  
4. **Generate AI Response:** Send prompt to OpenAI GPT model  
5. **Update Memory:** Save latest conversation back to Zapier Storage  
6. **Send Reply:** Post AI-generated message back to Telegram  

---

## 👥 Who Should Use It

- Educators, coaches, or community managers looking for an **AI-powered Telegram assistant**.  
- Teams needing **automated, context-aware support** or FAQ handling.  

---

## 💡 Benefits

- Provides **24/7 conversational support** without coding  
- Maintains conversation context for **natural and relevant replies**  
- Scales effortlessly for **one-on-one or group chats**  

---

## 📌 Setup Instructions

1. **Create Telegram Bot**  
   - Search for [BotFather](https://t.me/BotFather) on Telegram  
   - Create a new bot and save the **Bot Token** and **Bot Link**  

2. **Connect Telegram with Zapier**  
   - Create a new Zap → Trigger: *Telegram Bot – New Message Received*  
   - Connect your bot using the Bot Token  

3. **Set Up Memory Storage**  
   - Action: *Storage by Zapier – Get Value*  
   - Use UUID as Store Secret and configure keys for each chat  

4. **Combine Old Memory and New Message**  
   - Action: *Formatter by Zapier – Line Itemizer*  

5. **Generate Contextual Reply**  
   - Action: *OpenAI – Send Prompt*  
   - Model: `gpt-3.5-turbo-instruct`  
   - Insert prompt with FAQs and conversation context  

6. **Store Updated Memory**  
   - Action: *Storage by Zapier – Set Value*  

7. **Send Reply to Telegram**  
   - Action: *Telegram Bot – Send Message*  
   - Map the response from OpenAI  

---

## 🔗 References

- [Telegram Bot API](https://core.telegram.org/bots/api)  
- [Zapier Storage](https://zapier.com/apps/storage/help)  
- [OpenAI API](https://platform.openai.com/docs/api-reference/introduction)  

---

## ⚡ Notes

- Make sure to test each step in Zapier to confirm messages are passing correctly.  
- Update the OpenAI prompt to include FAQs specific to your use case.  

---

