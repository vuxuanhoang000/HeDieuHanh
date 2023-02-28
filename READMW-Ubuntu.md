# Cài đặt Ubuntu

## I. Link tải xuống Ubuntu

-   [Trên trang chủ](https://ubuntu.com/download)

## II. Cài đặt drivers

## III. Cài đặt phần mềm

#### 1. Cài đặt các phần mềm .deb

-   [Google Chrome](https://www.google.com/intl/vi/chrome/)
-   [Microsoft Edge](https://www.microsoft.com/vi-vn/edge/download)
- [WPS Office](https://www.wps.com/download/)
-   [Vs Code](https://code.visualstudio.com/Download)
-   [Git](https://git-scm.com/download/linux)

```bash
sudo apt update && sudo apt upgrade
sudo apt-get install git -y
git config --global user.name "Vu Xuan Hoang"
git config --global user.email vuxuanhoang000@gmail.com
```

-   [Telegram](https://desktop.telegram.org/)

```bash
sudo apt update && sudo apt upgrade
sudo apt install telegram-desktop -y
```
- [OBS Studio](https://obsproject.com/download#linux)
```bash
sudo add-apt-repository ppa:obsproject/obs-studio
sudo apt update
sudo apt install ffmpeg obs-studio -y
```
- [VLC Media Player](https://www.videolan.org/vlc/download-ubuntu.html)
```bash
sudo snap install vlc
```
#### 2. Cài bộ gõ tiếng việt Ibus-Bamboo

```bash
sudo add-apt-repository ppa:bamboo-engine/ibus-bamboo
sudo apt-get update
sudo apt-get install ibus ibus-bamboo -y
sudo reboot
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
Command 'java' not found, but can be installed with:
sudo apt install openjdk-11-jre-headless  # version 11.0.18+10-0ubuntu1~22.04, or
sudo apt install default-jre              # version 2:1.11-72build2
sudo apt install openjdk-17-jre-headless  # version 17.0.6+10-0ubuntu1~22.04
sudo apt install openjdk-18-jre-headless  # version 18.0.2+9-2~22.04
sudo apt install openjdk-19-jre-headless  # version 19.0.2+7-0ubuntu3~22.04
sudo apt install openjdk-8-jre-headless   # version 8u362-ga-0ubuntu1~22.04
```

-   Thực hiện lệnh sau để cài đặt Java Runtime Environment (JRE) mặc định, sẽ cài đặt JRE từ OpenJDK 11:

```bash
sudo apt install openjdk-17-jre-headless -y
```

-   JRE sẽ cho phép bạn chạy hầu hết các phần mềm Java.
-   Xác minh cài đặt với:

```bash
java -version
```

-   Bạn sẽ thấy đầu ra tương tự như sau:

```bash
openjdk version "17.0.6" 2023-01-17
OpenJDK Runtime Environment (build 17.0.6+10-Ubuntu-0ubuntu122.04)
OpenJDK 64-Bit Server VM (build 17.0.6+10-Ubuntu-0ubuntu122.04, mixed mode, sharing)
```

-   Bạn có thể cần Bộ công cụ phát triển Java (JDK) ngoài JRE để biên dịch và chạy một số phần mềm dựa trên Java cụ thể. Để cài đặt JDK, hãy thực hiện lệnh sau, lệnh này cũng sẽ cài đặt JRE:

```bash
sudo apt install openjdk-17-jdk-headless -y
```

-   Xác minh rằng JDK đã được cài đặt bằng cách kiểm tra phiên bản của javac, trình biên dịch Java:

```bash
javac -version
```

-   Bạn sẽ thấy đầu ra sau:

```bash
javac 17.0.6
```

#### 5. Cài đặt Python
```bash
sudo apt install python3 -y
sudo apt install python3-pip -y
sudo apt install python3-venv -y
```
