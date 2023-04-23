# Forms

* องค์ประกอบอีกชุดหนึ่งที่สำคัญมากเมื่อสร้างเว็บไซต์คือวิธีการรวบรวมข้อมูลจากผู้ใช้ คุณสามารถอนุญาตให้ผู้ใช้ป้อนข้อมูลโดยใช้แบบฟอร์ม HTML ซึ่งสามารถป้อนได้หลายประเภท ในวิชานี้ เราจะได้เรียนรู้เกี่ยวกับวิธีจัดการกับข้อมูลเมื่อมีการส่งแบบฟอร์ม
* เช่นเดียวกับองค์ประกอบ HTML อื่นๆ คุณไม่จำเป็นต้องจำองค์ประกอบเหล่านี้ และ W3 Schools เป็นแหล่งข้อมูลที่ยอดเยี่ยมสำหรับการเรียนรู้เกี่ยวกับองค์ประกอบเหล่านี้!

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Forms</title>
</head>
<body>
    <form>
        <input type="text" placeholder="First Name" name="first">
        <input type="password" placeholder="Password" name="password">
        <div>
            Favorite Color:
            <input name="color" type="radio" value="blue"> Blue
            <input name="color" type="radio" value="green"> Green
            <input name="color" type="radio" value="yellow"> Yellow
            <input name="color" type="radio" value="red"> Red

        </div>
        <input type="submit">
    </form>
</body>
</html>
```

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>
