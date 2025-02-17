 GaiaNet trên hệ điều hành Linux:

1. Yêu cầu hệ thống
Trước khi bắt đầu, đảm bảo rằng hệ thống của bạn đáp ứng các yêu cầu tối thiểu:

Ubuntu Linux 20.04 với Nvidia CUDA 12 SDK (nếu sử dụng GPU).
8GB VRAM trên GPU (hoặc cao hơn).
32GB RAM được khuyến nghị (16GB là tối thiểu).

2. Tải và cài đặt node GaiaNet
Tải script cài đặt: Sử dụng lệnh sau để tải và chạy script cài đặt GaiaNet:

bash
Sao chép
Chỉnh sửa
curl -sSfL 'https://github.com/GaiaNet-AI/gaianet-node/releases/latest/download/install.sh' | bash
Cài đặt đường dẫn môi trường: Sau khi hoàn tất, terminal sẽ in ra một lệnh source. Chạy lệnh này để thiết lập biến môi trường, ví dụ:

bash
Sao chép
Chỉnh sửa
source ~/.bashrc
Khởi tạo GaiaNet node: Chạy lệnh sau để khởi tạo node với cấu hình mặc định (sử dụng Llama 3.2 và dữ liệu về Paris):

bash
Sao chép
Chỉnh sửa
gaianet init
Lưu ý: Lệnh này sẽ tải các file mô hình (có dung lượng lớn) nên có thể mất thời gian.

3. Bắt đầu node GaiaNet
Sử dụng lệnh sau để khởi động node:

bash
Sao chép
Chỉnh sửa
gaianet start
4. Sau khi khởi động node
Nếu node được khởi động thành công, bạn sẽ thấy một URL công khai được in ra, ví dụ:
python
Sao chép
Chỉnh sửa
... https://0xf63939431ee11267f4855a166e11cc44d24960c0.gaianet.xyz
Truy cập URL trên trình duyệt để xem thông tin node và tương tác với AI agent.
5. Dừng node
Khi muốn dừng node, bạn có thể sử dụng lệnh:

bash
Sao chép
Chỉnh sửa
gaianet stop
6. Debug và xem logs
Nếu gặp lỗi hoặc cần kiểm tra hoạt động của node:

Xem log chi tiết:
bash
Sao chép
Chỉnh sửa
tail -f ~/gaianet/log/*
Kiểm tra trạng thái node:
bash
Sao chép
Chỉnh sửa
gaianet status
