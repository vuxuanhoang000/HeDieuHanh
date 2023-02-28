# Cài đặt Ubuntu

## I. Link tải xuống Ubuntu

-   [Trên trang chủ](https://ubuntu.com/download)

## II. Cài đặt drivers

## III. Cài đặt phần mềm

#### 1. Cài đặt các phần mềm .deb

-   [Google Chrome](https://www.google.com/intl/vi/chrome/)
-   [Microsoft Edge](https://www.microsoft.com/vi-vn/edge/download)
-   [Vs Code](https://code.visualstudio.com/Download)
-   [Git](https://git-scm.com/download/linux)

```bash
git config --global user.name "Vu Xuan Hoang"
git config --global user.email vuxuanhoang000@gmail.com
```

-   [Telegram](https://desktop.telegram.org/)

```bash
sudo apt update
sudo apt install telegram-desktop -y
```

#### 2. Cài bộ gõ tiếng việt Ibus-Bamboo

```bash
sudo add-apt-repository ppa:bamboo-engine/ibus-bamboo
sudo apt-get update
sudo apt-get install ibus ibus-bamboo –install-recommends
ibus restart
```

-   Vào `Settings` -> `Keyboard` nhấn vào dấu `+` trong phần `Input Sources` như hình.

![1](imgs/cai-go-tieng-viet-ubuntu-1.webp)

-   Một cửa sổ nhỏ hiện ra các bạn nhấn chọn vào `Vietnamese`.

![2](imgs/cai-go-tieng-viet-ubuntu-2.webp)

-   Chọn vào mục `Vietnamese (Bamboo)` rồi nhấn `Add` để thêm bộ gõ tiếng Việt cho Ubuntu.

![3](imgs/cai-go-tieng-viet-ubuntu-3.webp)

-   Nếu bạn không tìm thấy `Vietnamese (Bamboo)` trong danh sách thì hãy khởi động lại máy tính và thử lại.

-   Tiếp theo nhấn chọn vào `Show Applications` và chạy ứng dụng `Language Support`.

![4](imgs/cai-go-tieng-viet-ubuntu-4.webp)

-   Trong giao diện công cụ này, ở tab `Language` tìm đến `Keyboard input method system` và chuyển giá trị từ `Ibus` sang `none`.

![5](imgs/cai-go-tieng-viet-ubuntu-5.webp)

-   Bây giờ ở trên góc trên cùng bên phải có biểu tượng để chuyển giữa `en` và `vi` thì lúc này ta đã cài `unikey` cho Ubuntu thành công. Bước tiếp theo bạn chỉ cần thay đổi bộ gõ sang `Vietnamese (Bamboo)` để sử dụng.

#### 3. Cài bộ WPS Office

[Tải xuống tại trang chủ](https://www.wps.com/download/)

#### 4. Cài đặt Java

-   Cập nhật chỉ mục gói:

```bash
sudo apt update
```

-   Tiếp theo, kiểm tra xem Java đã được cài đặt chưa:

```bash
java -version
```

-   Nếu Java hiện chưa được cài đặt, bạn sẽ thấy đầu ra sau:

```
Output
Command 'java' not found, but can be installed with:

sudo apt install openjdk-11-jre-headless  # version 11.0.11+9-0ubuntu2~20.04, or
sudo apt install default-jre              # version 2:1.11-72
sudo apt install openjdk-13-jre-headless  # version 13.0.7+5-0ubuntu1~20.04
sudo apt install openjdk-16-jre-headless  # version 16.0.1+9-1~20.04
sudo apt install openjdk-8-jre-headless   # version 8u292-b10-0ubuntu1~20.04
```

-   Thực hiện lệnh sau để cài đặt Java Runtime Environment (JRE) mặc định, sẽ cài đặt JRE từ OpenJDK 11:

```bash
sudo apt install default-jre
```

-   JRE sẽ cho phép bạn chạy hầu hết các phần mềm Java.
-   Xác minh cài đặt với:

```bash
java -version
```

-   Bạn sẽ thấy đầu ra tương tự như sau:

```bash
Output
openjdk version "11.0.11" 2021-04-20
OpenJDK Runtime Environment (build 11.0.11+9-Ubuntu-0ubuntu2.20.04)
OpenJDK 64-Bit Server VM (build 11.0.11+9-Ubuntu-0ubuntu2.20.04, mixed mode, sharing)
```

-   Bạn có thể cần Bộ công cụ phát triển Java (JDK) ngoài JRE để biên dịch và chạy một số phần mềm dựa trên Java cụ thể. Để cài đặt JDK, hãy thực hiện lệnh sau, lệnh này cũng sẽ cài đặt JRE:

```bash
sudo apt install default-jdk
```

-   Xác minh rằng JDK đã được cài đặt bằng cách kiểm tra phiên bản của javac, trình biên dịch Java:

```bash
javac -version
```

-   Bạn sẽ thấy đầu ra sau:

```bash
Output
javac 11.0.11
```

#### 5. Cài đặt Python
