# Day16 Cloud Benchmark Report

1. Tôi sử dụng AWS tại region us-east-1 với compute node t3.medium và Bastion t3.micro. Source commit: <SHA>.

2. Dataset Credit Card Fraud Detection có 284,807 dòng và 31 cột. Dữ liệu được chia train/validation/test theo tỷ lệ 60/20/20 với seed 42 và stratified split.

3. Load dữ liệu mất <DATA_LOAD_SECONDS> giây; training mất <TRAINING_SECONDS> giây; best iteration là <BEST_ITERATION>.

4. Trên tập test: AUC-ROC = <AUC>, Accuracy = <ACCURACY>, F1 = <F1>, Precision = <PRECISION>, Recall = <RECALL>.

5. Latency 1 dòng là <LATENCY> ms; throughput batch 1,000 dòng là <THROUGHPUT> rows/second.

6. Trong lúc benchmark chạy, process Python đạt khoảng 131.9% CPU và 12.9% memory. VM có khoảng 3.7 GiB RAM. Network được quan sát bằng `ip -s link`.

7. AWS Billing tại thời điểm quan sát <TIME> là <COST hoặc "chưa cập nhật">.

8. Tôi đã tải benchmark.py và benchmark_result.json về laptop và chạy `terraform destroy`. Sau cleanup, `terraform state list` không còn resource của deployment.