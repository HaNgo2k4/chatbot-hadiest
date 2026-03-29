🎵 Hadiest – Multi-modal AI Music Assistant

Hadiest là một trợ lý ảo AI đa phương thức có khả năng trò chuyện, nhận diện bài hát từ âm thanh và gợi ý nhạc tự động.
Dự án kết hợp mô hình ngôn ngữ lớn (LLM), AI Agent và xử lý tín hiệu âm thanh để tạo trải nghiệm tương tác tự nhiên bằng văn bản và giọng nói.

🌟 Features
🤖 Intelligent AI Chatbot
Sử dụng AI Agent (ReAct) để suy luận và phản hồi theo ngữ cảnh hội thoại.

Có thể trò chuyện, tâm sự và gợi ý nhạc theo cảm xúc người dùng.

Hỗ trợ hội thoại dài nhờ lưu lịch sử trò chuyện.

🎙 Multi-modal Interaction

Nhập văn bản trực tiếp.

Ghi âm giọng nói từ microphone.

Xử lý yêu cầu bằng cả text và audio.

🎧 Advanced Audio Processing Pipeline

Hệ thống xử lý âm thanh gồm nhiều bước:

Voice Activity Detection (Silero VAD) – phát hiện giọng nói và loại bỏ khoảng lặng.

Speech-to-Text – chuyển giọng nói thành văn bản.

Noise filtering & silence removal bằng FFmpeg.

Song Recognition – nhận diện bài hát từ đoạn audio ngắn (~3–5 giây) bằng ACRCloud.

🎶 Music Recommendation & YouTube Integration

Tìm kiếm bài hát trên YouTube.

Hiển thị YouTube player trực tiếp trong giao diện chat.

Gợi ý nhạc dựa trên nội dung hội thoại và cảm xúc người dùng.

🧠 Conversation Memory

Lưu lịch sử hội thoại theo Session ID bằng Redis.

AI có thể ghi nhớ ngữ cảnh hội thoại dài.

Tính năng Clear History để xóa dữ liệu hội thoại.

🛠 Tech Stack

Backend

Python

FastAPI

LangChain

LangGraph

Redis

Frontend

JavaScript

HTML

CSS

AI & APIs

Groq API (Llama-3 LLM)

YouTube Data API

ACRCloud API

Audio Processing

FFmpeg

Silero VAD

SpeechRecognition

## System Architecture

```text
Text/Voice Input
      ↓
Frontend (Web UI)
      ↓
FastAPI Backend
      ↓
AI Agent (LangChain + LangGraph)
      ↓
Tools:
    - Speech-to-Text
    - Song Recognition
    - YouTube Search
    - Redis Memory
      ↓
LLM (Llama-3 via Groq)
      ↓
Response → Frontend
```
Hệ thống được thiết kế theo kiến trúc:

Modular architecture

Scalable architecture

API-based architecture

AI Agent + Tools

Audio Processing Pipeline

Redis Conversation Memory

📂 Project Structure
```text
hadiest/
│
├── agents/             # AI Agent, reasoning logic, tools
├── audio_processing/   # Audio pipeline, STT, song recognition
├── backend/            # FastAPI server, routing, session, memory
├── frontend/           # Web interface
├── main.py             # Application entry point
├── requirements.txt
└── .env.sample
```
🚀 Installation
1. Clone repository

```text
git clone https://github.com/HaNgo2k4/chatbot-hadiest
cd chatbot-hadiest
```
2. Install dependencies
```text
pip install -r requirements.txt
```
3. Setup environment variables

Tạo file .env từ .env.sample và điền các API key:
```text
GROQ_API_KEY=
YOUTUBE_API_KEY=
ACRCLOUD_ACCESS_KEY=
ACRCLOUD_ACCESS_SECRET=
ACRCLOUD_REQ_URL=
REDIS_URL=
```
4. Run application
```text
python main.py
```
Sau đó mở frontend để bắt đầu trò chuyện với chatbot.

📌 Project Highlights

Multi-modal AI Chatbot (Text + Voice)

ReAct AI Agent with tool calling

Song recognition from short audio

Audio processing pipeline

Redis conversation memory

Full-stack FastAPI + JavaScript

Modular & scalable architecture

🔮 Future Improvements

Text-to-Speech (AI trả lời bằng giọng nói)

Emotion detection từ giọng nói

Recommendation system cho nhạc

👨‍💻 Author

HaNgo2k4

GitHub: https://github.com/HaNgo2k4/chatbot-hadiest

⭐ If you find this project useful, please give it a star!
