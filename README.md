Miller–Rabin RSA Encryption Program in C
📌 Giới thiệu
Chương trình mô phỏng thuật toán mã hóa RSA bằng ngôn ngữ C. Chương trình tự động sinh hai số nguyên tố liên tiếp, tạo khóa RSA và thực hiện mã hóa — giải mã chuỗi ký tự do người dùng nhập.

🔧 Chức năng chính

✔ Kiểm tra số nguyên tố (Miller–Rabin)
Sử dụng thuật toán Miller–Rabin để xác định tính nguyên tố với độ chính xác cao.

✔ Sinh số nguyên tố
Tìm hai số nguyên tố liên tiếp lớn hơn giá trị người dùng nhập.

✔ Tạo khóa RSA
n = p × q

φ(n) = (p - 1) × (q - 1)

Tìm số mũ công khai e sao cho gcd(e, φ(n)) = 1

Tính số mũ bí mật d bằng thuật toán Euclid mở rộng

✔ Mã hóa & Giải mã
Mã hóa từng ký tự:
c = m^e mod n

Giải mã từng ký tự:
m = c^d mod n

▶ Hướng dẫn chạy
1. Biên dịch
bash
gcc rsa.c -o rsa
2. Chạy chương trình
bash
./rsa
3. Nhập dữ liệu
Nhập một số n → chương trình tìm hai số nguyên tố p, q lớn hơn n

Nhập chuỗi ký tự cần mã hóa (không có khoảng trắng)

📥 Ví dụ nhập

text

Enter n: 10

Enter the message to encrypt (string): hello

📤 Ví dụ xuất

Hai số nguyên tố p, q

n, φ(n)

Khóa công khai (e, n)

Khóa bí mật (d, n)

Dãy số sau khi mã hóa

Chuỗi gốc sau khi giải mã

⚠ Lưu ý

Đây là phiên bản học thuật của RSA, không dùng cho môi trường bảo mật thực tế

Mã hóa theo từng ký tự ASCII (không theo khối)

Không hỗ trợ chuỗi có khoảng trắng hoặc ký tự đặc biệt phức tạp
