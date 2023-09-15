# BASIC SYSTAX JAVA

- Chương trình Java là một ngôn ngữ lập trình hướng đối tượng, điều này có nghĩa rằng Java là sự tập hợp của các đối tượng, và những đối tượng này giao tiếp thông qua các cuộc gọi phương thức để làm việc cùng nhau. Dưới đây là một cuộc thảo luận ngắn về Lớp và Đối tượng, Phương thức, Biến thể thể hiện, cú pháp và ngữ nghĩa của Java.

## Các thuật ngữ cơ bản trong Java:

1. **Lớp (Class):** Lớp là một kế hoạch (blueprint) của một thể hiện của lớp (đối tượng). Nó có thể được định nghĩa như một mẫu logic chia sẻ các thuộc tính và phương thức chung.

   - Ví dụ1: Lớp của ngôi nhà là một lớp.
   - Ví dụ2: Trong thế giới thực, Alice là một đối tượng của lớp "Human" (Người).
2. **Đối tượng (Object)**: Đối tượng là một thể hiện của một lớp. Nó là một thực thể có hành vi và trạng thái.

   - Ví dụ: Chó, Mèo, Khỉ, v.v. là các đối tượng của lớp "Animal" (Động vật).
   - Hành vi: Chạy trên đường.
3. **Phương thức (Method)**: Hành vi của một đối tượng là phương thức.

   Ví dụ: Chỉ số nhiên liệu biểu thị lượng nhiên liệu còn lại trong ô tô.
4. **Lưu ý:** Khi lớp là **public**, tên tệp phải là tên của lớp.

   **demo.java**

   ```java
   import java.util.Scanner;

   public class demo{

       public static void main(String[] args) {
           Scanner inp = new Scanner(System.in);

           System.out.print("input n: ");

           int n = inp.nextInt();
           if (n <= 10) {
               System.out.println(n);
           } else {
               System.out.println("Over than 10");
           }


       }
   }
   ```

## **Systax (Cú pháp)**

### 1.Comment trong Java:

   Các loại **comment** trong Java.

   Comment trên một dòng (Single line Comment)

```
   // System.out.println("This is a comment.");
```

   Comment nhiều dòng (Multi-line Comment)

```
   /*
      System.out.println("This is the first line comment.");
      System.out.println("This is the second line comment.");
   */
```

### 2.Tên tệp nguồn (Source File Name):

   Tên của tệp nguồn phải chính xác trùng với tên lớp công cộng (public class) với phần mở rộng là .java. Tên tệp có thể khác nếu nó không có lớp công cộng. Giả sử bạn có một lớp công cộng GFG.

```
   GFG.java // cú pháp hợp lệ
   gfg.java // cú pháp không hợp lệ
```

### 3.Khả năng phân biệt chữ hoa và thường (Case Sensitivity):

   Java là ngôn ngữ phân biệt chữ hoa và thường, điều này có nghĩa rằng các định danh AB, Ab, aB và ab là khác nhau trong Java.

```
   System.out.println("GeeksforGeeks"); // cú pháp hợp lệ
   system.out.println("GeeksforGeeks"); // cú pháp không hợp lệ vì chữ cái đầu tiên của từ khóa System luôn là chữ in hoa.
```

### 4.Tên lớp (Class Names):

- Chữ cái đầu tiên của lớp nên là chữ in hoa (cho phép viết thường nhưng không khuyến khích).
- Nếu nhiều từ được sử dụng để tạo tên của lớp, thì chữ cái đầu tiên của mỗi từ nên là chữ in hoa. Dấu gạch dưới cũng được cho phép, nhưng không khuyến khích. Cũng được phép sử dụng số và ký hiệu tiền tệ, tuy nhiên, các ký hiệu tiền tệ cuối cùng cũng không được khuyến khích vì chúng được sử dụng cho mục đích đặc biệt (cho lớp nội và lớp ẩn danh).

```java
   class MyJavaProgram // cú pháp hợp lệ
   class 1Program // cú pháp không hợp lệ
   class My1Program // cú pháp hợp lệ
   class $Program // cú pháp hợp lệ, nhưng không khuyến khích
   class My$Program // cú pháp hợp lệ, nhưng không khuyến khích (lớp nội Program bên trong lớp My)
   class myJavaProgram // cú pháp hợp lệ, nhưng không khuyến khích
```

   public static void main(String [] args):

   Phương thức main() là điểm vào chính của một chương trình Java; đây là nơi xử lý bắt đầu. Cũng được phép sử dụng chữ ký public static void main(String… args).

### 5.Tên phương thức (Method Names):

- Tất cả tên phương thức nên bắt đầu bằng chữ cái viết thường (cho phép viết hoa nhưng viết thường được khuyến nghị).
- Nếu nhiều từ được sử dụng để tạo tên phương thức, thì chữ cái đầu tiên của mỗi từ nên là chữ in hoa. Dấu gạch dưới được cho phép, nhưng không khuyến khích. Cũng được phép sử dụng số và ký hiệu tiền tệ.

```
   public void employeeRecords() // cú pháp hợp lệ
   public void EmployeeRecords() // cú pháp hợp lệ, nhưng không khuyến khích
```

### 6.Định danh trong Java (Identifiers in Java):

   Định danh là tên của biến cục bộ, biến thể thể hiện và biến thể lớp, cũng như các nhãn, nhưng cũng là tên cho các lớp, gói (package), mô-đun và phương thức. Tất cả các ký tự Unicode đều hợp lệ, không chỉ tập con ASCII.

- Tất cả các định danh có thể bắt đầu bằng một chữ cái, ký hiệu tiền tệ hoặc gạch dưới (_). Theo quy ước, một chữ cái nên viết thường cho biến.
- Ký tự đầu tiên của các định danh có thể theo sau bởi bất kỳ sự kết hợp nào của chữ cái, chữ số, ký hiệu tiền tệ và gạch dưới. Gạch dưới không được khuyến khích cho tên biến. Hằng số (thuộc tính tĩnh cuối cùng và enums) nên được viết hoa toàn bộ.
- Quan trọng nhất là định danh là phân biệt chữ hoa và thường.
- Một từ khóa (keyword) không thể được sử dụng làm định danh vì nó là một từ được dự trữ và có một ý nghĩa đặc biệt.

   Các định danh hợp lệ: MinNumber, total, ak74, hello_world, $amount, _under_value
   Các định danh không hợp lệ: 74ak, -amount

### 7.Dấu trắng trong Java (White spaces in Java):

   Một dòng chỉ chứa dấu trắng, có thể có bình luận, được gọi là dòng trắng, và trình biên dịch Java hoàn toàn bỏ qua nó.

### 8.Các Modifiers truy cập (Access Modifiers): Những modifier này kiểm soát phạm vi của lớp và phương thức.

   Access Modifiers: default, public, protected, private.
   Non-access Modifiers: final, abstract, static, transient, synchronized, volatile, native.
