# TTCS_UDnghenhac
Ho va ten : Huynh Ngoc Hung
MSSV:61133707



I.Phân tích bài toán
1.Giới thiệu
Trong bài toán này đây là dạng ứng dụng và tôi sẽ sử dụng windowform 
-Ứng dụng nghe nhạc được viết bằng c# .Ý tưởng lấy từ chương trình nghe nhạc windowns Media Player Trên hệ điều hành Windowns sử dụng bunifuframework Để thiết kế GUI, WMPLib
2.Quá trình phát triển trên window c#
Ngôn ngữ lập trình C# chính là ngôn ngữ được nâng cấp lên từ C++ và Java và là một ngôn ngữ lập trình hướng đối tượng, ngôn ngữ C# cũng là một trong những ngôn ngữ sử dụng phổ biến hiện nay được sử dụng trên nền .Net với nhiều tính năng giúp cho việc lập trình trở lên dễ dàng hơn
.NET Framework
–Microsoft .NET Framework là môi trường chung cho việc xây dựng, triển khai và chạy các ứng dụng 
• Không gắn chặt vào hệ điều hành 
• Không gắn chặt vào ngôn ngữ 
• Nhiều tiện ích khác giúp cho việc phát triển các ứng dụng nhanh, hiệu quả hơn.
• .NET My Services  
– .NET My Services là một tập XML Web Service cho phép user truy cập thông tin qua Internet. Dùng các .NET My Service các ứng dụng có thể truyền thông trực tiếp bằng giao thức SOAP và XML
NET 5.0 là phiên bản tiếp theo của nền tảng .NET Core của Microsoft và là một nỗ lực để thống nhất hệ sinh thái cho các nhà phát triển của nó
NET 5.0 là phiên bản tiếp theo của nền tảng .NET Core của Microsoft và là một nỗ lực để thống nhất hệ sinh thái cho các nhà phát triển của nó.
Microsoft đã phát hành .NET 5.0, bản phát hành mới lớn nhất trong nền tảng phát triển .NET, cùng với các cập nhật khác, giới thiệu ngôn ngữ lập trình mới C# 9.0
.NET 5.0 là bản cập nhật đầu tiên cho nền tảng này kể từ khi Microsoft thông báo sẽ thống nhất bộ công cụ dành cho nhà phát triển của mình trên các nền tảng và các hệ điều hành. Điều này có nghĩa là, với .NET 5.0, các nhà phát triển có quyền truy cập vào một bộ duy nhất của các API, các ngôn ngữ và các công cụ để sử dụng bất kể họ đang xây dựng ứng dụng  cho máy tính để bàn, cho thiết bị di động, đám mây hay Internet of Things (IoT).
.NET 5.0 Vì có nhưng công nghệ mới 
•	.NET 5 có thể truy cập từ dotnet.microsoft.com hoặc bản cập nhật Visual Studio 2019 mới phát hành 16.8. Các khả năng chính khác trong .NET 5 bao gồm:
•	Hỗ trợ Windows ARM64.
•	Cải tiến phát triển máy tính để bàn Windows.
•	Các API trình tuần tự JSON được cải tiến.
•	Chú thích kiểu tham chiếu không thể xóa.
•	Đầu tư web và đám mây.
•	Các ứng dụng file đơn và hình ảnh vùng chứa nhỏ hơn.
•	Cải thiện hiệu suất, với hiệu suất gRPC được cho là vượt qua Go, C ++ và Java.
•	Các ứng dụng .NET đầy đủ với frameword giao diện người dùng web Blazor, hỗ trợ Blazor Server và Blazor WebAssembly, hỗ trợ các thư viện khung .NET Core và đã được thực hiện nhanh hơn trong .NET 5.
•	Một mô hình mới được đặc trưng để hỗ trợ các API WinRT, bao gồm gọi các API, sắp xếp dữ liệu giữa hai hệ thống kiểu và thống nhất các kiểu được thiết kế để xử lý giống nhau trên hệ thống kiểu hoặc ranh giới ABI. Hệ thống tương tác WinRT hiện có đã bị xóa khỏi thời gian chạy .NET.
-Các chức năng cơ bản 
+ Phát nhạc và video(mp3,mp4)
+Tìm kiếm nhạc
+ Chuyển đổi qua lại giữa các bài hát và video
II.Tìm hiểu giải thuật 
1.Định dạng file là gì?
Định dạng file hay định dạng tập tin là cách thông tin được mã hóa và lưu trữ. Nó chỉ định cách các bit được sử dụng để mã hóa thông tin trong một phương tiện lưu trữ kỹ thuật số.




2..Những định dạng âm thanh cơ bản phổ biến nhất hiện nay
+MP3








