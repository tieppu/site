---
layout: default
title: Lấy đoạn trích dẫn bài viết tự động trong jekyll
date: 2019-07-24T04:51:25.670Z
---
Hiện tại, tôi bao gồm các trích đoạn như thế này:

```
{{ post.excerpt | strip_html }}
```

Nhưng điều này dường như chỉ đưa ra đoạn đầu tiên. Nhưng tôi muốn có được một số lượng từ cố định.

Hoặc tốt hơn: Tôi muốn xác định số lượng ký tự tối đa và nhận được rất nhiều từ

số lượng ký tự ít hơn mức tối đa

một từ nữa sẽ vượt quá số lượng ký tự tối đa

Có cách nào để làm điều này với Jekyll (1.3.1) không?

chỉnh sửa: 

```
<!-- more -->
```

không phải là một câu trả lời! Tôi nghĩ rằng trích đoạn sẽ hoạt động tự động và bài viết của tôi chỉ nên chứa đánh dấu là hoàn toàn cần thiết.

Sau đây cho một đoạn trích tự động 75 từ:

```
{{ post.content | strip_html | truncatewords:75 }}
```



Thật ra 

```
<!-- more -->
```

là câu trả lời. Ít nhất, nó hoạt động tốt bây giờ.



Thêm dòng này vào **_config.yml:**



```
excerpt_separator: "<!-- more -->"
```



Sau đó thêm điều này vào mỗi bài đăng trong trang web của bạn:



```
<!-- more -->
```



Hy vọng nó sẽ giúp.
