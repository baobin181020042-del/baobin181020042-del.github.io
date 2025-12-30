---

title: "Lập trình hướng đối tượng (OOP) trong Java - Từ lý thuyết đến thực chiến"

date: 2024-12-20

draft: false

tags: ["Java", "OOP", "Lập trình", "Backend"]

categories: ["Java"]

featured_image: "/images/anh4.jpg"

description: "Phân tích chuyên sâu 4 trụ cột của OOP: Đóng gói, Kế thừa, Đa hình, Trừu tượng và cách áp dụng hiệu quả trong dự án Java."

---



## 🚀 Giới thiệu

<div style="background-color: #1e1e1e; padding: 15px; border-left: 5px solid #2196F3; margin-bottom: 20px; border-radius: 4px; color: #e0e0e0;">
'''
    <strong>💡 Tổng quan:</strong> Lập trình hướng đối tượng (OOP - Object Oriented Programming) không chỉ là viết code, mà là <em>tư duy mô hình hóa</em> thế giới thực vào trong máy tính. Thay vì viết một danh sách các lệnh chạy từ trên xuống dưới (Lập trình thủ tục), OOP giúp chúng ta chia nhỏ phần mềm thành các <strong>Đối tượng (Objects)</strong> tương tác với nhau.

</div>



Trong Java, mọi thứ đều xoay quanh **Class (Lớp)** và **Object (Đối tượng)**. Nếu coi **Class** là bản thiết kế (Blueprint), thì **Object** chính là ngôi nhà được xây dựng từ bản vẽ đó.



Hãy cùng đi sâu vào 4 trụ cột chính (The 4 Pillars) đã làm nên sức mạnh của ngôn ngữ này và lý do tại sao mọi Java Developer đều phải nắm vững chúng.



---



## 1. Encapsulation (Tính Đóng gói) - Chiếc két sắt an toàn



Đóng gói là kỹ thuật che giấu thông tin và ngăn chặn việc truy cập trái phép vào các chi tiết nội bộ của một đối tượng.



### 🛡️ Tại sao cần Đóng gói?

Hãy tưởng tượng tài khoản ngân hàng của bạn. Nếu ai cũng có thể truy cập trực tiếp vào biến `soDu` (số dư) và sửa nó thành 0, thì thật thảm họa. Đóng gói buộc mọi người phải đi qua các "cửa kiểm soát" (hàm) để thay đổi dữ liệu.



* **Dữ liệu (Variables):** Được khai báo là `private` để ẩn đi.

* **Cửa kiểm soát (Methods):** Sử dụng `public Getter/Setter` để truy cập và kiểm tra tính hợp lệ.



```java

public class BankAccount {

    // 1. Dữ liệu bị ẩn đi (Private)

    private double balance;



    // 2. Phương thức công khai để nạp tiền (kiểm soát dữ liệu đầu vào)

    public void deposit(double amount) {

        if (amount > 0) {

            this.balance += amount;

            System.out.println("Đã nạp: " + amount);

        } else {

            System.out.println("Số tiền nạp không hợp lệ!");

        }

    }



    // 3. Getter để xem số dư (chỉ xem, không sửa trực tiếp được)

    public double getBalance() {

        return balance;

    }

}
```
2. Inheritance (Tính Kế thừa) - "Cha truyền con nối"

Kế thừa cho phép một lớp con (Subclass) sở hữu các thuộc tính và phương thức của lớp cha (Superclass).



🧬 Lợi ích cốt lõi

Giống như việc Xe Thể Thao kế thừa các đặc điểm của Xe Ô tô (có 4 bánh, có vô lăng, có động cơ) nhưng được nâng cấp thêm tốc độ.



Tái sử dụng mã nguồn (Code Reusability): Viết một lần ở lớp cha, dùng lại ở nhiều lớp con.

Dễ bảo trì: Khi sửa logic ở lớp cha, toàn bộ lớp con đều được cập nhật.

Từ khóa: Sử dụng extends.

⚠️ Lưu ý: Trong Java, một lớp chỉ có thể kế thừa từ một lớp cha duy nhất (Single Inheritance) để tránh xung đột dữ liệu (Diamond Problem).

3. Polymorphism (Tính Đa hình) - "Một tên gọi, nhiều hình thái"

Đa hình cho phép chúng ta thực hiện một hành động duy nhất theo nhiều cách khác nhau. Đây là tính chất giúp code Java trở nên linh hoạt và dễ mở rộng.



🎭 Hai loại Đa hình trong Java

A. Đa hình lúc biên dịch (Compile-time): Overloading

Cùng tên hàm nhưng khác tham số.



Ví dụ: Hàm tinhTong(int a, int b) và hàm tinhTong(int a, int b, int c).

B. Đa hình lúc chạy (Runtime): Overriding

Lớp con viết lại (ghi đè) phương thức của lớp cha để hoạt động theo cách riêng.



Ví dụ: Cùng là hành động makeSound() (phát ra tiếng), nhưng Chó sủa "Gâu", Mèo kêu "Meow".

4. Abstraction (Tính Trừu tượng) - Ẩn đi sự phức tạp

Trừu tượng hóa là việc chỉ hiển thị những tính năng thiết yếu cho người dùng và ẩn đi các chi tiết thực thi phức tạp bên dưới.



👻 Ví dụ thực tế

Khi lái xe ô tô, bạn chỉ quan tâm đến cái Vô lăng, Chân ga, Chân phanh (Giao diện). Bạn không cần biết (và không nên biết) hệ thống phun xăng điện tử hay trục cam bên trong động cơ hoạt động chi tiết ra sao.

Trong Java, chúng ta thực hiện điều này thông qua:



Abstract Class: Lớp trừu tượng (có thể chứa hàm có code và hàm rỗng).

Interface: Bản thiết kế hoàn toàn trừu tượng (chỉ chứa tên hàm, không có code logic).

## 💻 Ví dụ thực chiến tổng hợp (Full Code)

Dưới đây là ví dụ minh họa sự kết hợp hoàn hảo giữa **Kế thừa**, **Đa hình** và **Trừu tượng**:

```java
// 1. ABSTRACT CLASS (Tính Trừu tượng)
// Đây là khuôn mẫu chung cho mọi con vật
public abstract class Animal {
    protected String name; // Protected để lớp con có thể truy cập
    
    public Animal(String name) {
        this.name = name;
    }
    
    // Phương thức trừu tượng: Bắt buộc con cháu phải tự định nghĩa
    public abstract void makeSound();

    // Phương thức thường: Dùng chung cho tất cả
    public void sleep() {
        System.out.println(name + " đang ngủ... Zzz");
    }
}

// 2. INHERITANCE (Tính Kế thừa)
// Lớp Chó kế thừa từ Animal
public class Dog extends Animal {
    public Dog(String name) {
        super(name); // Gọi constructor của lớp cha
    }
    
    // 3. POLYMORPHISM (Tính Đa hình - Overriding)
    // Chó thực hiện hành động kêu theo cách riêng
    @Override
    public void makeSound() {
        System.out.println(name + " sủa: Gâu Gâu! 🐕");
    }
}

// Lớp Mèo kế thừa từ Animal
public class Cat extends Animal {
    public Cat(String name) {
        super(name);
    }
    
    @Override
    public void makeSound() {
        System.out.println(name + " kêu: Meow Meow! 🐈");
    }
}

// CLASS MAIN ĐỂ CHẠY CHƯƠNG TRÌNH
public class Main {
    public static void main(String[] args) {
        // Khởi tạo đối tượng (Object)
        Animal myDog = new Dog("Cậu Vàng");
        Animal myCat = new Cat("Tom");

        // Kiểm thử đa hình
        myDog.makeSound(); // Output: Cậu Vàng sủa: Gâu Gâu!
        myCat.makeSound(); // Output: Tom kêu: Meow Meow!
        
        // Kiểm thử phương thức kế thừa
        myDog.sleep();     // Output: Cậu Vàng đang ngủ... Zzz
    }
}