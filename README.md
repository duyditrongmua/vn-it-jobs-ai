# vn-it-jobs-ai

Data Engineering & AI/RAG pipeline analyzing the Vietnam IT job market.

## Mục tiêu
Xây pipeline từ thu thập dữ liệu tuyển dụng IT đến trợ lý AI hỏi đáp
(text-to-SQL cho câu hỏi thống kê, RAG cho câu hỏi ngữ nghĩa).

## Tiến độ
- [x] Khám phá dữ liệu Kaggle (Vietnam Jobs Dataset)
- [ ] Làm sạch và chuẩn hóa dữ liệu
- [ ] Crawl dữ liệu IT mới
- [ ] Nạp vào PostgreSQL/DuckDB
- [ ] Text-to-SQL, RAG
- [ ] Đánh giá chất lượng

## Dữ liệu
Dùng Vietnam Jobs Dataset trên Kaggle (dán link vào đây). Dữ liệu gốc
không được đưa vào repo, chỉ có file mẫu ở `data/sample/`.
Tải `jobs.csv` và đặt vào `data/raw/` để chạy lại notebook.

## Cách chạy
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
