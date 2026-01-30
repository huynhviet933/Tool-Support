# Tool-Support
Automatically create wallet address. Email, user, ...
HƯỚNG DẪN CÀI ĐẶT VÀ SỬ DỤNG VIET MMO TOOL KIT

A. CHUẨN BỊ HỆ THỐNG
1. Cài đặt Node.js: Tải và cài đặt Node.js (phiên bản LTS) từ https://nodejs.org/
2. Tạo thư mục làm việc: Tạo một thư mục mới (ví dụ: ToolMMO), bỏ file Pro.js vào đó.

B. CÀI ĐẶT THƯ VIỆN (MỞ TERMINAL/CMD TẠI THƯ MỤC TOOL)
Chạy lệnh sau để cài đặt các thành phần cần thiết:

npm install ethers exceljs readline-sync cli-progress chalk@4.1.2 axios tweetnacl xlsx @mysten/sui.js https-proxy-agent

C. CẤU HÌNH TRƯỚC KHI CHẠY
1. License: Khi chạy lần đầu, tool sẽ yêu cầu nhập Key License. Key này sẽ được lưu vào file license.txt.
2. Proxy (Nếu dùng tính năng Mail.tm): 
   - Tạo file proxy.txt trong cùng thư mục.
   - Nhập proxy định dạng: http://user:pass@ip:port hoặc http://ip:port (mỗi dòng 1 proxy).

D. CÁCH CHẠY TOOL
Mở Terminal/CMD và gõ lệnh:
node Pro.js

E. CHI TIẾT CÁC TÍNH NĂNG TRONG MENU:

1. [EVM] Generate Wallets (Excel):
   - Tạo ví Ethereum/BSC/Polygon/Arbitrum...
   - Tùy chọn 12 hoặc 24 ký tự bảo mật (Mnemonic).
   - Kết quả lưu tại: evm_wallets.xlsx

2. [SOL] Generate Solana Wallets (Excel):
   - Tạo ví Solana (định dạng Base58).
   - Kết quả lưu tại: solana_wallets.xlsx

3. [SUI] Generate Sui Wallets (Txt):
   - Tạo ví mạng SUI.
   - Kết quả lưu tại: sui_wallets.txt

4. [UA] Generate User Agents:
   - Tạo danh sách trình duyệt ảo để nuôi acc/cheat air.
   - Kết quả lưu tại: user_agents.txt

5. [NAME] Generate Usernames:
   - Tạo tên người dùng ngẫu nhiên (kết hợp họ tên Việt/Anh và số).
   - Kết quả lưu tại: usernames.txt

6. [QUEST] Generate Crypto Questions:
   - Tạo các câu hỏi ngẫu nhiên về Crypto (dùng cho các form khảo sát).
   - Kết quả lưu tại: questions.txt

7. [MAIL] Create Mail.tm:
   - Tự động tạo tài khoản Email ảo (Mail.tm).
   - Chạy đa luồng (5 luồng cùng lúc).
   - Sử dụng Proxy từ file proxy.txt (nếu có) để tránh bị chặn IP.
   - Kết quả lưu tại: mail.txt (Định dạng: Email|Mật khẩu|Token)

F. LƯU Ý QUAN TRỌNG:
- Log hoạt động: Mọi thao tác đều được ghi lại trong file logs.txt.
- Bảo mật: File Excel/Txt chứa Private Key rất quan trọng, tuyệt đối không gửi cho người khác.
- Lỗi License: Tool xác thực dựa trên HWID (Mã phần cứng máy tính), mỗi key thường chỉ dùng cho 1 máy.
