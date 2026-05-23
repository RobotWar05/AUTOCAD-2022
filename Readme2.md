# 🛠️ Clement-AutoCAD
> **Phiên bản áp dụng:** AutoCAD Mechanical 2022

![AutoCAD](https://img.shields.io/badge/Tools-AutoCAD_Mechanical-red?style=flat-square)
![Status](https://img.shields.io/badge/Status-Learning-green?style=flat-square)
![Author](https://img.shields.io/badge/Author-Clement-blue?style=flat-square)

---

## 📑 MỤC LỤC (TABLE OF CONTENTS)
*(Click vào dòng dưới để nhảy đến mục cần xem)*

1. [⚡ Quy tắc vận hành chung](#quytac)
2. [🛠️ Nhóm 1: Cài đặt & Hỗ trợ (Setup & Aids)](#group1)
3. [✏️ Nhóm 2: Công cụ Vẽ (Draw)](#group2)
4. [✂️ Nhóm 3: Công cụ Chỉnh sửa (Modify)](#group3)
5. [📝 Nhóm 4: Text & Ký tự đặc biệt](#group4)
6. [📏 Nhóm 5: Kích thước & Đường tâm (Dimension & Centerlines)](#group5)
7. [📦 Nhóm 6: Block & Quản lý Layer nâng cao](#group6)
8. [🔍 Nhóm 7: Thống kê & Lọc dữ liệu thông minh](#group7)
9. [💡 Mục đề xuất tham khảo](#dexuat)

---

<a name="quytac"></a>
## ⚡ QUY TẮC VẬN HÀNH CHUNG
* Luôn để ngôn ngữ là ENG khi thao tác để không bị lỗi khi nhập lệnh.
* **Phím SPACE (Cách) = ENTER:** Ngón cái tay trái luôn đặt ở phím Space để gọi lệnh nhanh.
* **Lặp lại lệnh:** Nhấn Space/Enter khi không có lệnh nào -> Gọi lại lệnh vừa dùng.
* **Thoát lệnh:** Luôn nhấn `ESC` (2-3 lần) để hủy bỏ lệnh cũ trước khi nhập lệnh mới.
* **Bảng Setup (Dialog):** Nếu lệnh hiện bảng cài đặt, nhập số trực tiếp vào bảng hoặc gõ `D` để bật/tắt bảng này.
* **Phân biệt cấu trúc hình học đối tượng:** * **LINE** = Đoạn thẳng rời rạc từng phần.  
  * **PLINE / POLYLINE** = Chuỗi nhiều đoạn nối liền dính nhau thành 1 đối tượng duy nhất.  
  * **SPLINE** = Đường cong mềm mịn tự do (Không phải đường vô tận).  
  * **XLINE** = Đường thẳng vô tận kéo dài hai đầu dùng để dựng hình chiếu.

---

<a name="group1"></a>
## 🛠️ Nhóm 1: Cài đặt & Hỗ trợ vẽ (Setup & Aids)

### 1.1. Thiết lập thông số hình học ban đầu

| Lệnh / Phím | Phím Tắt | Chức Năng | Ghi chú vận hành |
| :--- | :--- | :--- | :--- |
| **UNITS** | `UN` | Thiết lập đơn vị bản vẽ | Bắt buộc thiết lập Milimeters lúc khởi tạo |
| **MVSETUP** | `MVSETUP` | Thiết lập nhanh khổ giấy | Chọn No -> Metric -> Nhập Tỉ lệ |
| **ORTHO** | `F8` | Chế độ khóa thẳng góc | Bật liên tục để kiểm soát hướng ngang/dọc tuyệt đối |
| **POLAR** | `F10` | Chế độ vẽ theo tia góc | Hỗ trợ bắt góc nghiêng định hình trước (30, 45, 90...) |
| **DYNAMIC INPUT** | `F12` | Hiển thị thông số tại con trỏ | Nhập kích thước trực tiếp tại vị trí chuột |
| **CHUYỂN Ô** | `TAB` | Chuyển đổi ô nhập dữ liệu | Chuyển giữa ô Chiều dài và ô Góc (khi bật F12) |
| **TỌA ĐỘ CỰC** | `@L<A` | Nhập khoảng cách và góc | Cấu trúc: `@Chiều_Dài<Góc_Độ` (Ví dụ: `@100<45`) |
| **TỌA ĐỘ TƯƠNG ĐỐI** | `@X,Y` | Tọa độ tính từ điểm vừa click | Ví dụ: `@100,50` |
| **TỌA ĐỘ TUYỆT ĐỐI** | `X,Y` | Tọa độ tính từ gốc gốc gốc (0,0) | Ví dụ: `100,50` |

---

### 1.2. Cơ chế truy bắt điểm hình học (Object Snap)

| Lệnh / Phím | Phím Tắt | Điểm bắt | Ứng dụng thực chiến |
| :--- | :--- | :--- | :--- |
| **OBJECT SNAP** | `F3` | Bật/Tắt truy bắt điểm chung | Tổng quản chế độ bắt điểm |
| **OSNAP SETTINGS** | `DSETTINGS` | Mở bảng cài đặt bắt điểm | Tích chọn các điểm cốt lõi thường dùng |
| **OBJECT SNAP TRACKING**| `F11` | Dóng điểm từ mốc có sẵn | Hỗ trợ dựng hình vuông góc không cần vẽ đường nháp |
| **ENDPOINT** | `Shift + Chuột phải` | Điểm đầu / Điểm cuối | Xác định mút đoạn thẳng |
| **MIDPOINT** | `Shift + Chuột phải` | Trung điểm | Điểm chính giữa đối tượng thẳng |
| **CENTER** | `Shift + Chuột phải` | Tâm hình tròn / Cung tròn | Dùng liên tục khi xác định tâm thiết bị |
| **INTERSECTION** | `Shift + Chuột phải` | Giao điểm | Điểm giao cắt giữa hai đường |
| **QUADRANT** | `Shift + Chuột phải` | 4 điểm góc đường tròn | Các điểm vị trí 0°, 90°, 180°, 270° |
| **TANGENT** | `Shift + Chuột phải` | Tiếp điểm | Vẽ đường thẳng tiếp xúc đường tròn |
| **PERPENDICULAR** | `Shift + Chuột phải` | Điểm vuông góc | Hạ đường vuông góc xuống cạnh có sẵn |
| **NEAREST** | `Shift + Chuột phải` | Điểm gần nhất trên cạnh | Bắt bám vào đường, dùng khi không cần chính xác điểm |
| **NODE** | `Shift + Chuột phải` | Điểm nút cơ sở | Dùng để bắt vào đối tượng POINT, DIVIDE |

---

### 1.3. Quản lý hiển thị hệ thống & Tỷ lệ nét vẽ (Linetype Display)

| Lệnh / Phím | Phím Tắt | Chức Năng | Ghi chú hệ thống |
| :--- | :--- | :--- | :--- |
| **PROPERTIES** | `Ctrl + 1` / `PR` | Bật bảng thuộc tính đối tượng | Sửa **Linetype Scale cục bộ** cho các nét đứt quá ngắn |
| **LTSCALE** | `LTSCALE` | Tỉ lệ nét đứt toàn bản vẽ | Giảm nhỏ hệ số (Ví dụ: `0.2`) để hiện rõ khoảng trống nét trục |
| **MSLTSCALE** | `MSLTSCALE` | Tỉ lệ nét đứt theo mác Model | Đặt bằng `1` để tự động hóa nét vẽ theo Annotation Scale |
| **PSLTSCALE** | `PSLTSCALE` | Tỉ lệ nét đứt theo Layout in | Đặt bằng `1` để đồng bộ hiển thị từ Model sang không gian in |
| **LINEWEIGHT** | `LWDISPLAY` | Hiển thị độ dày mỏng của nét | Đặt `ON` để phân biệt rõ nét đậm (biên dạng) và nét mảnh (trục) |
| **REGEN** | `RE` | Làm mới toàn bộ giao diện hình | Gõ sau khi đổi LTSCALE để cập nhật lại cấu trúc hiển thị |
| **GRID** | `F7` | Bật/Tắt lưới nền | Hỗ trợ căn tọa độ trực quan |
| **SNAP** | `F9` | Bật bước nhảy con trỏ | Nên tắt (`OFF`) để tránh hiện tượng chuột bị giật |
| **CURSORSIZE** | `CURSORSIZE` | Chỉnh độ dài crosshair con trỏ | Đặt bằng `100` để kéo dài sợi tóc vô tận, hỗ trợ dóng hình |
| **ZOOMFACTOR** | `ZOOMFACTOR` | Tốc độ phóng to thu nhỏ chuột | Giá trị tối ưu từ `60` - `100` |

[⬆️ Về đầu trang](#-mục-lục-table-of-contents)

---

<a name="group2"></a>
## ✏️ Nhóm 2: Công cụ Vẽ (Draw)

### 2.1. Nhóm cấu trúc đường và khung dựng

| Lệnh | Phím Tắt | Chức Năng | Đặc tính kỹ thuật |
| :--- | :--- | :--- | :--- |
| **LINE** | `L` | Vẽ đường thẳng rời | Tạo ra các đoạn độc lập, có thể quản lý riêng lẻ từng phân đoạn |
| **POLYLINE** | `PL` | Vẽ đa tuyến liền mạch | Tạo chuỗi đường liền khối, quản lý được độ dày (Width) của nét |
| **XLINE** | `XL` | Vẽ đường thẳng vô hạn | Đường chạy dài vô tận qua màn hình, dùng làm đường dóng dựng hình |
| **SPLINE** | `SPL` | Vẽ đường cong nội suy | Tạo các đường cong uốn lượn liên tục qua các điểm chỉ định |
| **MULTILINE** | `ML` | Vẽ các đường song song | Tạo nhanh hệ đường kép ứng dụng vẽ tường hoặc máng cáp song song |

---

### 2.2. Nhóm hình kín và tô vật liệu

| Lệnh | Phím Tắt | Chức Năng | Tham số mở rộng |
| :--- | :--- | :--- | :--- |
| **CIRCLE** | `C` | Vẽ hình tròn | Mặc định nhập Bán kính, gõ `D` để nhập Đường kính |
| **ARC** | `A` | Vẽ cung tròn | Vẽ qua 3 điểm hoặc kết hợp Tâm - Điểm đầu - Góc |
| **RECTANGLE** | `REC` | Vẽ hình chữ nhật | Gõ `F` để bo góc trước, gõ `D` để nhập kích thước dài/rộng |
| **POLYGON** | `POL` | Vẽ đa giác đều | Nhập số cạnh -> Chọn `I` (Nội tiếp) hoặc `C` (Ngoại tiếp) đường tròn |
| **ELLIPSE** | `EL` | Vẽ hình elip | Xác định trục dài và trục ngắn của hình |
| **HATCH** | `H` | Tô mặt cắt / Vật liệu | Dùng để biểu diễn mặt cắt cơ khí, vật liệu cách điện |

---

### 2.3. Nhóm quản lý điểm và chia đoạn

| Lệnh | Phím Tắt | Chức Năng | Nguyên lý hoạt động |
| :--- | :--- | :--- | :--- |
| **POINT** | `PO` | Vẽ một điểm mốc | Tạo ra một Point đơn lẻ trên tọa độ |
| **DIVIDE** | `DIV` | Chia đều đối tượng thành N phần | Nhập số phần cần chia, tự rải các điểm POINT ngăn cách |
| **MEASURE** | `ME` | Chia đối tượng theo đoạn cố định | Nhập chiều dài một đoạn, tự động chấm điểm mốc từ đầu tuyến |
| **POINT STYLE** | `PTYPE` | Thay đổi kiểu hiển thị điểm | Đổi dấu chấm nhỏ thành dấu X hoặc chữ thập để dễ nhìn thấy điểm chia |

[⬆️ Về đầu trang](#-mục-lục-table-of-contents)

---

<a name="group3"></a>
## ✂️ Nhóm 3: Công cụ Chỉnh sửa (Modify)

### 3.1. Hiệu chỉnh biên dạng & Làm sạch hình học nâng cao

| Lệnh | Phím Tắt | Chức Năng | Quy trình vận hành thực chiến |
| :--- | :--- | :--- | :--- |
| **ERASE** | `E` | Xóa đối tượng | Chọn đối tượng và gõ lệnh để xóa |
| **TRIM** | `TR` | Cắt xén phần thừa | Gõ `TR` -> Nhấn Space -> Click vào đoạn thừa để cắt bỏ |
| **EXTEND** | `EX` | Phóng đường thẳng tới đích | Gõ `EX` -> Chọn đường biên đích -> Chọn đường cần kéo dài |
| **OFFSET** | `O` | Copy tịnh tiến song song | Nhập khoảng cách ổn định -> Chọn đối tượng -> Click hướng copy |
| **FILLET** | `F` | Bo tròn góc | Gõ `F` -> Gõ `R` -> Nhập bán kính -> Chọn 2 cạnh góc |
| **CHAMFER** | `CHA` | Vát mép góc phẳng | Xác định khoảng cách vát 2 cạnh trước khi chọn góc |
| **BREAK** | `BR` | Ngắt đường tại 2 điểm | Tách một đường thẳng dài thành hai đoạn có khoảng hở |
| **JOIN** | `J` | Nối các nét rời thành khối | Gộp nhiều Line nằm thẳng hàng hoặc nối tiếp thành Polyline |
| **PEDIT** | `PE` | Sửa cấu trúc Polyline | Dùng chuyển đổi nhanh các nét Line rời rạc thành Polyline liên kết |
| **LENGTHEN** | `LEN` | **Thay đổi chiều dài đối xứng** | Gõ `LEN` -> Gõ `DE` (Delta) -> Nhập chiều dài -> Click vào đầu mút nào, đầu đó **tự động phóng dài ra/ngắn lại chính xác**. Tránh việc kéo tay lệch |
| **OVERKILL** | `OVERKILL` | **Xóa nét trùng đè tuyệt đối** | Quét toàn bộ bản vẽ -> Chạy lệnh. Tự động xóa các đường nằm đè lên nhau khít. **Bắt buộc dùng trước khi xuất file cắt CNC/Laser vỏ tủ** |
| **FLATTEN** | `FLATTEN` | **Ép phẳng cao độ về Z=0** | Khử lỗi lệch cao độ khi import hình từ 3D (SolidWorks) sang 2D. Đảm bảo các lệnh TRIM, EXTEND hoạt động chuẩn xác |

---

### 3.2. Biến đổi hình học & Sao chép mảng

| Lệnh | Phím Tắt | Chức Năng | Ghi chú |
| :--- | :--- | :--- | :--- |
| **MOVE** | `M` | Di chuyển đối tượng | Điểm gốc bắt điểm phải chuẩn |
| **COPY** | `CO` / `CP` | Sao chép đối tượng | Sao chép hàng loạt ra nhiều vị trí |
| **ROTATE** | `RO` | Xoay đối tượng quanh tâm | Gõ `R` sau khi chọn tâm nếu muốn xoay theo góc tham chiếu |
| **MIRROR** | `MI` | Lấy đối xứng đối tượng | Cần xác định 2 điểm tạo thành trục đối xứng |
| **SCALE** | `SC` | Thay đổi tỷ lệ kích thước | Nhập hệ số phóng to (>1) hoặc thu nhỏ (<1) |
| **STRETCH** | `S` | Kéo dãn một phần hình vẽ | **Bắt buộc quét chuột từ Phải sang Trái (Green Window)** bao đầu nút |
| **ARRAY** | `AR` | Sao chép theo mảng quy luật | Chế độ Rectangular (Hàng-Cột) hoặc Polar (Vòng tròn tâm) |
| **ALIGN** | `AL` | Căn chỉnh vị trí + Xoay hình | Khớp đối tượng vào vị trí chuẩn bằng cách nối các điểm mốc |
| **MATCH PROP** | `MA` | Sao chép thuộc tính | Copy Layer, màu sắc, Linetype Scale từ vật thể gốc sang vật thể đích |

[⬆️ Về đầu trang](#-mục-lục-table-of-contents)

---

<a name="group4"></a>
## 📝 Nhóm 4: Text & Ký tự đặc biệt

| Lệnh | Phím Tắt | Chức Năng | Trường hợp áp dụng |
| :--- | :--- | :--- | :--- |
| **DTEXT** | `DT` | Viết chữ đơn dòng nhanh | Phù hợp gõ ký hiệu dây, nhãn thiết bị nhỏ lẻ |
| **MTEXT** | `MT` / `T` | Viết đoạn văn bản lớn | Tạo bảng ghi chú kỹ thuật, tiêu chuẩn vận hành (hỗ trợ xuống dòng) |
| **EDIT** | `ED` | Sửa nội dung chữ | Click đúp vào chữ hoặc gõ `ED` để ghi đè số liệu |
| **TEXT STYLE** | `ST` | Khởi tạo kiểu font chữ | Cài đặt các Font kỹ thuật chuẩn như `romans.shx` hoặc `Arial` |
| **FIND** | `FIND` | Tìm kiếm & Thay thế chuỗi | Thay đổi nhanh tên linh kiện hàng loạt trên bản vẽ lớn |
| **FIELD** | `FIELD` | Chèn text động tự cập nhật | Liên kết text với diện tích, chu vi hoặc thông số biến đổi |

**Hệ thống mã gõ nhanh ký tự chuyên ngành (Nhập trực tiếp khi gõ Text):**
* `%%C` $\rightarrow$ Hiển thị ký hiệu Đường kính: **Ø**
* `%%P` $\rightarrow$ Hiển thị ký hiệu Dung sai cộng trừ: **±**
* `%%D` $\rightarrow$ Hiển thị ký hiệu Độ: **°**
* `%%U` $\rightarrow$ Kích hoạt chế độ **Gạch chân văn bản**

[⬆️ Về đầu trang](#-mục-lục-table-of-contents)

---

<a name="group5"></a>
## 📏 Nhóm 5: Kích thước & Đường tâm (Dimension & Axes)

### 5.1. Hệ thống lệnh đo kích thước hình học

| Lệnh | Phím Tắt | Loại đường đo | Ghi chú thực chiến |
| :--- | :--- | :--- | :--- |
| **LINEAR** | `DLI` | Đo thẳng đứng hoặc nằm ngang | Luôn khóa theo trục X hoặc Y |
| **ALIGNED** | `DAL` | Đo đường chéo nghiêng | Đo song song với cạnh nghiêng của vật thể |
| **CONTINUE** | `DCO` | Đo chuỗi nối tiếp liên tục | Tạo hàng kích thước thẳng hàng, phải có 1 đường Dim mốc trước |
| **RADIUS** | `DRA` | Đo bán kính đường tròn/cung | Ký hiệu chữ **R** tự động thêm phía trước |
| **DIAMETER** | `DDI` | Đo đường kính | Ký hiệu **Ø** tự động thêm phía trước |
| **ANGULAR** | `DAN` | Đo góc giữa 2 đường thẳng | Hiển thị giá trị độ (°), phút, giây |
| **DIMSTYLE** | `D` | Cài đặt cấu trúc đường đo | Quản lý cỡ chữ, kiểu mũi tên, số chữ số thập phân sau dấu phẩy |
| **BASELINE** | `DBA` | Đo phân tầng từ một gốc | Các đường kích thước xếp chồng lên nhau tính từ một mốc cố định |
| **DIMEDIT** | `DED` | Hiệu chỉnh chữ số kích thước | Nghiêng đường gióng hoặc ghi đè nội dung ký hiệu đặc biệt |

---

### 5.2. Công cụ quản lý và vẽ đường tâm tự động (Centerlines)
*Tiêu chuẩn hóa trục đối xứng cho chi tiết cơ khí, vị trí lỗ nút nhấn mặt tủ điện.*

> 📌 **QUY TRÌNH SETUP TRỤC TỰ ĐỘNG CHUẨN:**
> 1. Thiết lập khoảng trục thừa ra ngoài bằng biến `CENTEREXE`.
> 2. Đóng đinh layer lưu trữ nét trục bằng biến `CENTERLAYER`.
> 3. Triển khai vẽ trục tự động bằng lệnh `CL` hoặc `CM` để đảm bảo cân đối tuyệt đối.

| Lệnh / Biến hệ thống | Phím Tắt | Bản chất công cụ | Hướng dẫn vận hành nhanh |
| :--- | :--- | :--- | :--- |
| **CENTERLINE** | `CL` | Tạo trục giữa **2 đường thẳng** | Gõ `CL` -> Chọn cạnh biên 1 -> Chọn cạnh biên 2. Trục tự động sinh ở tâm và nhô đều ra 2 đầu. |
| **CENTERMARK** | `CM` | Tạo dấu chữ thập tâm **đường tròn**| Gõ `CM` -> Click trực tiếp vào biên đường tròn. Tự sinh hệ trục vuông góc đi qua tâm hình. |
| **CENTEREXE** | `CENTEREXE` | Cài đặt khoảng cách nhô trục | Nhập số đơn vị muốn phần nét trục thò ra ngoài biên vật thể (Ví dụ: `3` hoặc `5`). |
| **CENTERLAYER** | `CENTERLAYER` | Tự động hóa phân lớp Layer trục | Nhập chính xác tên Layer chứa nét trục (Ví dụ: `Net_Truc`). Hệ thống tự chuyển đường tâm về layer này khi vẽ. |

[⬆️ Về đầu trang](#-mục-lục-table-of-contents)

---

<a name="group6"></a>
## 📦 Nhóm 6: Block & Quản lý Layer nâng cao

### 6.1. Quản lý cấu trúc Khối (Block) & Thuộc tính

| Lệnh | Phím Tắt | Chức Năng | Lưu ý vận hành |
| :--- | :--- | :--- | :--- |
| **BLOCK** | `B` | Đóng gói đối tượng thành khối | Gom nhóm các nét vẽ rời thành 1 khối để tái sử dụng linh kiện |
| **WBLOCK** | `WB` | Xuất Block thành file CAD độc lập | Lưu trữ linh kiện thành thư viện dùng cho nhiều bản vẽ khác nhau |
| **INSERT** | `I` | Gọi Block từ thư viện ra bản vẽ | Lấy linh kiện ra dùng nhanh |
| **EXPLODE** | `X` | **Phá khối / Rã liên kết động** | Phá vỡ Block thành nét thường, hoặc **rã liên kết động của hệ lệnh `CM`/`CL`** để tùy ý xóa nét dọc/ngang thừa. |
| **PASTEBLOCK** | `Ctrl+Shift+V` | Dán nhanh cụm nét thành Block | Tạo nhanh block tạm không cần đặt tên |
| **REFEDIT** | `REF` | Sửa khối trực tiếp tại chỗ | Chỉnh sửa nội dung block ngay trên giao diện tổng |
| **BEDIT** | `BE` | Mở môi trường thiết kế Block Editor| Xây dựng Dynamic Block (Khối động biến đổi thông minh) |
| **ATTDEF** | `ATTDEF` | Tạo biến thuộc tính chữ cho Block | Ứng dụng làm khung tên tự động điền hoặc ký hiệu số chân linh kiện |
| **EATTEDIT** | `EATTEDIT` | Sửa nhanh nội dung biến thuộc tính | Thay đổi thông tin chữ trong Block thuộc tính bằng bảng nhập liệu |
| **BATTMAN** | `BATTMAN` | Quản lý đồng bộ thuộc tính | Cập nhật các thay đổi cấu trúc thuộc tính cho toàn bộ Block trên bản vẽ |

---

### 6.2. Kiểm soát hệ thống Layer chuyên sâu & Không gian in

| Lệnh | Phím Tắt | Ý nghĩa thực chiến | Ứng dụng thực tế |
| :--- | :--- | :--- | :--- |
| **LAYER** | `LA` | Bật bảng quản lý Layer tổng | Khởi tạo màu, độ dày, kiểu đường cho toàn bộ hệ thống |
| **LAYISO** | `LAYISO` | **Cô lập duy nhất Layer được chọn** | Ẩn toàn bộ mọi thứ, chỉ giữ lại duy nhất layer vừa click. Cực kỳ hữu ích khi cần rà soát lại riêng mạch dây điện tín hiệu. |
| **LAYUNISO**| `LAYUNISO`| Hủy bỏ trạng thái cô lập | Bật lại toàn bộ các Layer về trạng thái hiển thị bình thường |
| **LAYOFF** | `LAYOFF` | Tắt nhanh Layer bằng cách chọn vật thể| Click trực tiếp vào hình vẽ nào trên màn hình, layer chứa hình đó lập tức tắt đi |
| **XREF** | `XR` | Quản lý bản vẽ tham chiếu ngoài | Nhúng bản vẽ nền kiến trúc/cơ khí vào mà không làm nặng file hiện tại |
| **LAYOUT** | `LAYOUT` | Quản lý không gian bản vẽ in ấn | Thiết lập các trang giấy định hình trước khi xuất hồ sơ |
| **MVIEW** | `MV` | Tạo cửa sổ hiển thị (Viewport) | Mở cổng nhìn từ không gian giấy Layout xuyên về không gian Model |
| **PAGESETUP**| `PAGESETUP`| Cấu hình thông số trang in | Thiết lập khổ giấy, nét in đen trắng (monochrome) cho Layout |
| **PLOT** | `Ctrl + P` | Xuất bản vẽ | Xuất file CAD sang định dạng PDF hoặc đẩy lệnh ra máy in vật lý |

[⬆️ Về đầu trang](#-mục-lục-table-of-contents)

---

<a name="group7"></a>
## 🔍 Nhóm 7: Thống kê & Lọc dữ liệu thông minh

### 7.1. Lọc thuộc tính nâng cao (Data Selection)

| Lệnh | Phím Tắt | Bản chất công nghệ | Cách ứng dụng |
| :--- | :--- | :--- | :--- |
| **QUICK SELECT**| `QSELECT` | **Lọc tìm đối tượng hàng loạt theo dữ liệu** | Bật bảng lọc. Cho phép chọn toàn bộ các đường tròn có cùng bán kính $R=3mm$, hoặc toàn bộ Block mang tên `Aptomat_3P` trong 1 giây để sửa thông số. Không nhặt tay. |

---

### 7.2. Điều hướng góc nhìn & Chuẩn đoán sửa lỗi file

| Lệnh | Phím Tắt | Chức Năng | Tình huống áp dụng |
| :--- | :--- | :--- | :--- |
| **ZOOM EXTENTS**| `Z` -> `E` | Thu toàn bộ hình vẽ vừa vặn màn hình | Tìm lại hình khi bị lạc trôi xa tọa độ gốc |
| **ZOOM WINDOW** | `Z` -> `W` | Phóng to khu vực quét chuột | Tập trung quan sát một cụm chi tiết nhỏ |
| **PAN** | Giữ chuột giữa | Kéo di chuyển vùng quan sát bản vẽ | Di chuyển góc nhìn không làm thay đổi tọa độ |
| **DISTANCE** | `DI` | Đo kiểm tra nhanh kích thước hình | Xem nhanh khoảng cách giữa 2 điểm mà không cần ép đường Dim cố định |
| **AREA** | `AA` | Tính nhanh diện tích và chu vi | Quét biên dạng kín để bóc tách thông số |
| **LIST** | `LI` | Bóc tách toàn bộ thông số đối tượng | Hiển thị chi tiết ID, Layer, Tọa độ, Chiều dài của phần tử được chọn |
| **PURGE** | `PU` | **Dọn sạch rác file bản vẽ** | Quét sạch các Layer trống, Block rác không dùng. Giảm dung lượng file tối đa, làm nhẹ máy |
| **AUDIT** | `AUDIT` | Quét dọn và sửa lỗi cấu trúc file | Sửa các lỗi crash file ngầm do xung đột phần mềm |
| **UNDO / REDO** | `U` / `REDO` | Quay lại hoặc tiến tới thao tác | Khôi phục lại trạng thái lệnh trước đó |

[⬆️ Về đầu trang](#-mục-lục-table-of-contents)

---

<a name="dexuat"></a>
## 💡 Mục đề xuất tham khảo

### Lộ trình 4 giai đoạn làm chủ AutoCAD trong lập trình Nhúng & Tự động hóa:
* **Giai đoạn 1 (Làm chủ biên dạng cơ bản):** `LINE`, `CIRCLE`, `RECTANGLE`, `ARC`, `TRIM`, `OFFSET`. (Đủ dựng bao che, hình học thô robot).
* **Giai đoạn 2 (Chuẩn hóa tự động hình học):** `PLINE`, `POLYGON`, `FILLET`, `CHAMFER`, `ARRAY`, **`CENTERLINE`**, **`CENTERMARK`**, `LENGTHEN`. (Xử lý chi tiết lắp ráp, đục lỗ nút nhấn mặt tủ điện).
* **Giai đoạn 3 (Quản lý dữ liệu & Làm sạch hệ thống):** `LAYER`, **`LAYISO`**, **`LAYOFF`**, `BLOCK`, **`OVERKILL`**, **`FLATTEN`**, **`QSELECT`**. (Bóc tách sơ đồ mạch điện Smart Home đa tầng, xử lý file xuất CNC vỏ hộp máy).
* **Giai đoạn 4 (Đóng gói sản phẩm đầu ra):** `TEXT`, `DIMSTYLE`, `LAYOUT`, `VIEWPORT`, `PLOT`. (Xuất hồ sơ đồ án tốt nghiệp, tài liệu chuyển giao kỹ thuật).

---
*Created by Clement - 2026* *Bản hoàn chỉnh nhất: Tích hợp đầy đủ tư duy Quản lý dữ liệu (Data-Driven) và Tự động hóa kết cấu trục đối xứng kỹ thuật.*
