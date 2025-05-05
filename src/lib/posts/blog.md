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

# Hệ thống phân tán là gì?

Hệ thống phân tán là một hệ thống bao gồm nhiều máy tính hoặc nút (nodes), được kết nối với nhau và làm việc đồng thời để hoàn thành các tác vụ, chia sẻ dữ liệu và cung cấp dịch vụ. Các máy tính này có thể nằm ở các vị trí địa lý khác nhau, nhưng chúng phối hợp với nhau như thể chúng hoạt động như một hệ thống duy nhất.

Mục tiêu của hệ thống phân tán là cung cấp khả năng mở rộng, độ tin cậy cao, và hiệu suất tốt hơn so với hệ thống đơn lẻ. Hệ thống phân tán có thể được áp dụng trong nhiều lĩnh vực khác nhau, bao gồm điện toán đám mây, mạng lưới, và các ứng dụng internet.

# Các ứng dụng của hệ thống phân tán

Hệ thống phân tán được sử dụng rộng rãi trong các ứng dụng cần khả năng mở rộng và độ tin cậy cao, chẳng hạn như:

- **Điện toán đám mây**: Amazon Web Services (AWS), Google Cloud, và Microsoft Azure đều là các ví dụ điển hình về các nền tảng điện toán đám mây phân tán, cho phép người dùng thuê tài nguyên tính toán từ nhiều máy chủ khác nhau.
- **Cơ sở dữ liệu phân tán**: Các hệ thống cơ sở dữ liệu như Cassandra, MongoDB, và Amazon DynamoDB sử dụng các kỹ thuật phân tán để đảm bảo rằng dữ liệu luôn sẵn sàng và có thể mở rộng linh hoạt.
- **Mạng P2P**: Mạng chia sẻ file như BitTorrent sử dụng các hệ thống phân tán để chia sẻ dữ liệu giữa các nút trên mạng.
- **Các hệ thống web và ứng dụng di động**: Các ứng dụng như Facebook, Twitter và WhatsApp sử dụng các hệ thống phân tán để xử lý lượng lớn người dùng và dữ liệu.

# Các khái niệm chính của hệ thống phân tán

Dưới đây là một số thuật ngữ quan trọng trong hệ thống phân tán:

## Scalability (Khả năng mở rộng)

Scalability là khả năng của hệ thống để tăng cường tài nguyên (ví dụ như máy chủ, bộ nhớ, băng thông) mà không làm giảm hiệu suất. Có hai loại scalability:

- **Vertical Scaling**: Tăng tài nguyên của một máy tính (ví dụ: thêm CPU, RAM).
- **Horizontal Scaling**: Tăng số lượng máy tính (thêm các máy chủ).

## Fault Tolerance (Khả năng chịu lỗi)

Fault tolerance là khả năng của hệ thống để duy trì hoạt động bình thường ngay cả khi một số thành phần trong hệ thống gặp sự cố hoặc lỗi. Điều này đạt được thông qua việc sao lưu, nhân bản dữ liệu và phân tán nhiệm vụ.

## Availability (Tính khả dụng)

Availability là mức độ mà hệ thống có thể hoạt động và cung cấp dịch vụ khi người dùng yêu cầu. Hệ thống phân tán phải đảm bảo tính khả dụng cao, ngay cả khi một số máy chủ hoặc nút không hoạt động.

## Transparency (Tính minh bạch)

Transparency trong hệ thống phân tán đề cập đến việc hệ thống che giấu sự phức tạp của việc phân tán cho người dùng và lập trình viên. Ví dụ, người dùng không cần biết dữ liệu được lưu trữ ở đâu hoặc xử lý ra sao.

## Concurrency (Đồng thời)

Concurrency là khả năng của hệ thống để thực thi nhiều nhiệm vụ hoặc yêu cầu một cách đồng thời. Điều này có thể giúp tăng hiệu suất và giảm thời gian xử lý.

