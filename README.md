# 🎬 Đạo Diễn Video Người Que — Bản Tiếng Việt

**Biến bất kỳ kịch bản nào thành video người que nhiều phong cách, có lời dẫn, phụ đề và hiệu ứng âm thanh — cho kênh YouTube, TikTok, Facebook Reels không cần lộ mặt.**

Đưa vào một chủ đề, một bài viết hay một kịch bản. Nhận về video người que hoàn chỉnh, sẵn sàng đăng. **Miễn phí & mã nguồn mở. Không cần máy quay, không cần gói thuê bao hàng tháng, làm xong trong vài phút chứ không phải vài ngày.**

> Dựa trên [kaomei/stickman-video-director](https://github.com/kaomei/stickman-video-director) (MIT, 6.000 sao) — đã Việt hóa toàn bộ và điều chỉnh để người Việt dùng được ngay, kể cả khi không có tài khoản dịch vụ AI trả phí.

## 🎬 Hai cách làm video

**Muốn kiểm soát từng cảnh? Chọn A · Chế độ Đạo diễn. Muốn đưa chủ đề vào là nhận video xong? Chọn B · Chế độ Tự động.** Một Skill, hai quy trình.

|  | A · Chế độ Đạo diễn | B · Chế độ Tự động |
|---|---|---|
| **Cách làm** | Bạn kiểm soát quá trình làm phim; AI lên kế hoạch từng cảnh. Nhận storyboard và prompt, rồi tạo clip và tự ghép. | Đưa chủ đề hoặc brief vào; nhận video hoàn chỉnh. Tự động làm hình minh họa, lời dẫn, phụ đề, chuyển động nhỏ và ghép video. |
| **Độ dài** | **Ngắn trước**, thường 30 giây–3 phút. Video dài hơn thì làm từng cảnh rồi ghép. | **Dài trước**, đặc biệt là video có lời dẫn từ 10 phút trở lên. Cũng làm được video ngắn và truyện nhiều tập. |
| **Công cụ** | Lên kế hoạch với trợ lý AI, tạo clip bằng công cụ tạo video (Google Flow, Runway, Luma, Kling...) hoặc render bằng Stickman Studio, rồi ghép trong CapCut hoặc Premiere. | Chạy trong môi trường AI có quyền đọc/ghi file và chạy lệnh (như Muse, Claude Code, Codex), dùng Stickman Studio để render và giao file. |
| **Hình ảnh** | **Clip chuyển động đã tạo sẵn**, có chuyển động nhân vật, hướng máy quay và tương tác. | **Cảnh minh họa với chuyển động nhỏ**: biểu cảm, phản ứng nhân vật và chuyển động đạo cụ đi cùng lời dẫn, kèm cắt cảnh, lia máy và zoom. |
| **Sản phẩm** | Đề xuất đạo diễn, storyboard, prompt video từng cảnh và thiết kế âm thanh. | **Một file video hoàn chỉnh có lời dẫn, phụ đề và chuyển động nhỏ.** |

Cả hai chế độ đều bắt đầu từ chủ đề thô, link bài viết hay kịch bản đầy đủ. Tự chọn khổ hình (9:16, 16:9, 1:1) và ngôn ngữ lời dẫn. Độ dài trên đây là gợi ý, không phải giới hạn cứng.

## 🎨 Bảng phong cách

| Mã | Phong cách | Hợp làm video gì |
|---|---|---|
| **A1** | Trắng Đen Cổ Điển | Giải thích kiến thức, logic, mô hình tư duy |
| **A2** | Pop Hiện Đại (2A Studio Công Nghệ / 2B Điện Ảnh) | Hướng dẫn công nghệ, mẹo công việc, truyện truyền cảm hứng |
| **A3** | Hang Động Tiền Sử | Truyện châm biếm, ẩn dụ bằng hình ảnh, cái kết bất ngờ |
| **A4** | Kể Chuyện Ấm Áp | Chuyện đời thường, trưởng thành, kể chuyện giáo dục |
| **A5** | Hoạt Hình Lịch Sử | Giải thích lịch sử, đời sống xưa, chuyện hài lịch sử |
| **A6** | Hổ Phách Đêm | Chuyện đêm khuya, tâm sự, không khí điện ảnh |
| **B1** | Nét Vẽ Tối Giản | Giải thích khoa học, tâm lý, video kiến thức dài |
| **B2** | Vẽ Tay Nhiều Màu | Chuyện kể trước khi ngủ, chủ đề cảm xúc |
| **B3** | TV Retro | Truyện bí ẩn, giả tưởng, "TV lúc 3 giờ sáng" |
| **B4** | Giật Gân Sinh Tồn | Truyện sinh tồn, kịch tính, hồi hộp |
| **B5** | Giải Thích Nhân Vật | Giải thích khái niệm, video "tại sao nên..." |
| **B6** | Meme Động | Video hài, meme, kể chuyện nhanh cho TikTok/Reels |

Mô tả chi tiết từng phong cách: xem [bảng phong cách](skills/dao-dien-video-nguoi-que/references/bang-phong-cach.md).

## 🧭 Bắt đầu

Cài Skill này cho trợ lý AI của bạn, rồi nhắn:

```text
Cài Skill này giúp mình:
https://github.com/binhnguyen25/stickman-video-director-vi
Sau khi cài xong, đọc ngay file SKILL.md đã cài.
Giải thích bằng tiếng Việt: mỗi chế độ cho ra sản phẩm gì, cần công cụ gì,
quy trình làm ra sao, kèm ví dụ mình copy được.
Dựa vào thứ mình muốn làm, cho mình biết còn thiếu gì và phải làm gì tiếp.
```

### A · Chế độ Đạo diễn: prompt video từng cảnh

```text
Dùng Chế độ Đạo diễn / chế độ A để biến chủ đề, nội dung hoặc brief sau
thành video người que:
[Nhập chủ đề, dán nội dung, hoặc mô tả nhu cầu]
Yêu cầu: dọc 9:16, phong cách A1 nền tối, làm 60 giây trước.
Cho mình đề xuất đạo diễn trước. Sau khi mình duyệt, mới đưa prompt video từng cảnh.
```

**Quy trình:** đưa chủ đề và brief → làm đề xuất đạo diễn → bạn duyệt → (tùy chọn) duyệt ảnh nhân vật ba góc → nhận prompt video từng cảnh → tạo clip và ghép video.

### B · Chế độ Tự động: từ brief đến video dài

```text
Dùng Chế độ Tự động / chế độ B để biến chủ đề, bài viết, bài đăng, tin tức hoặc brief sau
thành video YouTube hấp dẫn:
[Dán nội dung, link, hoặc mô tả thứ muốn quảng bá]
Yêu cầu: 5–10 phút, ngang 16:9, phong cách B1 "Nét Vẽ Tối Giản", lời dẫn tiếng Việt,
có phụ đề và hiệu ứng âm thanh.
Kiểm tra cấu hình tạo hình, giọng đọc và render video trước. Rồi đưa kịch bản
và bản xem trước 20 giây có tiếng cho mình duyệt.
Sau khi mình duyệt, làm video đầy đủ theo đúng lời dẫn. Giao file video hoàn chỉnh;
mình không muốn tự ghép từng cảnh.
```

**Quy trình:** đưa chủ đề/nội dung/brief → duyệt kịch bản → duyệt bản xem trước 20 giây có tiếng → tự động sản xuất video đầy đủ → nhận file video hoàn chỉnh.

### Xem trước truyện mẫu

Repo này kèm sẵn storyboard mẫu [Trận Bóng Người Que](skills/dao-dien-video-nguoi-que/references/kich-ban-mau.md) — 7 cảnh, 20,5 giây, hai nhân vật An (đỏ) và Bình (xanh) đá bóng, sút và ghi bàn rồi bắt tay nhau. Truyện này đã render thành video MP4 thật trong Stickman Studio, xem để biết storyboard chuẩn trông như thế nào.

**Hoàn thiện tùy chọn cho cả hai chế độ:** sau khi bạn xác nhận video cuối cùng đã ưng ý, có thể làm tiếp ảnh bìa, tiêu đề, mô tả và bình luận ghim theo đúng phong cách của video — xem [bộ làm ảnh bìa](skills/dao-dien-video-nguoi-que/references/bo-thumbnail.md).

## ❓ Câu hỏi thường gặp

**Hỏi 1. Có thật sự miễn phí không? Có phí ẩn không?**
Skill này miễn phí, mã nguồn mở (MIT). Render bằng Stickman Studio dùng GitHub Actions miễn phí, không cần mua API tạo video AI. Chỉ khi bạn tự chọn dùng công cụ tạo video AI bên ngoài (Flow, Runway, Kling...) thì mới tốn phí của công cụ đó.

**Hỏi 2. Làm sao giữ nhân vật nhất quán qua các cảnh?**
Mỗi phong cách có một "mô tả nhân vật chuẩn" đã khóa (ví dụ: mũ len đỏ, áo vàng) và được lặp nguyên văn trong mọi prompt. Với phong cách A5 Hoạt Hình Lịch Sử, nên chuẩn bị ảnh nhân vật ba góc (chính diện, nghiêng, sau lưng) trước. Lưu ý: mô tả bằng chữ giúp ích nhiều nhưng không đảm bảo 100% — luôn kiểm tra clip thực tế.

**Hỏi 3. Cần công cụ gì? Có cần biết lập trình hay máy tính mạnh không?**
Chế độ A chỉ cần nhắn tin với trợ lý AI; tạo clip và ghép video thì dùng công cụ bạn đã quen (CapCut, Premiere, hoặc Stickman Studio). Chế độ B cần môi trường AI có quyền đọc/ghi file và chạy lệnh. Không cần GPU đắt tiền.

**Hỏi 4. Làm video được khi chưa có kịch bản không?**
Được. Chỉ cần đưa chủ đề, bài viết hoặc link — Skill sẽ viết kịch bản, bạn duyệt rồi mới làm tiếp.

**Hỏi 5. Video làm ra có đăng YouTube/TikTok/Facebook kiếm tiền được không?**
Video do bạn làm ra thuộc về bạn. Việc bật kiếm tiền còn tùy chính sách từng nền tảng và bản quyền nhạc/hình bạn dùng — Skill không chứng nhận điều này.

**Hỏi 6. Giọng đọc tiếng Việt lấy ở đâu?**
Lời dẫn tiếng Việt trong kịch bản do bạn tự thu âm, hoặc dùng dịch vụ đọc tiếng Việt (TTS) rồi ghép vào video khi đăng. Repo này chưa tích hợp sẵn giọng đọc AI tiếng Việt tự động.

## 🔄 Điểm khác so với bản gốc

|  | Bản gốc (kaomei/stickman-video-director) | Bản tiếng Việt này |
|---|---|---|
| Ngôn ngữ | Tiếng Anh (+ bản dịch Trung, Nhật, Hàn...) | **Tiếng Việt toàn bộ**: hướng dẫn, kịch bản, lời dẫn, ví dụ |
| Lời dẫn mặc định | Tiếng Anh | **Tiếng Việt** |
| Cách tạo hình ảnh | Dùng API tạo ảnh/video AI (Gemini, Flow...) | **Render nội bộ bằng Stickman Studio**: vẽ người que bằng code, ghép MP4 bằng ffmpeg, chạy trên GitHub Actions — không cần API trả phí |
| Giọng đọc | Dịch vụ giọng đọc tiếng Anh (Gemini, ElevenLabs...) | **Chưa tích hợp sẵn** giọng đọc AI tiếng Việt — tự thu âm hoặc dùng TTS rồi ghép khi đăng |
| Kịch bản mẫu | Ví dụ tiếng Trung/Anh ("đừng để suy nghĩ quá nhiều hủy hoại bạn") | **Truyện "Trận Bóng Người Que"** — truyện mẫu đã render thật trong Stickman Studio |
| Phong cách | 12 phong cách, tên tiếng Anh/Trung | 12 phong cách, **tên tiếng Việt** |

## 📁 Cấu trúc repo

```text
stickman-video-director-vi/
├── README.md                                   # File này
├── LICENSE                                     # MIT
└── skills/dao-dien-video-nguoi-que/
    ├── SKILL.md                                # Skill chính (tiếng Việt)
    └── references/
        ├── bang-phong-cach.md                  # 12 phong cách, mô tả chi tiết
        ├── kich-ban-mau.md                     # Storyboard mẫu: Trận Bóng Người Que
        ├── bo-thumbnail.md                     # Ảnh bìa + bộ đăng bài
        └── ranh-gioi-che-do.md                 # Ranh giới thực thi của chế độ A/B
```

## 📄 Giấy phép

MIT — xem [LICENSE](LICENSE). Dựa trên [kaomei/stickman-video-director](https://github.com/kaomei/stickman-video-director) (MIT) của kaomei, đã Việt hóa và điều chỉnh cho người dùng Việt Nam.
