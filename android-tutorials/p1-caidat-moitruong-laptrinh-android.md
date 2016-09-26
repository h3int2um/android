# Cài đặt môi trường lập trình Android

Thực hiện: Thi Minh Nhựt - Email: thiminhnhut@gmail.com

Thời gian: Ngày 26 tháng 09 năm 2016

## Tài liệu tham khảo

* Xem video hướng dẫn cài đặt trực tuyến trên Youtube của `ProgrammingKnowledge`:

	1. [How to install Oracle Java JDK on Ubuntu Linux (14.04 LTS)](https://www.youtube.com/watch?v=VrOhA-I3aFs&feature=youtu.be)

	2. [How to install Android Studio in Ubuntu Linux (14.04 LTS)](https://www.youtube.com/watch?v=axtVId9ASmY)
	
	3. [How to Install Genymotion Android Emulator in Ubuntu Linux](https://www.youtube.com/watch?v=k3MSTD9SLy4)
	
* Bài viết hướng dẫn của `Ngọc Lục`: [HƯỚNG DẪN CÀI ĐẶT JDK VÀ ANDROID STUDIO TRÊN LINUX](http://lucngoc.com/hoc-tap/huong-dan-cai-dat-jdk-va-android-studio-tren-linux/)
	
* Hoặc tải video hướng dẫn cài đặt của `ProgrammingKnowledge` theo địa chỉ:

	1. [How to install Oracle Java JDK on Ubuntu Linux (14.04 LTS)](https://drive.google.com/file/d/0BwKQkbSEXWHFekRfU3J0SThzdmM/view?usp=sharing)

	2. [How to install Android Studio in Ubuntu Linux (14.04 LTS)](https://drive.google.com/file/d/0BwKQkbSEXWHFR1JBSW15dXNpZ2M/view?usp=sharing)

## Hướng dẫn cài đặt Oracle Java JDK trên Ubuntu

* Bước 1: Mở cửa Terminal (nhấn `Ctrl + Alt + T`) cài đặt bằng các dòng lệnh bên dưới 
(làm theo hướng dẫn để hoàn thành quá trình cài đặt):

		sudo apt-add-repository ppa:webupd8team/java
		
		sudo apt-get update

		sudo apt-get install oracle-java8-installer
		
* Bước 2: Mở file `/etc/profile`

		sudo nano /etc/profile
		
* Bước 3: Thêm dòng bên dưới vào cuối file `profile`:

		export JAVA_HOME=/usr/lib/jvm/java-8-oracle
		
	Nhấn `Ctrl + X + Y` và `Enter` để lưu lại thay đổi.
	
	
## Hướng dẫn cài Genymotion trên Ubuntu

* Bước 1: Cài VirtualBox, [Download](https://www.virtualbox.org/wiki/Linux_Downloads), chọn phiên bản phù hợp với hệ điều hành.

* Bước 2: Tiến hành cài đặt file `.deb`, ví dụ: `virtualbox-5.1_5.1.6-110634-Ubuntu-trusty_i386.deb`. 
Mở file và chọn `Install`. Tiến hành cài đặt.

* Bước 3: Truy cập vào trang chủ của [Genymotion](https://www.genymotion.com/), tạo tài khoản để được download phần mềm.

* Bước 4: Sau khi tạo tài khoản trên `Genymotion` thành công, tiến hành [Download Genymotion](https://www.genymotion.com/download/). 
Chọn phiên bản 64 bit (không có phiên bản 32 bit cho Ubuntu). 

* Bước 5: Download thành công được file `.bin`, ví dụ: `genymotion-2.8.0-linux_x64.bin`. Copy và di chuyển file `.bin` 
đến thư mục `/home/username/`.

* Bước 6: Tiến hành cài đặt:

		cd ~
		
		chmod +x genymotion-2.8.0-linux_x64.bin
		
		./genymotion-2.8.0-linux_x64.bin
		
	Chọn `y` để bắt đầu cài đặt.

## Hướng dẫn cài đặt Android Studio trên Ubuntu

* Bước 1: Tải `Android-Studio` về máy: [Download](https://developer.android.com/studio/index.htm)

	Nếu máy tính sử dụng phiên bản hệ điều hành 64 bit thì cài thêm ứng dụng hỗ trợ chạy ứng dụng 32 bit:
	
			sudo apt-get install -y libc6-i386 lib32stdc++6 lib32gcc1 lib32ncurses5 lib32z1
			
* Bước 2: Sau khi tải về thành công được thư mục `android-studio-ide-*-linux.zip`, 
ví dụ: `android-studio-ide-145.3276617-linux.zip`. Copy `.zip` này và chuyển đến thư mục `/home/username/`.

* Bước 3: Tiến hành cài đặt, mở cửa sổ lệnh Terminal (`Ctrl + Alt + T`):

		cd ~
		
		unzip android-studio-ide-145.3276617-linux.zip
		
		cd android-studio/bin/
		
		sudo chmod 777 -R studio.sh
		
		./studio.sh
		
* Bước 4: Chọn `I do not have a previous version of Studio or I do not want to import my settings`. Click `OK`.

* Bước 5: Chọn `Next`. Chọn `Standard`. Chọn `Next`. Chọn `Finish`. Đợi quá trình cài đặt hoàn thành. Chọn `Finish`.
