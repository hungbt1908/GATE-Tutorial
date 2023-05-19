# HƯỚNG DẪN CÀI ĐẶT GATE
## 1. Cài đặt Gate cho hệ điều hành Linux

### 1.1. Cài đặt Geant4 10.06.p3
* Tham khảo cách cài đặt Geant4 tại [đây](https://github.com/hungbt1908/G4-User-Template)
* Lưu ý: để có thể biên dịch thành công Gate, người dùng cần phải tắt chế độ tính toán đa luồng khi biên dịch Geant4 bằng tùy chọn sau:
    ```c++
    -DGEANT4_BUILD_MULTITHREADED=OFF
    ```

### 1.2. Cài đặt ROOT 6.20.02
* Tham khảo cách cài đặt ROOT tại [đây](https://github.com/hungbt1908/G4-User-Template)

### 1.3. Cài đặt Libtorch
* Tải về thư viện libtorch ở [đây](https://drive.google.com/file/d/1BEptW-vgiKl7Fflw9KyfWTPeVudGHbDI/view?usp=share_link)
* Giải nén tệp tin vào thư mục Softwares
* Thêm biến môi trường sau cho thư viện libtorch
    ```c++
    # Libtorch
    export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/home/hungbt/Softwares/libtorch/lib
    ```

### 1.4. Cài đặt ITK
* Tải về gói mã nguồn ITK tại [đây](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmw2QnY3cmpiNjRhMEdlQXVnRHVneGxzZVl0d3xBQ3Jtc0trTzhUcU1QWmJWcUNUWnZicUJnLUs1eXdrai00S3AwVkJjdVNuOFROa0U2WTU1YXZiTXBIdDVvZmFzUTljWTJ4STlnUUg3MDRnY3ZFVFU4R3dCZzF4ZVlsYkxKeERpTDFZcDBqWUxsZXJwMzY0cUVjRQ&q=https%3A%2F%2Fgithub.com%2FInsightSoftwareConsortium%2FITK%2Freleases%2Fdownload%2Fv5.1.1%2FInsightToolkit-5.1.1.zip&v=mwc8MNjP8pU)
* Giải nén tệp tin trong thư mục Softwares
* Mở cửa sổ Terminal trong thư mục đã giải nén
* Nhập lệnh sau

    ```c++
    mkdir bin && cd bin
    ```
* Tiếp tục
    ```c++
    ccmake -DITK_USE_REVIEW=ON ..
    ```
    nhấn C và Enter để bắt đầu. Bật tùy chọn "Module_RTK=ON" và nhấn c để cấu hình sau đó nhấn g để xác nhận.
* Biên dịch mã
    ```c++
    make -j4
    ```
* Cài đặt mã nguồn:
    ```c++
    sudo make install
    ```


## 2. Cài đặt VGate trên máy ảo VirtualBox


