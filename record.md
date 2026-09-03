Part A, Section 1
touch week2.md
git add week2.md
git commit -m "Da them file week2.md"
git branch week2
git switch week2

Part A, Section 2
touch working1
touch working2
git add working1
git commit -m "working 1"
git add working2
git commit -m "working 2"

Part A, Section 3
echo "xinchao" >> week2.md
git commit -a -m "Them dong xinchao vao week2.md"
git switch main
Khi chuyển về main và cat week2.md thì không có nội dung nào trong week2.md 

Part A, Section 4
git checkout -b week2b
git merge week2
git branch -d week2

Part B, Section 1
git branch wip
git switch wip
touch wip.txt
git add wip.txt
git commit -m "Da them file wip.txt"
git switch main
git merge week2b

Part B, Section 2
git branch --merged
git branch --no-merged
git branch --merged >> week2.md
git branch --no-merged >> week2.md

Part B, Section 3
git branch -d week2b

Part B, Section 4
git branch -m wip work-in-progress
git remote add origin https://github.com/laithao0206-hub/git-homework-2-LaiTranPhuongThao.git
git push -u origin main
git push origin work-in-progress
Nếu trước đó đã từng push nhách wip lên github thì sau khi đổi tên branch wip thành work-in-progress thì cần phải push lại với tên branch mới và xóa tên cũ trên remote

Part C, Section 1
git switch working-in-progress
echo "xin chao ngay moi" >> wip.txt
git commit -a -m "Da them dong xin chao ngay moi vao file working-in-progress"

Part C, Section 2
git branch -vv

Part C, Section 3
Làm trên web gitbub

Part D, Section 1
git switch main
git branch experiment
git switch experiment
touch file1.txt
touch file2.txt
git add file1.txt
git commit -m "Da them file file1.txt"
git add file2.txt
git commit -m "Da them file file2.txt"

Part D, Section 2
git switch main
touch file3.txt
git add file3.txt
git commit -m "Da them file file3.txt"

Part D, Section 3
git switch experiment
git rebase main

Part D, Section 4
Khi chạy git rebase master trên nhánh experiment, git sẽ tạm thời tháo gỡ 2 commit mới của experiment, chuyển gốc của nhánh này tiến lên trùng với commit mới nhất của master, rồi lần lượt áp dụng lại 2 commit đó nối tiếp ngay sau master dưới dạng các commit hoàn toàn mới, giúp lịch sử commit biến thành một đường thẳng tuyến tính thay vì bị phân nhánh.

Part D, Section 5
git switch main
git merge experiment

Part D, Section 6
git push -u origin main

Part D, Section 7
git add record.md
git commit -m "Update record.md"
git push origin main
