Hadiest – Multi-modal AI Music Assistant
Hadiest là một trợ lý ảo AI đa phương thức có khả năng trò chuyện, nhận diện bài hát từ âm thanh và gợi ý nhạc tự động. Hệ thống kết hợp mô hình ngôn ngữ lớn (LLM) với xử lý tín hiệu âm thanh để tạo trải nghiệm tương tác tự nhiên bằng văn bản và giọng nói.

🌟 Features
1. Intelligent Chatbot
Sử dụng AI Agent (ReAct) với mô hình Llama-3.3-70B để trò chuyện, tâm sự và phản hồi theo ngữ cảnh.
Hỗ trợ hội thoại tự nhiên, không phản hồi cứng nhắc.
2. Multi-modal Interaction
Nhập văn bản trực tiếp.
Ghi âm giọng nói từ microphone.
Xử lý yêu cầu bằng cả text và audio.
3. Advanced Audio Processing
Pipeline xử lý âm thanh gồm:
Voice Activity Detection: Tách giọng nói và loại bỏ khoảng lặng.
Speech-to-Text: Chuyển giọng nói thành văn bản.
Noise filtering & silence removal: Xử lý audio bằng FFmpeg.
Song Recognition: Nhận diện bài hát từ đoạn audio ngắn (~3–5s).
4. Music Integration
Tìm kiếm bài hát trên YouTube.
Hiển thị YouTube player trực tiếp trong giao diện chat.
Gợi ý nhạc dựa trên hội thoại và cảm xúc người dùng.
5. Conversation Memory
Lưu lịch sử hội thoại theo Session ID.
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
HTML, CSS
AI & APIs
Groq (Llama-3.3-70B)
YouTube Data API v3
ACRCloud API
Audio Processing
FFmpeg
Silero VAD
SpeechRecognition

📂 Project Structure
hadiest/
│
├── agents/             # AI Agent, reasoning logic, tools
├── audio_processing/   # Audio pipeline, STT, song recognition
├── backend/            # FastAPI server, routing, session, memory
├── frontend/           # Web interface
├── main.py             # Application entry point
├── requirements.txt
└── .env.sample

🚀 Installation
1. Clone repository
git clone https://github.com/HaNgo2k4/chatbot-hadiest
cd chatbot-hadiest
2. Install dependencies
pip install -r requirements.txt
3. Setup environment variables
Tạo file .env từ .env.sample và điền các API key:
GROQ_API_KEY=
YOUTUBE_API_KEY=
ACRCLOUD_ACCESS_KEY=
ACRCLOUD_ACCESS_SECRET=
ACRCLOUD_REQ_URL=
REDIS_URL=
4. Run application
python main.py
Sau đó mở frontend để bắt đầu trò chuyện với chatbot.

🧠 System Architecture (Concept)
Hệ thống được thiết kế theo kiến trúc:
Modular architecture
API-based architecture
Scalable backend
AI Agent + Tools
Audio Processing Pipeline
Redis Memory
Flow hệ thống:
User (Text/Voice)
       ↓
Frontend (Web)
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

📌 Project Highlights
Multi-modal AI Chatbot (Text + Voice)
ReAct AI Agent with tool calling
Song recognition from short audio
Audio processing pipeline
Redis conversation memory
Full-stack FastAPI + JavaScript
Modular & scalable architecture
