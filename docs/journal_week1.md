# Nhật ký tuần 1: khám phá và lọc dữ liệu tuyển dụng IT

## Việc đã làm
- Khám phá Vietnam Jobs Dataset (Kaggle): 85.478 dòng, 11 cột.
- Xây bộ lọc tin IT, đo chất lượng bằng nhãn tay.
- Khử trùng lặp, trích xuất kỹ năng bằng từ điển.

## Phát hiện về dữ liệu
- Không có cột mô tả công việc và ngày đăng, nên chỉ làm được text-to-SQL;
  RAG và câu hỏi theo thời gian cần dữ liệu crawl.
- Nhãn ngành `job_fields` do người đăng tự chọn, rất nhiễu (nhiều tin chọn 5-8 nhãn).
  Tin chỉ dựa vào nhãn IT: precision khoảng 42% (mẫu 40 dòng).
- Lọc theo từ khóa tiêu đề cũng sai (ví dụ "data" bắt nhầm telesales).
- Có khoảng một nửa tin trùng (2.061 -> 1.016).

## Quy tắc lọc cuối cùng
- Tiêu đề có từ khóa IT mạnh, hoặc có nhãn IT cộng tín hiệu yếu trong tiêu đề,
  trừ khi dính từ khóa loại trừ.
- Gắn độ tin cậy `high` / `medium`.
- Precision nhóm `medium` đo được khoảng 78% (mẫu 40 dòng, sai số lớn).

## Quy tắc gắn nhãn tay
- Dựa vào tiêu đề, không dựa vào `job_fields`.
- Sửa máy tính/laptop = 1, sửa máy in/camera = 0, không chắc = 0.
- Ca biên: BrSE, xử lý dữ liệu, compliance and security.

## Điều mình học được
- (ghi bằng lời của bạn: bước nào khó, bước nào thích, điều gì bất ngờ)

## Việc cần làm tiếp
- Làm sạch `experience`, `salary`, thiết kế schema, nạp vào DuckDB.
- Khảo sát nguồn crawl (ITviec, TopCV).