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

![image](https://github.com/chinh310503/WxMCTF-2024-Write-Ups/assets/90301956/4dbf34c8-782d-4a4e-a519-be7655d53e47)

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






