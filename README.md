# WxMCTF '24 Web 1 - Mr. P
Đề cho ta 1 trang web như sau

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/13635ae5-c9dd-4258-a55f-084f737edd75)

Xem source code của trang web ta nhận được Flag

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/52b33813-e07c-4d55-829b-42538c239564)

Flag: wxmctf{4nd_h1s_n4me_1s!!!!!!!}

# WxMCTF '24 Web 2 - Compiler

Đề bài cho ta source của trang web. Nhìn qua thì đây là một trang web cho phép người dùng nhập code python và thực thi code đó

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/99f4f937-fddf-49e0-bf5a-b93a02e9d463)

Trong source code của trang web ta thấy được một Fake Flag ở trong Dockerfile.

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/ce0846a7-da1e-4d1f-be3b-04a12bb64353)


Điều này cũng gợi ý trong Dockerfile của trang web đang chạy sẽ giữ flag. Ta thực hiện chạy code python để xem file Dockerfile và lấy được flag

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/11aba097-7c10-4759-8164-18deb2e4d24e)

Flag: wxmctf{ok4Y_M4y8e_I_5K1mpED_@_bit}

# WxMCTF '24 Web 3 - Brawl: The Heist
Đề bài cho ta source code của trang web. Nhìn chung đây là source code thực hiện chuyển tiền từ Eatingfood đến các ví khác. Trong ví Eatingfood ban đầu có 1$, nếu số tiền lớn hơn 10000$ thì sẽ in ra Flag cho ta.

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/ed958534-cbc2-4675-8957-db4ce29ce21d)

Đọc code trang web, ta nhận thấy trang web đang bị lỗi Server-side parameter pollution, có thể xem thêm tại đây: https://portswigger.net/web-security/api-testing/server-side-parameter-pollution

Ta dùng burpsuite để sửa request, thêm &amount = 1000000 vào trong request. Cuối cùng nhận được Flag:

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/83e3e128-9c29-4184-9b30-14cb57e54446)

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/53ca7610-35f7-454b-b3dd-8578393307dc)

Flag: wxmctf{p4rAm373r_P0lLU7IOn}

# WxMCTF '24 Forensics 1- 諸葛亮
Đề bài cho ta 1 file answer.txt mở ra ta thấy như sau

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/dbcead9f-9fae-49d1-9c4d-6f8e93c4a37b)

Copy và giải mã bin string ta nhận được đoạn văn sau.

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/6a52e333-19d8-4ceb-85f4-9c170f9f0ab8)

Flag: wxmctf{Eightfold Battle Formation}

# WxMCTF '24 Forensics 2 - Covert Chinchillas
Đề bài cho ta một file ảnh. Ta dùng lệnh file để xem thông tin của file ảnh

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/0d463f63-22c9-48bb-b9b9-226c370c52ab)

Nhận thấy comment của ảnh là một mật mã, ta giải mã ra được nội dung sau.

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/5fe2e3fa-a51d-4ae4-8f7a-b93c30be0c68)

Dùng steghide và password vừa giải mã được, ta nhận được Flag.

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/a8c141b1-f1f2-4985-90ac-727d76f6f99f)

Flag: wxmctf{7h1n95_423_n07_41w4y5_wh47_7h3y_533m}

# WxMCTF '24 Misc 1 - Arrgh 
Đề bài cho ta một file apk. Dùng apktool để tạo thư mục từ file apk ta được thư mục app.

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/bfaedd4e-dfc6-4bc0-b585-12376f537c8d)

Dùng lệnh find app -type f -iname "*flag*" đề tìm ra file có tên chứa từ flag ta nhận được

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/8f724281-4805-4083-83a3-3360fe41bc9b)

Tìm các file flag.png trong các thư mục ta nhận được flag

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/4bd87efa-b5cf-45e6-9193-3be765af1f04)

Flag: wxmctf{4ndr01d_4n4lys1s}

# WxMCTF '24 Misc 3 - firstgrep 
Đề bài cho ta một file zip. Ta thực hiện giải nén. Thấy trong thư mục có rất nhiều thư mục con và các file txt chứa fake flag

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/3b7556a2-dce1-41d7-8e36-01cb92e91b42)

Ta dùng lệnh để loại bỏ các file chứa fake flag và nhận được flag

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/67532bcb-20aa-4a81-84b2-8eedd895e61b)

Flag: wxmctf{Wha7_W0uLD_w3_6e_w17HouT_Gr3P}




















