# More HTML Elements

* มีองค์ประกอบ HTML มากมายที่คุณอาจต้องการใช้ปรับแต่งเพจของคุณ รวมถึงส่วนหัว,heading, รายการ,list, และส่วนที่เป็นตัวหนา ในตัวอย่างต่อไปนี้ เราจะเห็นการดำเนินการบางอย่างเหล่านี้
* อีกสิ่งหนึ่งที่ควรทราบ: \<!-- This is comment -- > ให้ความคิดเห็นกับเราใน HTML ดังนั้นเราจะใช้ข้อมูลด้านล่างเพื่ออธิบายองค์ประกอบบางอย่าง

{% code overflow="wrap" lineNumbers="true" %}
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>HTML Elements</title>
    </head>
    <body>
        <!-- เราสามารถสร้างหัวเรื่องโดยใช้ h1 ถึง h6 เป็นแท็ก -->
        <h1>A Large Heading</h1>
        <h2>A Smaller Heading</h2>
        <h6>The Smallest Heading</h6>

        <!-- แท็ก strong และ i ทำให้เราเป็นตัวหนาและตัวเอียงตามลำดับ -->
        A <strong>bold</strong> word and an <i>italicized</i> word!

        <!-- เราสามารถลิงก์ไปยังหน้าอื่น (เช่น หน้าของ cs50) โดยใช้ -->
        View the <a href="https://cs50.harvard.edu/">CS50 Website</a>!

        <!-- เราใช้ ul สำหรับรายการที่ไม่เรียงลำดับ และ ol สำหรับรายการที่เรียงลำดับ ทั้งรายการที่สั่งซื้อและไม่เรียงลำดับมี li หรือรายการในรายการ -->
        An unordered list:
        <ul>
            <li>foo</li>
            <li>bar</li>
            <li>baz</li>
        </ul>
        An ordered list:
        <ol>
            <li>foo</li>
            <li>bar</li>
            <li>baz</li>
        </ol>

        <!-- รูปภาพต้องการแอตทริบิวต์ src ซึ่งอาจเป็นได้ทั้งเส้นทางไปยังไฟล์ในคอมพิวเตอร์ของคุณหรือลิงก์ไปยังรูปภาพออนไลน์ นอกจากนี้ยังมีแอตทริบิวต์ alt ซึ่งให้คำอธิบายในกรณีที่โหลดรูปภาพไม่ได้ -->
        An image:
        <img src="manja-vitolic-gKXKBY-C-Dk-unsplash.jpg" alt="Gipsy the Cat was sitting on a bookshelf one afternoon and just stared right at me">
        <!-- เราสามารถเห็นได้จากด้านบนว่าสำหรับบางองค์ประกอบที่ไม่มีองค์ประกอบอื่น แท็กปิดไม่จำเป็น -->

        <!-- Here, we use a br tag to add white space to the page. -->
        <br/> <br/>

        <!-- ที่นี่ เราใช้แท็ก br เพื่อเพิ่มพื้นที่ว่างให้กับหน้า -->
        <table>
            <thead>
                <th>Ocean</th>
                <th>Average Depth</th>
                <th>Maximum Depth</th>
            </thead>
            <tbody>
                <tr>
                    <td>Pacific</td>
                    <td>4280 m</td>
                    <td>10911 m</td>
                </tr>
                <tr>
                    <td>Atlantic</td>
                    <td>3646 m</td>
                    <td>8486 m</td>
                </tr>
            </tbody>
        </table>
    </body>
<html>
```
{% endcode %}

* หน้านี้เมื่อแสดงผลจะมีลักษณะดังนี้:

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

* ในกรณีที่คุณกังวลเกี่ยวกับเรื่องนี้ ให้รู้ว่าคุณจะไม่ต้องจำองค์ประกอบเหล่านี้อีกต่อไป มันง่ายมากที่จะค้นหาบางอย่างเช่น "image in HTML" เพื่อค้นหาแท็ก img แหล่งข้อมูลหนึ่งที่เป็นประโยชน์อย่างยิ่งสำหรับการเรียนรู้เกี่ยวกับองค์ประกอบเหล่านี้คือ [W3 Schools](https://www.w3schools.com/html/html\_elements.asp)
