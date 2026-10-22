# HƯỚNG DẪN CHẠY DỰ ÁN LAB 04
**Môn học:** Học máy (Machine Learning)  
**Sinh viên:** Nguyễn Đức Duy - MSSV: 65130628

---

## 1. Kích hoạt môi trường ảo (Virtual Environment)
Mở Terminal tại thư mục gốc của dự án (`Lab01_65130628_NguyenDucDuy`) và chạy:

```bash
# Trên macOS / Linux:
source ml_lab_env/bin/activate
```

*(Nếu cài đặt mới trên máy khác, chỉ cần chạy: `pip install -r requirements.txt`)*

---

## 2. Các cách chạy thực nghiệm

### Cách 1: Sử dụng JupyterLab (Khuyên dùng theo đề bài)
1. Trong terminal đã kích hoạt môi trường, khởi động JupyterLab:
   ```bash
   jupyter lab
   ```
2. Trình duyệt sẽ tự động mở giao diện JupyterLab.
3. Điều hướng vào thư mục `notebooks/`:
   * Mở `01_linear_regression.ipynb` (Hồi quy tuyến tính - Dự đoán giá nhà)
   * Mở `02_logistic_regression.ipynb` (Hồi quy Logistic - Chẩn đoán tiểu đường)
4. Trên thanh công cụ, chọn **Run -> Run All Cells** để thực thi lại toàn bộ và quan sát kết quả.

---

### Cách 2: Mở và chạy trực tiếp trên VS Code / Cursor
1. Mở thư mục dự án trong VS Code.
2. Mở tệp notebook trong thư mục `notebooks/`.
3. Nhấp vào nút **Select Kernel** ở góc trên cùng bên phải và chọn môi trường:
   `Python (ml_lab_env) ./ml_lab_env/bin/python`
4. Bấm **Run All** để chạy từng cell.

---

### Cách 3: Tự động chạy và xuất toàn bộ kết quả qua dòng lệnh (CLI)
Nếu muốn chạy lại toàn bộ notebook và cập nhật trực tiếp output:

```bash
./ml_lab_env/bin/python run_notebooks_and_populate.py
```

Nếu muốn chạy lại việc xuất các biểu đồ và tập dữ liệu tiền xử lý:
```bash
./ml_lab_env/bin/python -c "
import generate_report_pdf
generate_report_pdf.create_report()
"
```

---

## 3. Xem báo cáo thu hoạch
* Tệp PDF chính thức: `reports/Bao_cao_Lab04_65130628.pdf`
* Tệp Markdown: `reports/Bao_cao_Lab04_65130628.md`
