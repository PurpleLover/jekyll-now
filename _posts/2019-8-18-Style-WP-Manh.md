# Hướng dẫn tút tát vẻ ngoài (đặc biệt dành cho Manh)

## Lời nói đầu

Việc tút tát vẻ ngoài cho bài viết (post), trang (page) là một trong những công việc mà giới blogger rất thích vào thời điểm chưa có những CMS siêu đẳng như Wordpress, Drupal, Mojo... Tuy nhiên, muốn làm được điều này, các blogger đời đầu đã phải mài công khổ luyện để lần mò HTML, CSS, JS để kết nối các thứ lại với nhau.

Còn vào thời điểm này, thời đại mà vua-tin-vịt và lều-báo-chính-thống đưa tin về những thứ như là cách mạng công nghiệp 4.0, thì bạn đã rời xa khỏi cái thời phải lần mò từng ngóc ngách của Internet để biết cách dùng một thẻ HTML hay viết một dòng style trong CSS. Giờ đây bạn đã có những trang như:

* W3Schools để có thể truy cứu và học về đủ mọi thứ từ HTML, CSS, JS
* FreeCodeCamp là một trang, một cộng đồng giúp học Frontend (HTML, CSS) từ cơ bản đến nâng cao mà với ví dụ trực quan, ước tính chỉ trong vòng 100 - 200 giờ bạn đã có thể tự tin viết vào CV của mình là thành thạo Frontend dù chưa học qua trường lớp bài bản nào
* ...và một số trang khác như Udemy, Vietjack, vân vân và mây mây

Nói tóm lại, kiến thức là vô tận, nhưng giờ tiếp cận chúng quá dễ dàng rồi nên đừng lo sợ, đừng u sầu vì một cái gì đó quá mới. Hãy luôn mở rộng lòng mình, luôn sẵn sàng tiếp thu cái mới, và trên hết, chăm chỉ bù thông minh là tốt hơn cả.

Với tôi, sự chăm chỉ có thể bù lại nhiều thứ mà bạn không có - một kẻ đi thi IQ và đạt ở mức cận trung bình.

## Điều kiện tiên quyết

* Biết sử dụng máy vi tính
* Hiểu tiếng Anh, thành thạo tiếng Việt

## Các bài hướng dẫn

Ở mục này, tôi chia nhỏ ra thành các đề mục tương ứng với từng bài hướng dẫn mà tôi sẽ ghi lại cho bạn (Manh). Nếu có gì đó chưa hiểu, hãy liên hệ trực tiếp với tôi qua tài khoản Facebook (Manh knows this), hoặc bất cứ tài khoản nào mà bạn biết về tôi, thậm chí là Email.

Các bài hướng dẫn tôi viết đều dựa trên Classic Editor, vì hiện tại Block editor không ăn được CSS mà tôi tuỳ chỉnh, nên trong tương lai gần, bạn có thể tuỳ chỉnh ngay trên công cụ mới thêm vào WP 5.0 này.

Thôi xạo lìn thế đủ rồi, bắt đầu thôi nhỉ?

### Thêm một dòng mới trong bảng liệt kê truyện

Đoạn code vẽ ra một dòng mới có dạng như sau:

```
<div class="wp-block-columns">
  <div class="wp-block-column" style="flex-basis: 60%;">
    <p style="text-align: left;">
      <a href="https://vivi3010.wordpress.com/2019/04/10/phat-song-truc-tiep-sinh-hoat-cua-trai-dat-cuu-thien-giang/">
        [HĐ] Phát sóng trực tiếp sinh hoạt của Trái Đất
      </a>
    </p>
  </div>
  <div class="wp-block-column" style="flex-basis: 40%;">
    <div class="wp-block-button aligncenter is-style-default">
      <figure class="wp-block-jetpack-rating-star" style="text-align: center;">
        <span style="color: #f7777b;">★</span>
        <span style="color: #f7777b;">★</span>
        <span style="color: #f7777b;">★</span>
        <span style="color: #f7777b;">★</span>
        <span style="color: #f7777b;">★</span>
        <span style="color: #f7777b;">★</span>
      </figure>
    </div>
  </div>
</div>
```

#### Khái quát

Một dòng mới được bao bọc bằng thẻ div có class `wp-block-columns`. Trong một dòng thường chỉ nên có 2 cột, mỗi cột cũng nên được bọc trong thẻ div có class `wp-block-column`. `flex-basis` quy định độ rộng của cột đó, và tổng độ rộng của các cột trên một dòng phải là 100%, nếu không thì khả năng cao cột sau sẽ bị tụt xuống dưới.

Nếu bạn chỉ quan tâm đến nội dung của dòng, thì hãy giữ nguyên format như trên, đừng thay đổi gì hơn cả.

#### Nội dung

Để thay đổi tên truyện, hãy thay dòng `HĐ] Phát sóng trực tiếp sinh hoạt của Trái Đất` bằng tên truyện bạn muốn. Và đổi đường dẫn tới truyện đó trong phần `a href`.
Đến đây, chắc hẳn bạn sẽ nghĩ, ơ thế giờ chưa có link đính kèm với truyện thì làm thế nào? Nếu chưa có thì đừng bọc tên truyện trong thẻ `<a></a>`, mà hãy bọc nó trong thẻ p ngoài cùng. Chẳng hạn như sau:

```
<p style="text-align: left;">
  [HĐ] Phát sóng trực tiếp sinh hoạt của Trái Đất
</p>
```

Để thay đổi số sao tương ứng với tên truyện, hãy nhòm vào trong thẻ `<figure>`, mỗi thẻ `<span>` tương ứng với 1 trong 5 sao. Muốn tăng giảm số sao chỉ cần thêm bớt thẻ span trong này thôi. Tôi đề nghị đến lúc này bạn nên dùng Ctrl C và Ctrl V thay vì gõ lại, vừa mất thì giờ mà vừa dễ bị sai.