Hadiest - Multi-modal AI Music Assistant
Hadiest là một trợ lý ảo thông minh đa phương thức, được thiết kế để trở thành một người bạn tâm sự và chuyên gia gợi ý âm nhạc Việt Nam
. Dự án kết hợp sức mạnh của các mô hình ngôn ngữ lớn (LLM) với khả năng xử lý âm thanh kỹ thuật số để mang lại trải nghiệm tương tác tự nhiên và trực quan.
🌟 Tính năng nổi bật
Trò chuyện thông minh: Sử dụng AI Agent (mô hình Llama-3.3-70b) để thảo luận, tâm sự và phản hồi người dùng một cách thân thiện, không cứng nhắc
.
Tương tác đa phương thức: Hỗ trợ cả nhập liệu bằng văn bản và ghi âm giọng nói trực tiếp từ microphone
.
Xử lý âm thanh chuyên sâu:
Phân tách tín hiệu: Sử dụng Silero VAD để tự động tách biệt giọng nói người dùng và nhạc nền
.
Nhận diện bài hát: Tích hợp ACRCloud API để định danh bài hát từ đoạn nhạc thu âm được qua micro
.
Chuyển đổi giọng nói (STT): Nhận diện yêu cầu bằng giọng nói tiếng Việt thông qua thư viện SpeechRecognition
.
Lọc nhiễu: Tự động cắt bỏ các khoảng lặng ở đầu và cuối file âm thanh bằng FFmpeg
.
Tích hợp âm nhạc: Tìm kiếm và hiển thị trình phát video YouTube trực tiếp trong giao diện hội thoại khi người dùng yêu cầu nghe nhạc
.
Quản lý trí nhớ (Memory): Sử dụng Redis để lưu trữ lịch sử trò chuyện theo từng phiên (Session ID), giúp trợ lý ghi nhớ ngữ cảnh hội thoại
.
Quyền riêng tư: Tính năng "Clear History" cho phép người dùng xóa sạch dữ liệu hội thoại trên cả giao diện và máy chủ
.
🛠 Công nghệ sử dụng
Backend: Python, FastAPI
.
Frontend: JavaScript, HTML, CSS (Thiết kế giao diện hiện đại với font Poppins)
.
AI Frameworks: LangChain, LangGraph (Xây dựng ReAct Agent)
.
LLM Provider: Groq (Llama-3.3-70b-versatile)
.
Database: Redis
.
APIs: YouTube Data API v3, ACRCloud
.
Audio Tools: FFmpeg, Silero VAD
.
📂 Cấu trúc dự án
├── agents/             # Quản lý AI Agent, logic suy luận và công cụ (tools) [14, 20]
├── audio_processing/   # Module xử lý âm thanh, STT và nhận diện nhạc [14, 21]
├── backend/            # Cấu hình API, routing và lưu trữ [14, 22]
├── frontend/           # Giao diện người dùng (Web interface) [14, 23]
├── main.py             # Điểm chạy ứng dụng chính [14]
├── requirements.txt    # Danh sách các thư viện phụ thuộc [14]
└── .env.sample         # Tệp mẫu cấu hình biến môi trường [14, 19]
🚀 Cài đặt và sử dụng
Cài đặt môi trường:
Cấu hình biến môi trường: Tạo tệp .env từ .env.sample và điền các API Key cần thiết
:
GROQ_API_KEY
YOUTUBE_API_KEY
ACRCLOUD_ACCESS_KEY, ACRCLOUD_ACCESS_SECRET, ACRCLOUD_REQ_URL
REDIS_URL
Chạy ứng dụng:
Sau đó truy cập giao diện frontend để bắt đầu trò chuyện
.
