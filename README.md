# Admission Edge HSA Strategy 2026

Web tĩnh hỗ trợ tra cứu và quy đổi điểm HSA/THPT theo phương pháp bách phân vị, đối chiếu điểm chuẩn 2023–2025 và mô phỏng chiến thuật tuyển sinh 2026.

## Tính năng chính

- Chọn trường, phương thức xét tuyển và nhập điểm đầu vào.
- Quy đổi điểm HSA theo phương pháp bách phân vị.
- Tách riêng công thức theo từng trường:
  - QHI/UET, QHT/HUS: bảng quy đổi tương đương VNU-IDT theo A00, B00, C00, D01.
  - BVH/PTIT: nội suy tuyến tính theo bảng quy đổi HSA riêng của PTIT.
  - KHA/NEU: nội suy tuyến tính theo bảng quy đổi HSA riêng của NEU.
  - YHB/HMU: giữ riêng theo THPT, không gán HSA nếu chưa có bảng chính thức.
- Đối chiếu điểm chuẩn các năm gần đây.
- Phân loại khả năng: Khả năng đỗ cao, Có cơ hội tốt, Sát điểm chuẩn, Cần cân nhắc, Chưa đủ điểm.
- Có tab kiểm tra công thức để rà soát kết quả mẫu.
- Chạy offline, không cần backend, không cần thư viện ngoài.

## Cấu trúc dự án

```text
admission-edge-hsa-2026/
├── index.html
├── 404.html
├── README.md
├── LICENSE
├── .gitignore
├── .nojekyll
├── package.json
├── docs/
│   ├── DEPLOY_GITHUB.md
│   └── FORMULA_NOTES.md
├── data/
│   └── SOURCES.md
└── .github/
    └── workflows/
        └── pages.yml
```

## Chạy thử trên máy

Cách nhanh nhất:

```bash
python -m http.server 5173
```

Sau đó mở:

```text
http://localhost:5173
```

Hoặc mở trực tiếp file `index.html` bằng trình duyệt Microsoft Edge/Chrome.

## Đưa lên GitHub

```bash
git init
git add .
git commit -m "Initial Admission Edge HSA 2026 web app"
git branch -M main
git remote add origin https://github.com/<ten-tai-khoan>/<ten-repo>.git
git push -u origin main
```

Sau đó bật GitHub Pages theo hướng dẫn trong `docs/DEPLOY_GITHUB.md`.

## Ghi chú dữ liệu

Dữ liệu tuyển sinh có thể thay đổi theo từng năm và từng đề án của trường. Web ưu tiên hiển thị “—” với dữ liệu chưa xác minh, thay vì tự suy đoán số liệu.

## Bản quyền

Mặc định: All rights reserved. Có thể thay đổi giấy phép trong file `LICENSE` nếu muốn công khai mã nguồn theo MIT/GPL/Apache.
