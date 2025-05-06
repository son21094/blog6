---
title: "Blog"
date: "2025-29-28"
updated: "2023-04-28"
categories:
  - "sveltekit"
  - "markdown"
  - "svelte"
coverImage: "/images/jerry-zhang-ePpaQC2c1xA-unsplash.jpg"
coverWidth: 16
coverHeight: 9
excerpt: This post demonstrates how to include a Svelte component in a Markdown post.
---

# BÁO CÁO TÌM HIỂU – HỆ THỐNG PHÂN TÁN, ĐA TIẾN TRÌNH, ĐA LUỒNG

## **1. Kiểm tra CPU, GPU, RAM và phân tích hiệu năng máy tính**

### ✅ Cách kiểm tra (Windows):
- Nhấn `Ctrl + Shift + Esc` để mở **Task Manager**
- Chọn tab **Performance** để xem:
  - **CPU**: Tên, số lõi (cores), số luồng (threads)
  - **RAM**: Tổng dung lượng, tốc độ
  - **GPU**: Tên card đồ họa, VRAM

### ✍️ Ví dụ báo cáo:
- **CPU**: Intel Core i5-1235U (10 cores, 12 threads) → Đủ để lập trình, học máy nhẹ, không phù hợp render hay train AI nặng.
- **RAM**: 8GB DDR4 @ 3200MHz → Đáp ứng lập trình, mở trình duyệt, chạy máy ảo cơ bản.
- **GPU**: Intel Iris Xe → GPU tích hợp, không chuyên cho AI, đồ họa.
- **Tổng kết hiệu năng**: Phù hợp sinh viên CNTT, học tập, lập trình web, mobile. Không phù hợp deep learning hay thiết kế 3D.

---

## **2. 12 Bài toán phổ biến trong CNTT sử dụng đa luồng / đa tiến trình**

| STT | Bài toán CNTT phổ biến           | Đa luồng / Đa tiến trình dùng ở đâu              |
|-----|----------------------------------|--------------------------------------------------|
| 1   | Web server (Node.js, Apache)     | Mỗi request xử lý ở thread hoặc worker riêng     |
| 2   | Xử lý ảnh hàng loạt              | Mỗi ảnh xử lý ở process/thread riêng             |
| 3   | Dò mật khẩu brute-force          | Nhiều thread thử mật khẩu cùng lúc               |
| 4   | Tìm kiếm dữ liệu lớn             | Thread chia nhỏ tập dữ liệu để xử lý song song   |
| 5   | Chat server                      | Mỗi kết nối client dùng thread riêng             |
| 6   | Game engine (Unity)              | Physics, AI, rendering chạy ở nhiều thread       |
| 7   | Render video                     | Mỗi đoạn video = 1 tiến trình xử lý              |
| 8   | Huấn luyện mô hình AI            | GPU xử lý đa luồng, mỗi batch dữ liệu song song  |
| 9   | Trình duyệt web (Chrome)         | Mỗi tab = 1 process, script = 1 thread           |
| 10  | IDE (VSCode, IntelliJ)           | UI, biên dịch, kiểm lỗi hoạt động song song      |
| 11  | Web crawler                      | Mỗi URL được crawl ở 1 thread riêng              |
| 12  | Mô phỏng IoT                     | Mỗi thiết bị ảo dùng 1 tiến trình hoặc thread     |

---

## **3. Bảng phân biệt dùng Thread / Process**

| Tiêu chí              | Dùng Thread khi                              | Dùng Process khi                                | Dùng cả hai khi                                      |
|-----------------------|-----------------------------------------------|--------------------------------------------------|-------------------------------------------------------|
| Bộ nhớ chia sẻ        | Cần chia sẻ dữ liệu dễ dàng                   | Không cần chia sẻ, muốn cô lập                   | Vừa chia sẻ nhanh, vừa cô lập xử lý riêng             |
| Hiệu năng             | Ít overhead, nhanh                           | Ổn định hơn, không ảnh hưởng lẫn nhau           | Tối ưu hóa cả hiệu năng và độ tin cậy                |
| Lỗi / crash           | Thread lỗi → ảnh hưởng chương trình chính    | Process crash → không ảnh hưởng chương trình chính | Muốn kết hợp an toàn và hiệu suất cao                |
| Ví dụ bài toán        | Web server, xử lý tập tin                     | Huấn luyện AI, xử lý ảnh                         | Microservice gọi AI (mỗi service = process, nhiều thread trong service) |

---

## **4. ChatGPT training bằng distributed system**

### ✅ Tóm tắt cách hoạt động:
- **GPT-4** được huấn luyện với **hàng tỷ tham số**, yêu cầu chia nhỏ mô hình và dữ liệu.
- Sử dụng hệ thống phân tán với **nghìn GPU** chạy song song.
- **Chiến lược chính**:
  - **Data Parallelism**: Chia batch dữ liệu cho các GPU xử lý cùng mô hình.
  - **Model Parallelism**: Chia mô hình ra nhiều phần trên các GPU.
  - **Pipeline Parallelism**: Xử lý theo luồng pipeline qua nhiều GPU.
- Dùng thư viện như: **DeepSpeed**, **Megatron-LM**, **PyTorch Distributed**.
- Hạ tầng: **GPU A100 / H100** chạy trên Microsoft Azure.

### ✅ Tài liệu tham khảo:
- [GPT-4 Technical Report](https://openai.com/research/gpt-4)
- [Microsoft đầu tư vào OpenAI (2023)](https://news.microsoft.com/2023/01/23/microsoft-announces-multiyear-multibillion-dollar-investment-in-openai/)
- [DeepSpeed (Microsoft)](https://www.deepspeed.ai/)
- [Model Parallelism Explained](https://sebastianraschka.com/blog/2021/model-parallelism.html)

---