File MP3 MP3 là cụm từ viết tắt của MPEG-1 audio Player 3 hay Motion Pictures Expert Group 1 Layer 3.
Đây là định dạng âm thanh được tạo ra qua quá trình cắt bỏ bớt dãy âm quá thấp và quá cao khi nén âm thanh. MP3 là file âm thanh phổ biến nhất hiện nay, có đặc điểm là rất nhẹ, dễ dàng tải về và chia sẻ, nhưng nhược điểm là chất lượng âm thanh sẽ bị giảm nhiều so với bản gốc ở phòng thu.
Các file MP3 có đuôi file là .mp3.
 +  WMA








WMA - Windows Media Audio. Định dạng này do Microsoft tạo ra để cạnh tranh cùng MP3. Với ưu điểm là dung lượng còn nhẹ hơn cả MP3 nhưng chất lượng lại tương đương nên nó cũng được yêu thích bởi khá nhiều người chơi.




+WAV









WAV - Waveform Audio File Format. Được xem là sự thay thế cho các bản gốc studio hoặc CD và được tạo ra bởi Microsoft hợp tác cùng IBM. Nhưng cũng vì thế, dung lượng của nó khá nặng và chất âm không thua âm thanh phòng thu.
3.Những chuẩn flle video 
+File AVI
AVI là tên viết tắt của Audio Video Interleave và được phát triển bởi Microsoft.
AVI là file không nén, vì vậy mà cho ra chất lượng video, âm thanh tốt, hình ảnh rõ nét hơn những file khác.
Các file AVI có phần đuôi .avi, vì là file không nén nên file AVI chiếm khá nhiều dung lượng và hạn chế thiết bị phát, không phải thiết bị nào cũng tương thích với địn dạng video này.
Định dạng AVI thường được sử dụng trên các hệ thống như Windows, macOS, Linux,...
 

+File MP4
Định dạng MP4 (viết tắt của Moving Pictures Expert Group 4) là định dạng đã quá quen thuộc với hầu hết mọi người, bởi sự tương thích cực cao, đa số trình xem video đều sử dụng được.
Các file MP4 có phần đuôi .mp4 đem đến những video chất lượng cao mà chỉ chiếm một dung lượng khá thấp. Chính vì vậy mà những kênh streaming online nổi tiếng, thậm chí cả YouTube và Vimeo, đều sử dụng định dạng này. MP4 được tạo ra bằng cách nén dữ liệu nên mặc dù mang ưu điểm nhẹ, dễ sao chép nhưng chất lượng hình ảnh sẽ kém hơn file không nén như AVI.











+File WMV
WMV là viết tắt của Windows Media Video. Định dạng file có đuôi là .mkv này được phát triển bởi Microsoft.
WMV được sử dụng để chạy trên tất cả hệ điều hành Windows, và có cả trình phát WMV miễn phí trên hệ điều hành macOS. Định dạng file này được sử dụng rộng rãi trên mạng nhờ chất lượng hình ảnh tốt, kích thước nhỏ gọn, giúp người dùng dễ dàng tải, chia sẻ qua email.
+File MKV
MKV là tên viết tắt của Matroska Video, là định dạng có thể kết hợp đa phương tiện từ âm thanh, video, và phụ đề vào trong một tập tin duy nhất. Khi bạn tải phim từ trên mạng xuống thì những file nhúng sẵn phụ đề thường có định dạng đuôi là .mkv.

File MKV có dung lượng không quá cao, dễ dàng tải về và chia sẻ, và có chất lượng âm thanh, hình ảnh khá tốt.










