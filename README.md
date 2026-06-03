# Đồ án Môn học: Kho dữ liệu và OLAP (Data Warehouse & OLAP)
**Mã môn học:** IS217.Q11  
**Đề tài:** Hệ thống Kho dữ liệu (Data Warehouse), Phân tích OLAP và Khai phá dữ liệu Điện ảnh (TMDB Movie Dataset)

---

## 📝 Giới thiệu dự án
Dự án này tập trung vào việc xây dựng một hệ thống Kho dữ liệu toàn diện từ nguồn dữ liệu điện ảnh TMDB. Quy trình thực hiện bao gồm các giai đoạn:
1. **ETL (Extract - Transform - Load):** Sử dụng công cụ SSIS để làm sạch, biến đổi và nạp dữ liệu thô vào Data Warehouse.
2. **Xây dựng Data Warehouse:** Thiết kế mô hình dữ liệu (hình sao/bông tuyết) tối ưu cho việc truy vấn báo cáo.
3. **Phân tích OLAP (SSAS & MDX):** Thiết kế các cấu trúc Cube, Dimensions, Measures và viết các câu truy vấn nâng cao bằng MDX.
4. **Trực quan hóa dữ liệu (BI Dashboard):** Xây dựng các báo cáo phân tích đa chiều thông qua Power BI, Looker và Excel Pivot.
5. **Khai phá dữ liệu (Data Mining):** Ứng dụng các thuật toán khai phá dữ liệu trên Python để tìm kiếm tri thức ẩn.

---

## 👥 Thành viên thực hiện
| STT |     Họ và Tên     | Mã số Sinh viên |

|  1  | Phạm Nhật Khoa    |    23520753     |

|  2  | Lê Nguyễn Thúy An |    23520009     |


---

## 📁 Cấu trúc thư mục dự án
Kho chứa này được tổ chức theo các phân mục chức năng như sau:

📂 **Data_ original dataset/**: Chứa tập dữ liệu thô ban đầu và các tập dữ liệu đã qua xử lý chuẩn bị cho phân tích.  
📂 **Database_ warehouse database (_.mdf, _.ldf)/**: Chứa file cơ sở dữ liệu Kho dữ liệu (đã được nén thành `.rar` để đảm bảo hiệu năng lưu trữ).  
📂 **Slide trình bày đồ án môn học/**: Slide PowerPoint và PDF phục vụ cho việc thuyết trình báo cáo trước giảng viên.  
📂 **Source_ SSIS project, SSAS project, Excel Pivot file, MDX, Looker, Power BI, data mining project/**: Thư mục cốt lõi chứa toàn bộ mã nguồn của đồ án:
- Dự án ETL (SSIS) & Thiết kế OLAP Cube (SSAS).
- Các câu lệnh truy vấn phân tích chuyên sâu (`MDX_Query.mdx`).
- File thiết kế báo cáo trực quan (`.pbix`, Looker, Excel Pivot).
- Mã nguồn phân tích khai phá dữ liệu (`.ipynb`, `.html`).

📂 **Text file_ the information of group (member name, job)/**: Thông tin chi tiết về bảng phân công công việc của nhóm.

---

## 🛠 Công nghệ & Công cụ sử dụng
- **Hệ quản trị CSDL:** Microsoft SQL Server
- **Công cụ tích hợp & Phân tích:** SQL Server Integration Services (SSIS), SQL Server Analysis Services (SSAS)
- **Ngôn ngữ truy vấn:** T-SQL, MDX (Multi-Dimensional Expressions)
- **Trực quan hóa (BI Tools):** Power BI, Looker Studio, Microsoft Excel Pivot Table
- **Khai phá dữ liệu:** Python (Jupyter Notebook, Pandas, Scikit-learn)

---

## 🔗 Liên kết tải dữ liệu lớn (Large Files Backup)
Do quy định giới hạn dung lượng của GitHub, một số file dữ liệu thô gốc (`.csv` > 500MB) và file báo cáo chi tiết không thể đẩy trực tiếp lên kho chứa này. Nhóm đã sao lưu toàn bộ phiên bản đầy đủ tại đường link dưới đây:

👉 **[[Bấm vào đây để tải Dataset gốc (Kaggle)]](https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies)**  
👉 **[[Bấm vào đây để tải Báo cáo đầy đủ (Google Drive)]](https://docs.google.com/document/d/11mu0VT6AdEWilfDGRYg95d9LCZizHExI/edit?usp=sharing&ouid=113799970762456408969&rtpof=true&sd=true)**

---

## 🚀 Hướng dẫn triển khai dự án (Deployment)
1. **Khôi phục Database:** Tải file trong thư mục `Database_ warehouse database`, giải nén và `Attach` file `.mdf` vào SQL Server của bạn.
2. **Chạy gói ETL:** Mở công cụ Visual Studio, import project `TMDB_MOVIE_SSIS` để xem hoặc thực thi lại quy trình làm sạch dữ liệu.
3. **Triển khai Cube:** Mở project `TMDB_Movie_SSAS` trong Visual Studio, cấu hình lại `Data Source` trỏ về SQL Server của bạn, sau đó thực hiện `Process` và `Deploy` khối Cube lên Analysis Services server.
4. **Xem báo cáo:** Sử dụng Power BI Desktop để mở file `REPORT POWER BI.pbix` hoặc Excel để mở các file Pivot mẫu nhằm tương tác với dữ liệu.
