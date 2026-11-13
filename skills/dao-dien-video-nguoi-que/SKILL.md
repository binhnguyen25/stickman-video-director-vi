---
name: dao-dien-video-nguoi-que
description: "Biến chủ đề, yêu cầu, bài viết hoặc kịch bản thành video người que tiếng Việt. Chế độ Đạo diễn tạo storyboard đã duyệt và prompt video từng cảnh để bạn tự tạo clip hoặc render bằng Stickman Studio; Chế độ Tự động làm ra video MP4 hoàn chỉnh có lời dẫn, phụ đề và hiệu ứng âm thanh. Đồng thời hướng dẫn cài đặt, lần dùng đầu tiên và cách bắt đầu của riêng Skill này."
---

# Đạo Diễn Video Người Que

## Hai chế độ, một Skill

Giữ nguyên tên Skill và các lựa chọn đã biết; chỗ nào chưa rõ thì hỏi gọn một lần. Trước khi lên kế hoạch, đọc [ranh giới thực thi của hai chế độ](references/ranh-gioi-che-do.md) (nếu có), rồi đi theo đúng tuyến đã chọn:

- **A · Đạo diễn / A1–A5:** duyệt đề xuất đạo diễn rồi nhận prompt video từng cảnh, mỗi cảnh khoảng 10 giây. A1 là phong cách 1 (nền sáng/tối), A2 là phong cách 2/2A/2B, A3–A5 là phong cách 3–5. Làm theo đúng hợp đồng bên dưới.
- **A6 · Hổ Phách Đêm:** khi chọn phong cách này, đọc [A6](references/bang-phong-cach.md#a6--hổ-phách-đêm) trước khi lên kế hoạch; phong cách này có cách làm riêng, không dùng hợp đồng A1–A5 bên dưới.
- **B · Tự động:** đọc [Chế độ Tự động](#b--tự-động) bên dưới, rồi đọc đúng phong cách B đã chọn trong [bảng phong cách](references/bang-phong-cach.md): B1 Nét Vẽ Tối Giản, B2 Vẽ Tay Nhiều Màu, B3 TV Retro, B4 Giật Gân Sinh Tồn, B5 Giải Thích Nhân Vật, B6 Meme Động. Mỗi phong cách B có hình ảnh, phụ đề, giọng đọc, nhịp độ và âm thanh của riêng nó; không lấy phong cách B1 làm mặc định cho các phong cách khác, không mượn luật của chế độ A sang chế độ B.

Chế độ A và B dùng chung phần cài đặt, không dùng chung hợp đồng sản xuất. Các quy tắc từ **A · Đạo diễn** trở đi chỉ áp dụng cho A1–A5, không áp dụng cho A6 hay bất kỳ phong cách B nào.

Chế độ B nhận chủ đề, yêu cầu, bài viết, bài đăng, tin tức và kịch bản. **Lời dẫn mặc định là tiếng Việt**; nếu người dùng chọn ngôn ngữ/giọng khác thì ưu tiên lựa chọn đó. Không bao giờ tự động đọc lại lời dẫn của đoạn phim đã được duyệt.

Phụ đề: B1–B4 và B6 chỉ một dòng; B5 tối đa ba dòng theo từng ý nghĩa. Áp dụng đúng phông chữ của phong cách đã chọn và kiểm tra chuyển động/phụ đề/âm thanh thật trên file video đã render.

Tất cả phong cách B đều làm được cả **16:9 và 9:16**. Với khổ dọc 9:16, phụ đề phải đọc được trên điện thoại, mỗi cảnh phải có vùng tập trung riêng, hành động chính không được lọt ra ngoài vùng an toàn của màn hình.

## Lần đầu sử dụng

Sau khi cài đặt xong và kiểm tra thấy Skill đã chạy, hoặc khi được gọi lần đầu, hãy giới thiệu ngắn gọn bằng tiếng Việt: nói rõ hai chế độ cho ra sản phẩm gì, hợp làm nội dung nào, cần chuẩn bị gì, các bước làm ra sao, và đưa một câu lệnh mẫu để người dùng copy. Dùng lại các lựa chọn đã biết; không chào lại, không hỏi lại những gì đã chốt. Hướng dẫn bằng tiếng Việt là độc lập với ngôn ngữ lời dẫn trong video: người dùng nói tiếng Việt vẫn có thể yêu cầu video lời dẫn tiếng Anh, và ngược lại.

Sau khi video được duyệt, đọc [bộ làm ảnh bìa](references/bo-thumbnail.md); chỉ gợi ý một lần, không bao giờ chặn việc giao video.

## A · Đạo diễn

### Hợp đồng cốt lõi

Biến một nguồn nội dung thành một đề xuất đạo diễn đã được xác nhận, rồi thành N prompt video độc lập, mỗi prompt cho một clip khoảng 10 giây (N = thời lượng mục tiêu tính bằng giây / 10; mặc định 6 clip cho video 60 giây). Giữ đúng ý nghĩa của nguồn, nhưng sắp xếp lại theo mạch cảm xúc 5 chặng (xem bên dưới) để người xem xem đến cuối.

### Cổng kiểm tra đầu vào

Phải có đủ những thứ này mới được lên kế hoạch:

- nguồn nội dung (chủ đề, bài viết, link hoặc kịch bản)
- khổ hình: `16:9` hoặc `9:16`
- thời lượng mục tiêu: bội số của 10 giây (ví dụ `30 giây`, `60 giây`, `90 giây`, `3 phút`, `5 phút`; mặc định `60 giây` / 6 clip nếu không nói)
- phong cách và tông màu — xem [bảng phong cách](references/bang-phong-cach.md):
  - `Phong cách 1 (Trắng Đen Cổ Điển)`: nền sáng (nền trắng, người que đen) hoặc nền tối (nền đen, người que trắng)
  - `Phong cách 2 (Pop Hiện Đại — nhân vật đội mũ len đỏ)`:
    - `Phong cách 2A (Studio Công Nghệ)`: studio trắng sáng, sàn có lưới phối cảnh xám nhạt, giao diện kính xanh lam/cyan lơ lửng
    - `Phong cách 2B (Điện Ảnh)`: môi trường đủ màu, ánh sáng điện ảnh, có chiều sâu
  - `Phong cách 3 (Hang Động Tiền Sử / Hài Đen)`: đầu trắng có mặt biểu cảm, tay chân que đen, mặc đồ da thú, bối cảnh thời tiền sử
  - `Phong cách 4 (Kể Chuyện Ấm Áp)`: nhân vật tối giản, đầu trắng có mặt, tay chân que đen, trong môi trường hoạt hình 2D đủ màu
  - `Phong cách 5 (Hoạt Hình Lịch Sử)`: đầu trắng, cổ trắng ngắn nối liền, mặt biểu cảm, tay chân que đen, mặc đồ theo thời đại, bối cảnh lịch sử tô màu cel-shading

Nếu thiếu khổ hình hoặc phong cách, hỏi tất cả những thứ còn thiếu trong **một** tin nhắn ngắn rồi dừng lại. Nếu thiếu thời lượng, mặc định 60 giây (6 clip). Nếu người dùng đưa thời lượng không chia hết cho 10, làm tròn về bội số 10 gần nhất. Nếu người dùng chỉ nói nền sáng hoặc nền tối, mặc định phong cách 1. **Không bao giờ tự chọn khổ hình hay phong cách thay người dùng.** Không hỏi lại những lựa chọn đã có.

Gấp gáp, sợ tốn tiền hay câu "cứ chọn bình thường đi" đều không được bỏ qua cổng kiểm tra này.

### Quy trình làm việc

1. Đọc [bảng phong cách](references/bang-phong-cach.md) và [kịch bản mẫu](references/kich-ban-mau.md). Sắp xếp câu chuyện theo **mạch cảm xúc 5 chặng** (Móc Vàng → Phá Vỡ Định Kiến → Vén Màn Bí Mật → Sự Thật Cốt Lõi → Nâng Tầm & Gợi Thảo Luận), co giãn theo thời lượng mục tiêu. Viết **Giai đoạn A** (đề xuất đạo diễn) bằng tiếng Việt, kèm lời dẫn tiếng Việt đầy đủ.
2. Dừng lại sau đề xuất đạo diễn và xin người dùng duyệt rõ ràng.
3. Nếu người dùng đổi khổ hình, thời lượng, phong cách, tông màu, lời dẫn, cấu trúc cảnh hoặc hướng đi chung, viết lại Giai đoạn A và xin duyệt lại.
4. Chỉ sau khi Giai đoạn A hiện tại được duyệt, mới làm **Giai đoạn B** (prompt video từng cảnh).
5. Chỉ dùng [kịch bản mẫu](references/kich-ban-mau.md) khi cần một ví dụ trọn vẹn để giải quyết chỗ còn mơ hồ.

Việc duyệt chủ đề, bị giục làm nhanh, hay duyệt một bản nháp cũ **không** tính là duyệt Giai đoạn A hiện tại.

### Quy tắc đầu ra

- Sắp xếp mọi kịch bản theo mạch 5 chặng:
  1. **Móc Vàng**: câu hỏi ngược đời hoặc hình ảnh nghịch lý khiến người xem tò mò ngay. Video ngắn thì đưa vào 2–5 giây đầu, video dài thì trong 10–15 giây đầu; không bao giờ mở đầu bằng câu xã giao chung chung.
  2. **Phá Vỡ Định Kiến**: nói ra điều ai cũng tưởng là đúng, rồi đập vỡ nó trong một câu để tạo mâu thuẫn trong đầu người xem.
  3. **Vén Màn Bí Mật**: hé lộ cơ chế ẩn, chi tiết ngược đời hoặc trở ngại thật sự.
  4. **Sự Thật Cốt Lõi**: đưa ra logic hoặc tâm lý cốt lõi đằng sau câu chuyện, cho người xem cảm giác "à, ra là vậy".
  5. **Nâng Tầm & Gợi Thảo Luận**: kết lại bằng một câu punchline dễ nhớ và một câu hỏi mở khiến người xem muốn tranh luận ở bình luận.
- Lời dẫn tiếng Việt khoảng **25–30 từ cho mỗi clip 10 giây** (khoảng 150–180 từ cho video 60 giây / 6 clip; khoảng 75–90 từ cho 30 giây / 3 clip; khoảng 450–540 từ cho 3 phút / 18 clip).
- Mỗi clip có ba nhịp timed, ít nhất bốn yếu tố hình ảnh liên quan, và một thay đổi hình ảnh rõ rệt sau mỗi 2–3 giây.
- Giữ tỷ lệ nhân vật, độ dày nét vẽ, phong cách và người dẫn chuyện nhất quán suốt các clip.
- Với phong cách 1, khóa mô tả nhân vật chuẩn sau đây và lặp lại **nguyên văn** trong mọi clip. Giữ đúng hai tay, hai chân; một chi chỉ có một tư thế tại một thời điểm (tay giơ lên thì thay thế tư thế tay cũ, không vẽ thêm tay). Nhân vật giữ một màu; màu nhấn chỉ dùng cho đạo cụ và đồ họa. Không thay mô tả này bằng câu "nhân vật như cũ", không dùng công thức số đo hay hướng dẫn vẽ khung xương.
  - Nền sáng: `Vẽ hoạt hình 2D tối giản bằng nét đen trên nền trắng. Một người que nhất quán: đầu là vòng tròn rỗng, không mặt, không mắt, không miệng, không tóc, không quần áo, thân không tô màu, tỷ lệ ổn định, tay chân là nét liền nhau, độ dày nét đều nhau. Mỗi nhân vật đúng hai tay, hai chân.`
  - Nền tối: như trên nhưng `bằng nét trắng trên nền đen`.
- Với phong cách 1, toàn video tối đa ba màu nhấn bão hòa, gọi tên bằng từ thường (ví dụ: đỏ tươi, xanh điện, vàng ấm). Nền sáng phải là nền trắng phẳng, không vân, không gradient, không bóng đổ, không chiều sâu 3D.
- Với phong cách 2 (nhân vật đội mũ len đỏ), khóa nhân vật:
  - Clip 1: `Một người que hoạt hình 2D tối giản, đội mũ len đỏ tươi (mũ len trơn, không có cục bông), mặc áo thun vàng, tay chân là nét đen đơn giản, mặc quần short. Nét đen đơn giản, màu sắc rực rỡ, phong cách hoạt hình 2D mượt mà.`
  - Clip 2 trở đi: `Vẫn người que hoạt hình 2D tối giản đó, đội mũ len đỏ và mặc áo vàng... Nét đen đơn giản, màu sắc rực rỡ, phong cách hoạt hình 2D mượt mà.`
  - Không vẽ mắt chi tiết, con ngươi hay nét mặt tả thực (dễ bị biến dạng thành mắt lồi). Mũ len phải trơn, không cục bông.
- Với phong cách 2A, môi trường là `studio trắng sáng hiện đại, sàn có đường lưới phối cảnh xám nhạt, ánh sáng studio sáng đều, nhiều khoảng trắng, các khối giao diện kính phát sáng màu cyan và xanh điện`. Luôn thêm câu cấm: `Tuyệt đối tối giản, không vân mạch điện tử, không tấm tường khoa học viễn tưởng, không bê tông nứt, không da người tả thực.`
- Với phong cách 2B, mô tả bối cảnh đủ màu và ánh sáng điện ảnh, nhưng giữ nguyên nhân vật người que 2D đội mũ len đỏ, áo vàng.
- Với mọi phong cách, tránh biến hình chất lỏng/trừu tượng. Dẫn dắt chuyển động bằng hành động cụ thể của nhân vật (nhảy, chạm vào tấm kính, vẽ đường sáng, mở cửa), chia nhịp `[0–3 giây]`, `[3–7 giây]`, `[7–10 giây]`. Không bao giờ để nhân vật đứng yên.
- Với mọi phong cách, chọn một hồ sơ giọng đọc đầy đủ cho cả video ngay ở Giai đoạn A, rồi lặp lại nguyên văn trong mọi clip. Video khác có thể chọn giọng khác; nhưng trong một video, đổi cảnh hay đổi phong cách cũng không được đổi người dẫn chuyện. Giữ nguyên âm sắc, âm vực, giọng vùng miền, kết cấu giọng, cách đọc, tốc độ và chất lượng thu âm; cảm xúc đi lên nhờ hình ảnh và nhạc, không nhờ đổi giọng.
- Lời dẫn chỉ là âm thanh (`chỉ đọc thành tiếng, tuyệt đối không bong bóng thoại, không khung hội thoại`). Trích đúng lời thoại, cấm sửa, lặp lại, thêm phụ đề hay chép lời thoại thành chữ trên hình.
- Không bao giờ ghi mã màu kỹ thuật (hex, RGB, Pantone) trong prompt tạo video.
- Prompt video ở Giai đoạn B gửi cho công cụ AI bên ngoài (Flow, Runway, Kling...) thì viết bằng **tiếng Anh** để công cụ hiểu tốt nhất — dịch mô tả nhân vật, bối cảnh và hành động trong Giai đoạn A sang tiếng Anh khi làm Giai đoạn B. Lời dẫn, phụ đề và mọi trao đổi với người dùng vẫn bằng tiếng Việt. Khi render bằng Stickman Studio thì không cần bước dịch này.
- Mặc định clip tạo ra không có chữ, số hay chữ viết nào trên hình. Chữ phủ thêm (tối đa 2–5 từ) chỉ ghi riêng ở phần ghi chú hậu kỳ.
- Cuối mỗi clip phải nối được với đầu clip sau bằng hành động, đạo cụ quan trọng, hướng di chuyển hoặc một cú cắt đã tính trước. Phong cách 4 được đổi cảnh/dòng thời gian theo ý đồ, nhưng phải nói rõ cái gì giữ nguyên (nhân vật, đạo cụ, hướng đi) và cái gì đổi (địa điểm/thời gian).
- Không bịa số liệu, trích dẫn hay khẳng định không có căn cứ.

### Quy tắc sửa đổi

- `16:9`: dàn cảnh theo trái – giữa – phải; dùng tracking ngang và khoảng trống.
- `9:16`: dùng chiều sâu, chuyển động xếp chồng, mở màn theo chiều dọc, chừa chỗ an toàn cho chữ phủ thêm.

Đổi khổ hình, thời lượng, phong cách hay tông màu đều phải kiểm tra lại cân bằng hình ảnh. Thay đổi toàn cục làm mất hiệu lực của lần duyệt trước.

### Kiểm tra cuối Giai đoạn A

- Đã có đủ nguồn, khổ hình (`16:9` hoặc `9:16`), thời lượng và phong cách/tông màu.
- Kịch bản đi đúng mạch 5 chặng.
- Clip cuối kết bằng câu hỏi gợi tranh luận.
- Lời dẫn khớp thời lượng (khoảng 25–30 từ cho mỗi clip 10 giây).
- Đúng N hàng storyboard, mỗi hàng một nhiệm vụ kể chuyện riêng (N = thời lượng / 10).
- Mỗi hàng có ba nhịp, ít nhất bốn yếu tố hình ảnh, âm thanh và chuyển cảnh.
- Hình ảnh thay đổi sau mỗi 2–3 giây.
- Không quá ba màu nhấn (phong cách 1) hoặc đúng luật bảng màu của phong cách đã chọn.
- Không có mã màu kỹ thuật.
- Mọi chữ đề xuất đều tách riêng làm lớp phủ hậu kỳ, không nằm trong cảnh quay.
- Mỗi cặp cảnh kề nhau đều có điểm nối đã nêu tên.
- Đoạn kết quay về thông điệp chính và lời kêu gọi.
- Không thêm chi tiết sự thật nào không có căn cứ.
- Đã chốt một hồ sơ giọng đọc đầy đủ cho cả video.

## B · Tự động

### Hợp đồng cốt lõi

Đưa một chủ đề, yêu cầu, bài viết hoặc kịch bản vào, nhận về **một file video MP4 hoàn chỉnh**: có lời dẫn tiếng Việt, phụ đề, hình minh họa, chuyển động nhỏ và hiệu ứng âm thanh, đúng thời lượng và khổ hình đã chọn. Người dùng duyệt kịch bản và duyệt bản xem trước khoảng 20 giây có tiếng, rồi mới làm toàn bộ video; không phải tự ghép từng cảnh.

### Quy trình làm việc

1. **Nhận yêu cầu và nguồn.** Chấp nhận chủ đề, yêu cầu, link bài viết/bài đăng/tin tức hoặc kịch bản; người dùng không cần viết sẵn truyện. Nếu link không đọc được, xin nội dung dạng chữ hoặc ảnh chụp màn hình và nói rõ còn thiếu gì. Không bao giờ lấp chỗ trống bằng sự thật bịa ra.
2. **Kiểm tra cấu hình render.** Bản tiếng Việt này render bằng **Stickman Studio** (vẽ người que bằng code rồi ghép thành video MP4 bằng ffmpeg, chạy trên GitHub Actions — xem mục "Điểm khác so với bản gốc" trong README). Trước khi làm, kiểm tra xem repo render có sẵn sàng không; nếu chưa, nói rõ còn thiếu bước nào và ai làm bước đó. Không hứa hẹn giọng đọc AI tự động nếu chưa có dịch vụ đọc tiếng Việt được cấu hình — xem giới hạn ở cuối file.
3. **Duyệt kịch bản.** Trình bày dàn ý/kịch bản ngắn, thiết kế nhân vật, cách làm phụ đề và lựa chọn giọng đọc. Nêu rõ cần duyệt gì trước khi tạo hình ảnh, và còn vướng mắc dịch vụ/chi phí nào.
4. **Bản xem trước khoảng 20 giây có tiếng.** Làm và kiểm tra bản xem trước có lời dẫn, phụ đề, diễn xuất/chuyển động nhỏ và hiệu ứng âm thanh. Đưa link phát được thật, nói rõ đã kiểm tra kỹ thuật những gì, và nhờ người dùng xem/nghe rồi duyệt đúng bản xem trước này. Không coi "render thành công về mặt kỹ thuật" là đã được duyệt. Nếu cần sửa, chỉ sửa đúng chỗ bị chê, giữ lại phần âm thanh/tài sản đã duyệt.
5. **Sản xuất toàn bộ và giao file.** Sau khi bản xem trước được duyệt thật sự, render phần còn lại theo đúng lời dẫn đã duyệt, giữ nguyên tốc độ đọc. Giao file MP4, file phụ đề, và đường dẫn dự án. Nếu còn kiểm tra nào chưa làm, nói thẳng; không gọi một file còn thiếu là "phim hoàn chỉnh". Kết thúc bằng hành động tiếp theo có ích (ví dụ: xem lại phim hoặc yêu cầu sửa một chỗ cụ thể), không tự đăng video hay tự bắt đầu video mới.

### Quy tắc riêng của chế độ B

- Lời dẫn mặc định tiếng Việt. Dùng giọng đọc đã chọn đúng như tên gọi của dịch vụ, không tự thêm mô tả phong cách giọng. Không tự động đọc lại đoạn phim đã duyệt.
- Phụ đề chia theo ý nghĩa và khoảng nghỉ thật của lời nói; mỗi lần chỉ hiện một dòng (B5 tối đa ba dòng). Chia câu dài thành các đơn vị ý nghĩa nối tiếp nhau, không nhồi thành hai dòng, không cắt theo số từ cố định, không thu nhỏ chữ một cách máy móc.
- Mỗi phong cách B có hình ảnh, phụ đề, giọng đọc, nhịp độ và âm thanh riêng; không mượn luật của chế độ A hay phong cách B khác.
- Giữ mỗi cảnh mở đầu/thân/kết tối đa ba giây với phong cách B4 (Giật Gân Sinh Tồn); với các phong cách khác, mỗi cảnh cũng nên đổi hình rõ rệt sau mỗi 2–3 giây, không để một khung hình đứng yên quá lâu.
- Kiểm tra thực tế trên file MP4 đã render: xem hình, đọc chữ phụ đề, nghe âm thanh. Render thành công về mặt kỹ thuật không tính là đạt yêu cầu.

## Quy tắc chung cho cả hai chế độ

- Giữ nguyên tên Skill và mã phong cách (A1, A2, B1...) khi trao đổi; dịch phần giải thích, không dịch mã.
- Ngôn ngữ hướng dẫn (tiếng Việt) độc lập với ngôn ngữ lời dẫn/phụ đề trong video.
- Mỗi lần duyệt chỉ có giá trị cho đúng bản đang duyệt; sửa kịch bản, đổi thiết lập chung hay đổi chi phí thì phải xin duyệt lại.
- Không tự động đăng video lên bất kỳ tài khoản nào; không tự gọi dịch vụ trả phí khi chưa được phép và chưa nói rõ chi phí.
- Khi một việc bị chặn, báo đúng ba dòng: **đã xong gì**, **còn thiếu gì**, **bước tiếp theo là gì** — ngắn gọn, nói rõ ai làm bước đó.

## Giới hạn còn lại của bản tiếng Việt này

- Đây là **Skill + hướng dẫn** (file chữ). Video thực tế vẫn render bằng Stickman Studio (repo riêng), không render trực tiếp trong Skill này.
- **Chưa có giọng đọc AI tiếng Việt tự động trong repo này.** Lời dẫn tiếng Việt trong kịch bản do người dùng tự thu âm, hoặc dùng dịch vụ đọc tiếng Việt (TTS) rồi ghép vào video khi đăng. Bản gốc dùng các dịch vụ giọng đọc tiếng Anh (ví dụ: Gemini, ElevenLabs) — các dịch vụ này có thể không dùng được ở khu vực của người dùng, nên bản Việt không hứa hẹn phần đó.
- **Không cần API tạo video AI trả phí** (Flow/Runway/Kling...) để làm video kiểu Stickman Studio: nhân vật và cảnh được vẽ bằng code rồi ghép MP4 bằng ffmpeg, chạy miễn phí trên GitHub Actions.
- Muốn tạo clip bằng công cụ AI bên ngoài (chế độ A, Giai đoạn B) thì vẫn cần tài khoản của công cụ đó; Skill chỉ viết prompt, không tạo clip thay.
