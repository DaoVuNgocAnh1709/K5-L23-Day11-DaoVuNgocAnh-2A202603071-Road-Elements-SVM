# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): doanquangminh        Người kiểm (học viên): daovungocanh (Đào Vũ Ngọc Anh)  
Ngày: 2026-11-21                          Phiên bản guideline: Road v1.0  
File được kiểm (tên + `revision` trong manifest): doanquangminh-front.zip, doanquangminh-fisheye.zip (rev 1)  
Số ảnh kiểm: 6 (+ 0 ảnh thêm, ghi riêng)   Số nhãn đã kiểm (shape + tag): 80  

## Tổng hợp theo mã
| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | 24 | 0 | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | 12 | 1 | nặng |
| QC1-03 position | sai thuộc tính / thừa | 16 | 1 | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | 16 | 0 | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | 8 | 0 | chính |
| QC1-06 style, color, kind | sai thuộc tính | 16 | 0 | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | 14 | 0 | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | 26 | 0 | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | 10 | 0 | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | 10 | 0 | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | 9 | 0 | chính |
| QC1-12 file | lỗi file | 4 | 1 | nhẹ / nặng |

## Danh sách lỗi (mỗi lỗi một dòng)
| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| 1 | QC1-03 | A09 | lane (x≈523..672) | nặng | Vạch mép phải làn xe chạy bị gán nhầm thuộc tính `position: L1` thay vì `R1`. |
| 2 | QC1-02 | A09 | lane | nặng | Do vạch phải bị gán thành L1 nên ảnh A09 bị thiếu vạch `R1` (kéo theo từ lỗi QC1-03). |
| 3 | QC1-12 | Chung | format nộp | nhẹ | Đang xuất thành 4 file zip riêng (`*-extra.zip`). Nên gộp task thường và extra vào đúng 2 file zip theo đặc tả SUBMISSION (`doanquangminh-front.zip` 16 ảnh và `doanquangminh-fisheye.zip` 12 ảnh). |

## Ca mơ hồ
| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A06 | Ảnh A06 không vẽ vạch R1 do vạch sơn bên phải bị mờ hoàn toàn ở ngã tư. | Đồng ý chấp nhận miễn trừ theo quy tắc ca khó của guideline Road v1.0. |

## Quyết định
Lỗi nặng: 1 (do lỗi gán nhầm position ở A09 kéo theo thiếu R1)   Lỗi chính: 0 / 80 nhãn = 0.0%   Lỗi nhẹ: 1   Ca chờ lead: 0  
Quyết định (Release / Hold / Rework): Rework  
Lý do (theo luật của phiếu): Ảnh A09 bị nhầm thuộc tính `position` giữa L1 và R1 (lỗi nặng theo bảng phân mức lỗi), và cần gộp file nộp theo đúng chuẩn 2 file zip của môn học. Bạn chỉ cần sửa thuộc tính của vạch này thành R1 trên CVAT rồi xuất lại là đạt Release!

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); "sai thuộc tính" và "lỗi file" là khóa học thêm. Cách xếp mức: [thang mức lỗi](docs/qc_severity_road_v1.0.md).
