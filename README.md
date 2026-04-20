# Lưu ý quan trọng

- Tối **2026-04-19**, tôi đã submit kết quả bằng phương pháp **ensemble**, nhưng **quên lưu weight của model #2**. Vì vậy **hôm nay 2026-04-20** khi chạy lại pipeline, tôi phải **train lại riêng model #2**. Kết quả ensemble với model train lại có thể **sai lệch nhỏ** so với bản submit trước.

- Trong notebook train ban đầu, tôi có lưu **training log** thể hiện đầy đủ quá trình **train** và **inference**. Ban giám khảo có thể tham khảo tại:  
  - [`effvs2-27e-b0-13e-mass-aug.ipynb`](effvs2-27e-b0-13e-mass-aug.ipynb)

## Các file chính trong repo

1. **Train lại model ensemble #2 (do không lưu weight)**
   - [`train-only-13-epochs-b2.ipynb`](train-only-13-epochs-b2.ipynb): train **13 epochs** cho model ensemble #2.

2. **Chạy lại toàn bộ pipeline (train + inference)**
   - [`train-full-pipeline.ipynb`](train-full-pipeline.ipynb):  
     - Train **25 epochs** cho model ensemble #1  
     - Train **13 epochs** cho model ensemble #2  
     - Có thể Run-All để chạy lại toàn bộ pipeline, bao gồm cả inference.  
     - Kết quả inference (submission) được lưu tại:
       - [`my_submission_no_tta (2).csv`](my_submission_no_tta%20(2).csv)

3. **Inference (có thể dùng model path)**
   - [`inference-all.ipynb`](inference-all.ipynb): luồng inference, có thể trỏ tới đường dẫn weight model.

## Link weight model (Google Drive)

- Weight model được lưu tại Google Drive:  
  - https://drive.google.com/drive/folders/1OPI5FK_DPgfwUYMhHTR0vEtAuuASpQBh?usp=drive_link

# Cách train và inference

1. **Kiểm chứng khả năng tái lập (reproducibility)**  
   Ban tổ chức có thể Run-All notebook:
   - [`train-full-pipeline.ipynb`](train-full-pipeline.ipynb)

2. **Inference bằng weight có sẵn**  
   Ban tổ chức có thể Run-All notebook:
   - [`inference-all.ipynb`](inference-all.ipynb)
