# Make file là gì ? 

`Makefile` là một tệp hướng dẫn cho chương trình `make`, giúp tự động hóa quá trình biên dịch mã nguồn thành chương trình chạy được. Nó liệt kê các quy tắc và mối quan hệ giữa các tệp, để khi bạn thay đổi một phần mã, make chỉ cần biên dịch lại những phần bị ảnh hưởng mà không phải biên dịch toàn bộ dự án, giúp tiết kiệm thời gian.

# Cấu trúc Makefile 

Trước khi sử dụng Makefile hãy cùng tìm hiểu về cấu trúc của nó:

> ![alt text](Image\Make_file_structure.png)

Giải thích: 
> - Target (Mục tiêu): Đây là cái bạn muốn tạo ra, như tệp thực thi hoặc nhiệm vụ cần thực hiện. Ví dụ, nếu bạn đang viết chương trình, target có thể là tệp chạy được như các file `.exe`.
>
> -  Dependencies (Phụ thuộc): Đây là những tệp cần có để tạo ra target (Target phụ thuộc vào những file này). Ví dụ, nếu `sum` cần `main.o` và `sum.o` thì hai tệp đó là dependencies. Nếu bất kỳ tệp nào trong dependencies thay đổi, Makefile sẽ biết để biên dịch lại `sum`.
>
> - Shell lines trong Makefile là các dòng chứa lệnh mà hệ thống sẽ chạy trong môi trường dòng lệnh (shell) của `Linux` hoặc `Unix`.
>
> - Rules (Quy tắc): Đây là các lệnh chỉ dẫn cách tạo ra target từ dependencies. Thường là các lệnh biên dịch để chuyển đổi từ mã nguồn thành tệp thực thi.

# Cú pháp Makefile