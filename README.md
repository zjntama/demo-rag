# Build a rag app using ollama and langchain
Ứng dụng RAG (Retrieval-Augmented Generation) để trả lời câu hỏi sử dụng LangChain và Ollama.

## Cài đặt

1. **Tạo virtual environment:**
```bash
python3 -m venv .venv
source .venv/bin/activate  # macOS/Linux
# hoặc
.venv\Scripts\activate  # Windows
```

2. **Cài đặt dependencies:**
```bash
pip install -r requirements.txt
```

3. **Cài đặt Ollama (nếu chưa có):**
```bash
# macOS
curl -fsSL https://ollama.ai/install.sh | sh

# Hoặc tải từ: https://ollama.ai/download
```

4. **Tải model Llama3:**
```bash
ollama pull llama3
```

## Sử dụng

1. **Chuẩn bị dữ liệu:**
   - Đặt file PDF "SQL Server 2012 T-SQL Recipes.pdf" vào thư mục `data/`

2. **Chạy ứng dụng:**
```bash
python app.py
```

## Cấu trúc dự án

```
rag-app/
├── app.py              # File chính của ứng dụng
├── requirements.txt    # Dependencies
├── data/              # Thư mục chứa file PDF
├── sql_chroma_db/     # Vector database (tự động tạo)
└── README.md          # Hướng dẫn này
```

## Tính năng

- **Ingest**: Tải và xử lý file PDF thành chunks
- **Vector Store**: Lưu trữ embeddings trong ChromaDB
- **RAG Chain**: Kết hợp retrieval và generation
- **Question Answering**: Trả lời câu hỏi dựa trên context

## Lưu ý

- Đảm bảo Ollama đang chạy trước khi sử dụng ứng dụng
- File PDF cần được đặt trong thư mục `data/`
- Vector store sẽ được tạo tự động khi chạy lần đầu 

# Tutorial 
https://www.youtube.com/watch?v=Ii4ouKEUgz4