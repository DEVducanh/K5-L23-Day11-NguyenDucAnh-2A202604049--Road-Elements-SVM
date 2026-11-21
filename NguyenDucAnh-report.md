# Báo cáo cá nhân — Ngày 11

Họ tên: Nguyen Duc Anh    Mã học viên: 2A202604049  
Phiên bản CVAT (Help → About): **cần điền từ CVAT**  
Guideline: Road v1.0    Lần nộp (`revision` trong manifest): 3  
Thời điểm export (manifest UTC): 2026-11-21 09:49 UTC    Số lần nộp lại sau Rework: **xác nhận**

## 1. Kiểm project

| Mục | Đúng như guideline Road v1.0? | Ghi chú |
| --- | --- | --- |
| 6 label, đúng kiểu | Kiểm tra trong Project → Labels | Export nhận diện đủ sáu tên label; cần ảnh chụp tab Labels |
| Thuộc tính và giá trị | Kiểm tra trong Project → Labels | Taxonomy trong repo khớp Road v1.0; cần xác nhận project CVAT và chụp màn hình |
| 4 tag ảnh | Có trong export | Lint đọc đủ bốn tag ở 20/20 ảnh; cần ảnh chụp tab Labels |

Cách kết thúc polyline trên bản CVAT này: **điền sau khi xác nhận trong CVAT**  
Cách đặt tag ảnh trên bản CVAT này: **điền sau khi xác nhận trong CVAT**

## 2. Số lượng đã gán

| Task | Ảnh | lane | road_curb | crosswalk | drivable | traffic_light | traffic_sign |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| front | 12 | 23 | 6 | 7 | 22 | 13 | 9 |
| front-extra | 0 / 4 | 0 | 0 | 0 | 0 | 0 | 0 |
| fisheye | 8 | 3 | 3 | 9 | 1 | 2 | 2 |
| fisheye-extra | 0 / 4 | 0 | 0 | 0 | 0 | 0 | 0 |

## 3. Bảng ca khó

| Ảnh | Nhãn | Phân vân giữa | Đã chọn | Lý do |
| --- | --- | --- | --- | --- |
| **Bổ sung các ca khó thực tế nếu có** |  |  |  |  |

## 4. Phiếu QC 1 nhận được

Bạn kiểm lô của tôi: **điền tên bạn kiểm**    Quyết định nhận được: **điền sau khi nhận phiếu**

| Mã lỗi | Số lỗi | Đồng ý? | Đã sửa? |
| --- | ---: | --- | --- |
| **Điền theo phiếu nhận được** |  |  |  |

## 5. Kiểm file export

| File | Mở lại được? | Shape ảnh 1 (job / file) | Shape ảnh 2 (job / file) | Tag camera có trong XML? |
| --- | --- | --- | --- | --- |
| NguyenDucAnh_front.zip | Có, lint đọc được XML; không kèm ảnh | **Đối chiếu CVAT job** | **Đối chiếu CVAT job** | Có |
| NguyenDucAnh_fisheye.zip | Có, lint đọc được XML; không kèm ảnh | **Đối chiếu CVAT job** | **Đối chiếu CVAT job** | Có |

## 6. Ảnh chụp màn hình

1. **Cần chụp:** tab Labels của project.
2. **Cần chụp:** một ảnh camera trước đã gán đủ.
3. **Cần chụp:** một ảnh fisheye đã gán, phóng to polyline cong.
4. **Cần chụp:** đoạn XML có `<polyline label="lane">`.

## 7. Tự đánh giá

Lỗi bạn mắc nhiều nhất hôm nay (theo mã QC1-xx), và cách tránh ở Ngày 20: **điền sau khi nhận phiếu QC**  
Nhãn của bạn đi vào model ở đâu? Chọn một lỗi đã sửa và nói nó làm model học sai thế nào: **điền một lỗi thực tế đã sửa**

## 8. (Tùy chọn, buffer) Từ polyline đến đích row-anchor

Bỏ qua nếu không làm hoạt động buffer.
