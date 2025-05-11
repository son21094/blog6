# 📘 Báo cáo tìm hiểu thư viện: ScyllaDB

## 1. Mục đích của thư viện

**ScyllaDB** là một **Cassandra-compatible NoSQL database** được viết bằng C++. Nó được thiết kế để thay thế Apache Cassandra bằng một hệ thống **hiệu năng cao, độ trễ thấp, và tiết kiệm tài nguyên** hơn, tận dụng tối đa phần cứng hiện đại (đa lõi, NUMA, I/O tốc độ cao).

---

## 2. ScyllaDB giải quyết vấn đề gì?

- **Hiệu năng thấp của Cassandra** do sử dụng JVM: ScyllaDB viết bằng C++ và tránh các vấn đề về garbage collection.
- **Không tận dụng tối đa tài nguyên hệ thống**: Scylla sử dụng kiến trúc *shard-per-core*, mỗi lõi CPU xử lý độc lập.
- **Độ trễ cao trong truy vấn dữ liệu lớn**: Scylla tối ưu độ trễ với reactor model và backpressure.
- **Khó mở rộng quy mô dữ liệu**: Scylla hỗ trợ mở rộng tuyến tính với khả năng xử lý hàng triệu truy vấn mỗi giây.

---

## 3. Điểm mạnh

| Ưu điểm                        | Mô tả                                                                 |
|-------------------------------|------------------------------------------------------------------------|
| 🧠 Hiệu năng cao              | Gấp 10 lần Cassandra trong nhiều trường hợp.                         |
| 💾 Sử dụng C++, không JVM     | Không bị chậm do garbage collector như Cassandra.                    |
| 🔀 Kiến trúc shard-per-core   | Mỗi CPU core hoạt động như một node riêng biệt, tăng song song.     |
| 🕓 Độ trễ cực thấp             | Phù hợp với ứng dụng thời gian thực.                                 |
| 🚀 Tương thích Cassandra      | Dùng schema và query như Cassandra (CQL).                            |
| 📈 Scale tốt                  | Dễ mở rộng lên hàng trăm TB dữ liệu.                                |

---

## 4. Điểm yếu

| Nhược điểm                     | Mô tả                                                                 |
|-------------------------------|------------------------------------------------------------------------|
| 🛠️ Khó cấu hình               | Cần hiểu sâu về hệ thống để tối ưu tốt nhất.                         |
| 📉 Tài nguyên lớn             | Tối ưu cho máy nhiều core, không phù hợp hệ thống nhỏ.               |
| 🔧 Cộng đồng nhỏ hơn Cassandra| Ít tài liệu, diễn đàn thảo luận hơn so với Cassandra.                |

---

## 5. So sánh với các hệ NoSQL khác

| Tiêu chí           | ScyllaDB       | Cassandra      | MongoDB        | Redis          |
|--------------------|----------------|----------------|----------------|----------------|
| Kiểu dữ liệu       | Wide Column     | Wide Column     | Document       | Key-Value      |
| Viết bằng          | C++            | Java           | C++            | C              |
| Độ trễ             | Rất thấp       | Trung bình      | Trung bình     | Rất thấp       |
| Scale horizontal   | Có             | Có             | Có             | Có             |
| GC (Garbage collect)| Không (C++)    | Có (JVM)        | Không          | Không          |
| Use case mạnh      | Time-series, streaming | Logs, IoT   | JSON, Web      | Cache, Realtime|

---

## 6. Ứng dụng thực tế

ScyllaDB phù hợp với các hệ thống:
- **Realtime analytics** (log, clickstream, IoT)
- **Monitoring metrics** (Prometheus, Grafana backend)
- **Time-series databases**
- **E-commerce, Social apps** cần truy cập nhanh, độ trễ thấp
- **Streaming platforms** (Kafka integration)

---

# 📝 Kế hoạch dự kiến bài giữa kỳ

## 1. Bài toán ứng dụng: **Hệ thống quản lý dữ liệu cảm biến (IoT)**

### Mục tiêu:
- Thu thập dữ liệu từ hàng ngàn thiết bị cảm biến theo thời gian thực.
- Lưu trữ hiệu quả và truy vấn nhanh các dữ liệu time-series.

### Tại sao chọn ScyllaDB?
- Hỗ trợ write-heavy load (hàng triệu insert/giây).
- Truy vấn theo thời gian (timestamp) hiệu quả.
- Độ trễ thấp, phù hợp với hệ thống giám sát.
---

