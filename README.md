# Lưu ý quan trọng

- Tối qua tôi đã submit kết quả bằng phương pháp ensemble, nhưng quên lưu weight của model số 2. Vì vậy hôm nay khi chạy lại pipeline, tôi phải train lại riêng model số 2. Kết quả ensemble với model này có thể có sai lệch nhỏ so với bản submit trước.  
- Trong file train ban đầu, tôi có lưu training log thể hiện quá trình train và inference. Ban giám khảo có thể tham khảo ở file **effvs2_27e_b0_13e_mass_aug.ipynb** (bao gồm cả log training và inference).  
- Ngoài ra, repo còn có các file sau:  
  1. **train_only_13_epochs_b2.ipynb**: train 13 epochs cho model ensemble số 2, dùng để train lại do không lưu weight.  
  2. **train_full_pipeline.ipynb**: train 25 epochs cho model ensemble số 1 và 13 epochs cho model ensemble số 2. Có thể chạy lại toàn bộ pipeline bằng Run-All, bao gồm cả inference, kết quả lưu ở file **my_submission_no_tta.csv**.  
  3. File weight của model ensemble số 1: đây là weight chính xác đã được lưu và dùng cho submission.  

# Cách train và inference

1. Nếu muốn chạy lại toàn bộ pipeline để kiểm chứng khả năng tái lập, ban tổ chức có thể Run-All file **train_full_pipeline.ipynb**.  
2. Nếu muốn sử dụng file weight có sẵn trong repo để inference, ban tổ chức có thể Run-All file **inference_all.ipynb**.  