## Parallelism (Xử lý song song)

Parallelism là việc thực hiện nhiều tác vụ cùng lúc trên các nút khác nhau trong hệ thống phân tán. Điều này thường liên quan đến việc chia nhỏ công việc và xử lý chúng song song trên các nút khác nhau.

## Openness (Tính mở)

Openness là khả năng của hệ thống phân tán để tích hợp và tương tác với các hệ thống khác một cách dễ dàng. Điều này thường đạt được thông qua các chuẩn giao thức mở.

## Vertical Scaling (Tăng cường chiều dọc)

Vertical scaling, hay còn gọi là scaling up, là việc thêm tài nguyên vào một nút duy nhất trong hệ thống, chẳng hạn như tăng dung lượng bộ nhớ hoặc CPU.

## Horizontal Scaling (Tăng cường chiều ngang)

Horizontal scaling, hay còn gọi là scaling out, là việc thêm nhiều nút (máy chủ) vào hệ thống để mở rộng năng lực của nó.

## Load Balancer (Cân bằng tải)

Load balancer là phần mềm hoặc phần cứng giúp phân phối tải công việc hoặc yêu cầu vào các máy chủ hoặc nút khác nhau trong hệ thống phân tán, nhằm đảm bảo hiệu suất tối ưu.

## Replication (Nhân bản)

Replication là quá trình sao chép dữ liệu từ một nút này sang nút khác để đảm bảo tính sẵn sàng và khả năng chịu lỗi của hệ thống. Nếu một nút gặp sự cố, dữ liệu có thể được truy cập từ các bản sao khác.

### Ví dụ và giải thích cách các thuật ngữ này liên quan đến ví dụ

Giả sử chúng ta có một ứng dụng web chạy trên một hệ thống phân tán với nhiều máy chủ. Để đảm bảo khả năng mở rộng, hệ thống sử dụng **horizontal scaling** bằng cách thêm nhiều máy chủ vào cụm (cluster). **Load balancer** sẽ phân phối các yêu cầu người dùng giữa các máy chủ này để tránh tình trạng quá tải. Dữ liệu của người dùng được **replication** đến nhiều máy chủ để đảm bảo **availability** và **fault tolerance**. Nếu một máy chủ gặp sự cố, hệ thống vẫn có thể cung cấp dịch vụ nhờ vào các bản sao của dữ liệu.

# Kiến trúc của hệ thống phân tán

Các mô hình kiến trúc của hệ thống phân tán có thể khác nhau tùy thuộc vào nhu cầu của ứng dụng và môi trường triển khai. Một số mô hình phổ biến bao gồm:

- **Kiến trúc Client-Server**: Một hoặc nhiều máy chủ cung cấp dịch vụ cho các máy khách. Máy khách gửi yêu cầu đến máy chủ, và máy chủ xử lý yêu cầu đó.
- **Kiến trúc Peer-to-Peer (P2P)**: Mỗi nút trong mạng đều có thể đóng vai trò là máy chủ hoặc máy khách. Mạng P2P thường được sử dụng trong các ứng dụng chia sẻ dữ liệu như BitTorrent.
- **Kiến trúc Microservices**: Mỗi dịch vụ trong ứng dụng được triển khai độc lập và giao tiếp với các dịch vụ khác qua API, giúp tăng tính mở rộng và khả năng bảo trì.

Ví dụ: Trong hệ thống điện toán đám mây, mô hình kiến trúc phổ biến là sử dụng **Microservices** để quản lý các chức năng độc lập, chẳng hạn như dịch vụ người dùng, dịch vụ thanh toán, dịch vụ thông báo. Các dịch vụ này có thể được triển khai trên các máy chủ khác nhau trong một hệ thống phân tán lớn, với mỗi dịch vụ có thể tự mở rộng hoặc thay đổi mà không ảnh hưởng đến các dịch vụ khác.
