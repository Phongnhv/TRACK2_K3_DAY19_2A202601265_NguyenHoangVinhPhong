# Reflection — Lab 19

Tên: Nguyen Hoang Vinh Phong
Cohort: A20 · Track 2
Path: lite

Trên golden set, BM25 mạnh nhất ở `exact` vì query chứa trực tiếp thuật ngữ
trong corpus. Vector phù hợp hơn với `paraphrase` khi model hiểu được ngữ
nghĩa. `mixed` là nơi hybrid thắng rõ nhất vì kết hợp tín hiệu từ khóa và
ngữ nghĩa. Kết quả đo được: keyword 77,8%, semantic 73,2%, hybrid 78,6%;
hybrid đạt 100% trên slice `mixed`.

Tôi không dùng hybrid khi query là exact và cần tốc độ, độ đơn giản hoặc khả
năng giải thích của BM25. Pure vector cũng hợp lý khi dữ liệu và truy vấn
chủ yếu giàu ngữ nghĩa, không có thuật ngữ ổn định. Hybrid không đáng dùng
nếu chi phí embedding hoặc latency nghiêm ngặt hơn lợi ích chất lượng.

Điểm bất ngờ: model embedding tiếng Anh vẫn tìm đúng một số paraphrase tiếng
Việt, nhưng semantic giảm rõ so với mixed query.

Bonus: chưa làm. Pair work: không có.
