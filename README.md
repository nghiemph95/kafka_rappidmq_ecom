# Real-time E-commerce Platform with Kafka and RabbitMQ

Một nền tảng thương mại điện tử thời gian thực sử dụng kiến trúc microservice với Kafka và RabbitMQ.

## Kiến trúc hệ thống

![Kiến trúc hệ thống](./docs/architecture.png)

## Các service chính

1. **API Gateway**: Điểm vào chính, xử lý routing, xác thực
2. **Order Service**: Xử lý logic đặt hàng
3. **Payment Service**: Xử lý thanh toán
4. **Inventory Service**: Quản lý tồn kho
5. **Notification Service**: Gửi thông báo

## Công nghệ sử dụng

- **Ngôn ngữ**: Node.js với TypeScript
- **Framework**: NestJS
- **Database**: MongoDB, Redis
- **Message Brokers**: Apache Kafka, RabbitMQ
- **Containerization**: Docker, Docker Compose

## Cài đặt và chạy

### Yêu cầu

- Docker và Docker Compose
- Node.js 16+
- npm hoặc yarn

### Cách chạy

1. Clone repository:
   ```bash
   git clone [your-repo-url]
   cd kafka_rabbitmq_ecom
   ```

2. Sao chép file cấu hình mẫu:
   ```bash
   cp .env.example .env
   ```

3. Khởi động các service bằng Docker Compose:
   ```bash
   docker-compose up -d
   ```

4. Khởi động các service (development):
   ```bash
   # Trong thư mục gốc
   npm install
   npm run start:dev
   ```

## Cấu trúc thư mục

```
kafka_rabbitmq_ecom/
├── .github/workflows/    # GitHub Actions workflows
├── docker/               # Dockerfiles cho các service
├── scripts/              # Các script tiện ích
├── services/             # Các microservices
│   ├── api-gateway/      # API Gateway service
│   ├── order-service/    # Order service
│   ├── payment-service/  # Payment service
│   ├── inventory-service/ # Inventory service
│   └── notification-service/ # Notification service
├── .env.example         # Mẫu file cấu hình
├── .gitignore           # Git ignore file
├── docker-compose.yml   # Docker compose cho tất cả services
└── README.md           # Tài liệu dự án
```

## Tài liệu API

Xem [API Documentation](./docs/API.md) để biết chi tiết về các endpoints.

## Giấy phép

MIT
