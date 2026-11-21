# Báo cáo cá nhân — Ngày 11

Họ tên: Nguyen Duc Anh    Mã học viên: 2A202604049  
Phiên bản CVAT (Help → About): chưa ghi nhận trong repo  
Guideline: Road v1.0    Lần nộp (`revision` trong manifest): 3  
Thời điểm export (manifest UTC): 2026-11-21 09:49 UTC    Số lần nộp lại sau Rework: 2 lần sau bản đầu (manifest revision 3)

## 1. Kiểm project

| Mục | Đúng như guideline Road v1.0? | Ghi chú |
| --- | --- | --- |
| 6 label, đúng kiểu | Đúng theo cấu trúc export đã lint | lane, road_curb, crosswalk, drivable, traffic_light, traffic_sign |
| Thuộc tính và giá trị | Đúng theo cấu trúc export đã lint | Taxonomy export khớp tên label và giá trị Road v1.0 |
| 4 tag ảnh | Đủ trong export | Lint đọc được đủ 4 tag trên cả 20 ảnh; camera khớp tên file |

Cách kết thúc polyline trên bản CVAT này: chưa ghi nhận.  
Cách đặt tag ảnh trên bản CVAT này: từng ảnh có bốn tag trong export.

## 2. Số lượng đã gán

| Task | Ảnh | lane | road_curb | crosswalk | drivable | traffic_light | traffic_sign |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| front | 12 | 23 | 6 | 7 | 22 | 13 | 9 |
| front-extra | 0 / 4 | 0 | 0 | 0 | 0 | 0 | 0 |
| fisheye | 8 | 3 | 3 | 9 | 1 | 2 | 2 |
| fisheye-extra | 0 / 4 | 0 | 0 | 0 | 0 | 0 | 0 |

## 3. Bảng ca khó

Chưa có ghi chú ca khó được lưu trong repo.

| Ảnh | Nhãn | Phân vân giữa | Đã chọn | Lý do |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

## 4. Phiếu QC 1 nhận được

Chưa có phiếu QC 1 từ bạn kiểm trong repo.

| Mã lỗi | Số lỗi | Đồng ý? | Đã sửa? |
| --- | ---: | --- | --- |
|  |  |  |  |

## 5. Kiểm file export

Hai ZIP mở được bằng `road_check lint`, đúng cấu trúc CVAT for images 1.1 và không kèm ảnh. Shape count đầu hai ảnh lấy từ XML; so sánh với số trong CVAT job chưa được ghi nhận.

| File | Mở lại được? | Shape ảnh 1 (job / file) | Shape ảnh 2 (job / file) | Tag camera có trong XML? |
| --- | --- | ---: | ---: | --- |
| NguyenDucAnh_front.zip | Có / Có | chưa ghi / 7 | chưa ghi / 6 | Có |
| NguyenDucAnh_fisheye.zip | Có / Có | chưa ghi / 1 | chưa ghi / 4 | Có |

Lint hiện còn 6 cảnh báo nặng và 9 cảnh báo chính; xem `NguyenDucAnh-lint.txt` trong thư mục dự án.

## 6. Ảnh chụp màn hình

Ảnh chụp CVAT không có trong repo tại thời điểm đóng gói:

1. Tab Labels của project.
2. Một ảnh camera trước đã gán đủ.
3. Một ảnh fisheye đã gán, phóng to polyline cong.
4. Đoạn XML có `<polyline label="lane">`.

## 7. Tự đánh giá

Lỗi được lint nhắc nhiều nhất là QC1-02 (thiếu L1/R1); cần xác nhận trực tiếp trên ảnh, không vẽ thêm nếu vạch không nhìn thấy. Để tránh lặp lại, self-QC từng ảnh và kiểm riêng L1/R1 trước export.

Polyline bị đảo chiều có thể làm sai thứ tự điểm gần/xa mà model học từ đường làn. Nên bắt đầu vẽ sát xe rồi đi ra xa, sau đó rà chiều từng đường trước export.

## 8. (Tùy chọn, buffer) Từ polyline đến đích row-anchor

Không thực hiện.
