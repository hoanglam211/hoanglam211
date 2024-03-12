listStudent.forEach((student) -> {
    double value = hashMap.get(student.getType()) + 1;
    hashMap.replace(student.getType(), value);
});
- Với mỗi sinh viên trong danh sách, lấy loại sinh viên của sinh viên đó và tăng giá trị tương ứng trong HashMap lên 1.

- Lưu ý: Nếu loại sinh viên chưa tồn tại trong HashMap, thì hashMap.get(student.getType()) sẽ trả về null. Tuy nhiên, khi thực hiện phép cộng _**null + 1**_, sẽ xảy ra lỗi, vì vậy bạn cần đảm bảo rằng giá trị cho mỗi loại sinh viên đã được khởi tạo là 0.0 trước khi tăng giá trị.
Sau đó, cập nhật giá trị mới vào HashMap bằng cách sử dụng phương thức replace.
