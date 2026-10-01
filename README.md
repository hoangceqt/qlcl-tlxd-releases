# QLCL TLXD — bản phát hành

Phần mềm quản lý chất lượng, hồ sơ nghiệm thu công trình xây dựng.
Kho này **chỉ chứa bản phát hành**; mã nguồn ở kho riêng.

## Cài mới

Vào [Release mới nhất](https://github.com/hoangceqt/qlcl-tlxd-releases/releases/latest),
tải `QLCL-TLXD-Setup-<số>-<ngày>.exe`, chạy bằng quyền quản trị. Cài xong mở trình duyệt
vào `http://localhost:4000`.

Bộ cài đã có sẵn cơ sở dữ liệu và thư viện định mức — không cần cài thêm gì.

## Cập nhật

Máy đã cài **tự thấy bản mới**: phần mềm hiện dải "Có bản mới", bấm **Cập nhật ngay** là
xong. Dữ liệu được sao lưu trước khi cập nhật.

Máy không có mạng: chép ba tệp của một Release (`.exe`, `.zip`, `ban-cai.json`) vào một
thư mục (USB, máy văn phòng) và trỏ nguồn cập nhật vào đó
(`QLCL_NGUON_CAP_NHAT` trong tệp `.env` ở thư mục cài).

## Mỗi Release có ba tệp

| Tệp | Dùng khi |
|---|---|
| `QLCL-TLXD-Setup-….exe` | cài mới, hoặc bản mới đổi thư viện máy chủ |
| `QLCL-TLXD-BanVa-….zip` | cập nhật thường — chỉ thay phần mềm, vài MB |
| `ban-cai.json` | máy đã cài đọc tệp này để biết có bản mới và tải tệp nào |

Mã SHA-256 của từng tệp ghi trong `ban-cai.json` và trong ghi chú Release; phần mềm kiểm
mã băm trước khi áp, tệp hỏng hay bị đổi thì bỏ.