+File 3GP
3GP được phát triển bởi Third Generation Partnership Project. Đây là phiên bản thu gọn của chuẩn MP4 đang được sử dụng phổ biến cho đa số các dòng điện thoại hiện nay.
Định dạng 3GP được thiết kế để giảm dung lượng và băng thông video để phù hợp với các dòng điện thoại được hỗ trợ. File này sử dụng chuẩn hình ảnh MPEG-4, H2.263 và âm thanh AMR-NB, AAC-LC.
Các file 3GP có đuôi file là .3gp.
III.Tìm hiểu công cụ lập trình
Visual studio là một trong những công cụ hỗ trợ lập trình website rất nổi tiếng nhất hiện nay của Mcrosoft và chưa có một phần mềm nào có thể thay thế được nó. Visual Studio được viết bằng 2 ngôn ngữ đó chính là C# và VB+. Đây là 2 ngôn ngữ lập trình giúp người dùng có thể lập trình được hệ thống một các dễ dàng và nhanh chóng nhất thông qua Visual Studio.
Visual Studio là một phần mềm lập trình hệ thống được sản xuất trực tiếp từ Microsoft. Từ khi ra đời đến nay, Visual Studio đã có rất nhiều các phiên bản sử dụng khác nhau. Điều đó, giúp cho người dùng có thể lựa chọn được phiên bản tương thích với dòng máy của mình cũng như cấu hình sử dụng phù hợp nhất.
Bên cạnh đó, Visual Studio còn cho phép người dùng có thể tự chọn lựa giao diện chính cho máy của mình tùy thuộc vào nhu cầu sử dụng.
Một số tính năng của phần mềm Visual Studio
•	Biên tập mã
Giống như bất kỳ một IDE khác, Visual Studio gồm có một trình soạn thảo mã hỗ trợ tô sáng cú pháp và hoàn thiện mả bằng các sử dụng IntelliSense không chỉ cho các hàm, biến và các phương pháp mà còn sử dụng cho các cấu trúc ngôn ngữ như: Truy vấn hoặc vòng điều khiển.
Bên cạnh đó, các trình biên tập mã Visual Studio cũng hỗ trợ cài đặt dấu trang trong mã để có thể điều hướng một cách nhanh chóng và dễ dàng. Hỗ trợ các điều hướng như: Thu hẹp các khối mã lệnh, tìm kiếm gia tăng,…
Visual Studio còn có tính năng biên dịch nền tức là khi mã đang được viết thì phần mềm này sẽ biên dịch nó trong nền để nhằm cung cấp thông tin phản hồi về cú pháp cũng như biên dịch lỗi và được đánh dấu bằng các gạch gợn sóng màu đỏ.
•	Trình gỡ lỗi
Visual Studio có một trình gỡ lỗi có tính năng vừa lập trình gỡ lỗi cấp máy và gỡ lỗi cấp mã nguồn. Tính năng này hoạt động với cả hai mã quản lý giống như ngôn ngữ máy và có thể sử dụng để gỡ lỗi các ứng dụng được viết bằng các ngôn ngữ được hỗ trợ bởi Visual Studio.

•	Windows Forms Designer
Được sử dụng với mục đích xây dựng GUI sử dụng Windows Forms, được bố trí dùng để xây dựng các nút điều khiển bên trong hoặc cũng có thể khóa chúng vào bên cạnh mẫu. Điều khiển trình bày dữ liệu có thể được liên kết với các nguồn dữ liệu như: Cơ sở dữ liệu hoặc truy vấn.
•	WPF Designer
Tính năng này cũng giống như Windows Forms Designer có công dụng hỗ trợ kéo và thả ẩn dụ. Sử dụng tương tác giữa người và máy tính nhắm mục tiêu vào Windows Presentation Foundation.
•	Web designer/development
Visual Studio cũng có một trình soạn thảo và thiết kế website cho phép các trang web được thiết kế theo tính năng kéo và thả đối tượng. Mục đích là để hỗ trợ người dùng tạo trang web dễ dàng hơn, những yêu cầu đơn giản như thiết kế web du lịch hay các trang giới thiệu của công ty có thể sử dụng tính năng này vì nó vẫn đảm bảo cho bạn sở hữu được một website hoàn chỉnh.
– Visual Studio hỗ trợ lập trình trên nhiều ngôn ngữ như: C/C++, C#, F#, Visual Basic, HTML, CSS, JavaScript.
– Là một công cụ hỗ trợ việc Debug một cách dễ dàng và mạnh mẽ như: Break Point, xem giá trị của biến trong quá trình chạy, hỗ trợ debug từng câu lệnh.
– Giao diện Visual Studio rất dễ sử dụng đối với người mới bắt đầu lập trình.
– Visual Studio hỗ trợ phát triển các ứng dụng: desktop MFC, Windows Form, Universal App, ứng dụng mobile Windows Phone 8/8.1, Windows 10, …
– Visual Studio hỗ trợ xây dựng ứng dụng một cách chuyên nghiệp bằng các công cụ kéo thả.
– Visual Studio được đông đảo lập trình viên trên thế giới sử dụng.

IV.Mô tả giải thuật và cài đặt thực toán
- Chương trình nghe nhạc này có những chức năng nghe nhạc,xem video, tìm kiếm nhac
 
Đoạn code có chức năng phóng to và ẩn windows form 
Thu nhỏ windows form
 
Close
 
Button next
 
Button back
 
Play
 
Pause
 Mở file 







 



Time
 
List Music
 





 
a.Cá nhân













Hình 1. Cá nhân

b.Albums













Hình 2 . Albumns

C.MV














Hình 3: MV
Link gihub https://github.com/ngochung130201/TTCS_UDnghenhac





