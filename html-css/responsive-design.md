# Responsive Design

* ปัจจุบัน ผู้คนจำนวนมากดูเว็บไซต์บนอุปกรณ์อื่นที่ไม่ใช่คอมพิวเตอร์ เช่น สมาร์ทโฟนและแท็บเล็ต สิ่งสำคัญคือต้องแน่ใจว่าเว็บไซต์ของคุณสามารถอ่านได้ในทุกอุปกรณ์
* วิธีหนึ่งที่เราจะบรรลุสิ่งนี้ได้คือมีความรู้เรื่อง **viewport**.  วิวพอร์ตคือส่วนของหน้าจอที่ผู้ใช้สามารถมองเห็นได้ตามเวลาที่กำหนด ตามค่าเริ่มต้น หน้าเว็บจำนวนมากถือว่าวิวพอร์ตเหมือนกันในทุกอุปกรณ์ ซึ่งเป็นสาเหตุที่ทำให้ไซต์จำนวนมาก (โดยเฉพาะไซต์ที่เก่ากว่า) โต้ตอบบนอุปกรณ์เคลื่อนที่ได้ยาก
* วิธีง่ายๆ วิธีหนึ่งในการปรับปรุงรูปลักษณ์ของไซต์บนอุปกรณ์เคลื่อนที่คือการเพิ่มบรรทัดต่อไปนี้ในส่วนหัวของไฟล์ HTML ของเรา บรรทัดนี้บอกให้อุปกรณ์เคลื่อนที่ใช้วิวพอร์ตที่มีความกว้างเท่ากับอุปกรณ์ที่คุณใช้แทนที่จะเป็นอุปกรณ์ที่ใหญ่กว่ามาก

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

* อีกวิธีหนึ่งที่เราสามารถจัดการกับอุปกรณ์ต่างๆ ได้คือ [media queries](https://www.w3schools.com/cssref/css3\_pr\_mediaquery.asp).  Media queries เป็นวิธีการเปลี่ยนสไตล์ของเพจตามวิธีการดูเพจ
* สำหรับตัวอย่างของ media query, มาลองเปลี่ยนสีของหน้าจอง่ายๆ เมื่อมันย่อขนาดลงจนถึงขนาดที่กำหนด. เราส่งสัญญาณmedia query โดยการพิมพ์ `@media` ตามด้วยประเภทของ query ในวงเล็บ:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Screen Size</title>
        <style>
            @media (min-width: 600px) {
                body {
                    background-color: red;
                }
            }

            @media (max-width: 599px) {
                body {
                    background-color: blue;
                }
            }
        </style>
    </head>
    <body>
        <h1>Welcome to the page!</h1>
    </body>
</html>
```

<figure><img src="../.gitbook/assets/responsive0.gif" alt=""><figcaption></figcaption></figure>

* อีกวิธีในการจัดการกับขนาดหน้าจอที่แตกต่างกันคือการใช้แอตทริบิวต์ CSS ใหม่ที่เรียกว่า aอีกวิธีในการจัดการกับขนาดหน้าจอที่แตกต่างกันคือการใช้แอตทริบิวต์ CSS ใหม่ที่เรียกว่า [flexbox](https://www.w3schools.com/css/css3\_flexbox.asp). วิธีนี้ช่วยให้เรามีองค์ประกอบล้อมรอบบรรทัดถัดไปได้อย่างง่ายดายหากไม่พอดีกับแนวนอน เราทำเช่นนี้โดยใส่องค์ประกอบทั้งหมดของเราใน `div` ที่เราจะเรียกว่าคอนเทนเนอร์ของเรา จากนั้นเราเพิ่มสไตล์ให้กับ div นั้นโดยระบุว่าเราต้องการใช้การแสดง flexbox สำหรับองค์ประกอบที่อยู่ภายในเรายังได้เพิ่มสไตล์เพิ่มเติมให้กับ div ภายในเพื่อแสดงให้เห็นการรวมที่เกิดขึ้นที่นี่ได้ดียิ่งขึ้น

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Screen Size</title>
        <style>
            #container {
                display: flex;
                flex-wrap: wrap;
            }

            #container > div {
                background-color: green;
                font-size: 20px;
                margin: 20px;
                padding: 20px;
                width: 200px;
            }
        </style>
    </head>
    <body>
        <div id="container">
            <div>Some text 1!</div>
            <div>Some text 2!</div>
            <div>Some text 3!</div>
            <div>Some text 4!</div>
            <div>Some text 5!</div>
            <div>Some text 6!</div>
            <div>Some text 7!</div>
            <div>Some text 8!</div>
            <div>Some text 9!</div>
            <div>Some text 10!</div>
            <div>Some text 11!</div>
            <div>Some text 12!</div>
        </div>
    </body>
</html>
```

<figure><img src="../.gitbook/assets/flexbox.gif" alt=""><figcaption></figcaption></figure>

* อีกวิธีที่นิยมในการจัดหน้าเพจคือการใช้ HTML [grid](https://www.w3schools.com/css/css\_grid.asp). ในกริดนี้ เราสามารถระบุแอตทริบิวต์ของสไตล์ เช่น ความกว้างของคอลัมน์และช่องว่างระหว่างคอลัมน์และแถว ดังที่แสดงด้านล่าง โปรดทราบว่าเมื่อเราระบุความกว้างของคอลัมน์ เราจะบอกว่าค่าที่สามคือ `auto`, หมายความว่าควรเติมส่วนที่เหลือของหน้า

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>My Web Page!</title>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <style>
            .grid {
                background-color: green;
                display: grid;
                padding: 20px;
                grid-column-gap: 20px;
                grid-row-gap: 10px;
                grid-template-columns: 200px 200px auto;
            }

            .grid-item {
                background-color: white;
                font-size: 20px;
                padding: 20px;
                text-align: center;
            }
        </style>
    </head>
    <body>
        <div class="grid">
            <div class="grid-item">1</div>
            <div class="grid-item">2</div>
            <div class="grid-item">3</div>
            <div class="grid-item">4</div>
            <div class="grid-item">5</div>
            <div class="grid-item">6</div>
            <div class="grid-item">7</div>
            <div class="grid-item">8</div>
            <div class="grid-item">9</div>
            <div class="grid-item">10</div>
            <div class="grid-item">11</div>
            <div class="grid-item">12</div>
        </div>
    </body>
</html>
```

<figure><img src="../.gitbook/assets/grid.gif" alt=""><figcaption></figcaption></figure>
