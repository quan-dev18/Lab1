# BÁO CÁO LAB 1: TRẢI NGHIỆM DEVOPS WORKFLOW END-TO-END

**Họ và tên:** QuanDev-thaiNG  
**Email:** quandev18@gmail.com  
**Khóa học:** Vận hành & Bảo trì Phần mềm (DevOps)  

---

## 1. Bảng So Sánh DevOps vs Truyền Thống (Traditional)

| Tiêu chí | Cách THỦ CÔNG (Traditional) | Cách DEVOPS (CI/CD Pipeline) |
|---|---|---|
| **Làm sao để deploy?** | Copy/FTP/SSH thủ công file lên hosting hoặc server | Push code lên GitHub (`git push`), pipeline tự động chạy |
| **Mất bao lâu?** | 15 - 30 phút hoặc lâu hơn | ~10 - 30 giây |
| **Ai làm deploy?** | Kỹ sư vận hành (Sysadmin/DevOps engineer) làm bằng tay | GitHub Actions (máy/hệ thống tự động thực hiện) |
| **Có bị sai sót không?** | Dễ sai sót do thao tác con người (quên file, nhầm môi trường) | Không — quy trình chuẩn hóa và nhất quán 100% |
| **Rollback nếu lỗi?** | Tìm file backup cũ, upload lại đè lên (rất rủi ro và chậm) | `git revert <commit>` và push → pipeline tự động deploy bản cũ |
| **Làm sao biết deploy thành công?** | Tự kiểm tra bằng tay, dễ bỏ sót lỗi | GitHub Actions gửi thông báo trạng thái trực quan (✅ / ❌) |

---

## 2. Trả lời câu hỏi thu hoạch

1. **DevOps workflow tự động hóa những bước nào mà cách thủ công phải làm bằng tay?**  
   - Trả lời: Tự động hóa các bước kiểm tra mã nguồn (Checkout, Validate/Lint HTML), đóng gói (Build) và phát hành lên môi trường chạy thực tế (Deploy lên GitHub Pages). Toàn bộ quy trình diễn ra tự động mà không cần can thiệp thủ công.

2. **Nếu bạn deploy sai (website bị lỗi), làm sao để quay lại phiên bản cũ?**  
   - Trả lời: Sử dụng lệnh `git revert <commit_id>` để hoàn tác thay đổi rồi push lại lên GitHub, hoặc chuyển về commit ổn định trước đó. CI/CD pipeline sẽ ngay lập tức kích hoạt và tự động deploy lại phiên bản chuẩn xác.

3. **GitHub Actions pipeline đã giúp bạn tiết kiệm bao nhiêu thời gian so với cách thủ công?**  
   - Trả lời: Tiết kiệm rất nhiều thời gian. Với cách thủ công phải mất 15–30 phút cho mỗi lần đóng gói và tải tệp tin lên máy chủ, trong khi với GitHub Actions chỉ mất khoảng 10–30 giây từ lúc `git push` đến khi website cập nhật trực tiếp.
