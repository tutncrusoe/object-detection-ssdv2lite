1. Tải dữ liệu VOC2007 (bao gồm trainval + test) (http://host.robots.ox.ac.uk/pascal/VOC/voc2007/index.html) + giải nén; trong đó:

- anotation: chứa nhãn dữ liệu;
- imageset/Main : chứa thông tin hình ảnh thuộc tập train/val/test;
- JPEGImages: chứa toàn bộ dữ liệu.
- vậy là chúng ta đã hoàn tất xong phần chuẩn bị cho bộ dữ liệu huấn luyện object-detection datatype==voc

2. Tạo thư mục Object_Detection:

- chứa file pretrain_colab.ipynb và readme (anh Huy gửi)
- Mở file pretrain_colab.ipynb
- Cài đặt các thư viện cần thiết trên ggcolab.
- Import ggDrive vào ggcolab. (sau khi import hoàn tất mới xuất hiện thư mục drive bên tay trái).
- Mở thư mục Object_Detection để theo dõi.

3. git clone https://github.com/qfgaohao/pytorch-ssd.git (anh đã clone rồi nên không cần thiết chạy lại) => pytorch-ssd đã được tải về.
   -Tạo thư mục pytorch-ssd/data (anh cũng đã tạo rồi)
   -Upload "VOC2007_trainval.zip" and "VOC2007_test.zip" vào thư mục pytorch-ssd/data/ va` giai ne'n.

4. Tải nhãn voc-model-labels.txt (chứa tất cả các classes có sẵn) vào thư mục models. Done.

5. Download pre-trained model mb2-ssd-lite-mp-0_686.pth (Ở đây chúng ta train v2 nên chỉ quan tâm V2)
6. Huấn luyện ssd-v2-lite. (khai báo đúng đường dẫn "data/VOC2007_trainval", "data/VOC2007_test", "models/mb2-ssd-lite-mp-0_686.pth",
7. Khởi động tiếp quá trình train (dành cho đang train nhưng timeup colab).

- khai báo --resume=models/mb2-ssd-lite-Epoch-0-Loss-5.2631532115321.pth (tương ứng với epoch finally)
  có thể điều chỉnh batch_size cho phù hợp.

8. Test images
   tạo thư mục test_images => upload images to test
   khai báo đường dẫn theo --help
   phát sinh lỗi như hình => cách sửa lỗi như sau: mở file run_ssd_sample.py
   9.Done.
