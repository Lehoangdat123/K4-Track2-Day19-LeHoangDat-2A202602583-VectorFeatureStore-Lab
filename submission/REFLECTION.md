# Reflection — Lab 19

**Tên:** Lê Hoàng Đạt
**Cohort:** A20-K4
**Path đã chạy:** lite

---

## Câu hỏi (≤ 200 chữ)

Trên golden set, BM25 thắng ở `exact` (96,7%, bằng hybrid); vector chỉ đạt 24,0% ở
`paraphrase`, thấp hơn BM25 (33,3%) và hybrid (32,0%) — model bge-small tiếng Anh
yếu với câu hỏi diễn đạt lại bằng tiếng Việt. Ở `mixed`, hybrid đứng đầu (100%).
Trung bình, hybrid đạt 78,6%, nhỉnh hơn BM25 77,8% và vector 73,2%. Tôi sẽ chọn
BM25 khi truy vấn chứa đúng thuật ngữ và cần cách truy hồi đơn giản; chỉ dùng
vector riêng khi embedding đa ngôn ngữ đã được đánh giá tốt trên truy vấn thực.
Hybrid phù hợp khi loại truy vấn hỗn hợp và mức cải thiện đo được xứng với chi phí.

---

Quan sát: paraphrase mẫu ở NB1 vẫn tìm đúng cụm `cloud`, nhưng trên golden set
vector-only yếu hơn BM25. Một ví dụ thành công không thay thế được đánh giá tổng hợp.
