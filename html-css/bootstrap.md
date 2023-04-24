# Bootstrap

* ปรากฎว่ามีไลบรารี่มากมายที่คนอื่นเขียนไว้แล้วที่สามารถทำให้สไตล์ของเว็บเพจง่ายยิ่งขึ้นไปอีก ไลบารียอดนิยม ที่เราจะใช้ตลอดทั้งหลักสูตรเรียกว่า [bootstrap](https://getbootstrap.com/).
* เราสามารถรวม bootstrap ไว้ในโค้ดของเราได้โดยเพิ่มบรรทัดเดียวที่ส่วนหัวของไฟล์ HTML ของเรา:

```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css" integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">
```

* ต่อไป เราสามารถดูคุณลักษณะบางอย่างของบูตสแตรปได้โดยไปที่ [documentation](https://getbootstrap.com/docs/4.5/components/) ส่วนหนึ่งของเว็บไซต์ของพวกเขา ในหน้านี้ คุณจะพบตัวอย่างคลาสมากมายที่คุณสามารถเพิ่มลงในองค์ประกอบที่อนุญาตให้จัดรูปแบบด้วยบูตสแตรป
* ฟีเจอร์บูตสแตรปยอดนิยมอย่างหนึ่งคือ [grid system](https://getbootstrap.com/docs/4.0/layout/grid/). Bootstrap จะแบ่งหน้าออกเป็น 12 คอลัมน์โดยอัตโนมัติ และเราสามารถเลือกได้ว่าจะใช้องค์ประกอบกี่คอลัมน์โดยการเพิ่มคลาส `col-x` ที่ซึ่ง `x` เป็นตัวเลขระหว่าง 1 ถึง 12 ตัวอย่างเช่น ในหน้าต่อไปนี้ เรามีแถวของคอลัมน์ที่มีความกว้างเท่ากัน แล้วมีแถวที่คอลัมน์ตรงกลางมีขนาดใหญ่กว่า:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>My Web Page!</title>
        <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
        <style>
            .row > div {
                padding: 20px;
                background-color: teal;
                border: 2px solid black;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <div class="row">
                <div class="col-4">
                    This is a section.
                </div>
                <div class="col-4">
                    This is another section.
                </div>
                <div class="col-4">
                    This is a third section.
                </div>
            </div>
        </div>
        <br/>
        <div class="container">
            <div class="row">
                <div class="col-3">
                    This is a section.
                </div>
                <div class="col-6">
                    This is another section.
                </div>
                <div class="col-3">
                    This is a third section.
                </div>
            </div>
        </div>
    </body>
</html>
```

<figure><img src="../.gitbook/assets/cols1.gif" alt=""><figcaption></figcaption></figure>

* เพื่อปรับปรุงการตอบสนองต่อมือถือ บูตสแตรปยังช่วยให้เราสามารถระบุขนาดคอลัมน์ที่แตกต่างกันไปตามขนาดหน้าจอ ในตัวอย่างต่อไปนี้ เราใช้ `col-lg-3` เพื่อแสดงว่าองค์ประกอบหนึ่งๆ ควรมี 3 คอลัมน์บนหน้าจอขนาดใหญ่ และ `col-sm-6` ในการแสดงองค์ประกอบควรใช้ 6 คอลัมน์เมื่อหน้าจอมีขนาดเล็ก:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>My Web Page!</title>
        <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
        <style>
            .row > div {
                padding: 20px;
                background-color: teal;
                border: 2px solid black;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <div class="row">
                <div class="col-lg-3 col-sm-6">
                    This is a section.
                </div>
                <div class="col-lg-3 col-sm-6">
                    This is another section.
                </div>
                <div class="col-lg-3 col-sm-6">
                    This is a third section.
                </div>
                <div class="col-lg-3 col-sm-6">
                    This is a fourth section.
                </div>
            </div>
        </div>
    </body>
</html>
```

<figure><img src="../.gitbook/assets/cols2.gif" alt=""><figcaption></figcaption></figure>
