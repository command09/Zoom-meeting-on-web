# การติดตั้ง Zoom meeting บนเว็บไซต์

สามรถศึกษาคู่มือได้จาก [Terms of Use](https://zoom.us/docs/en-us/zoom_api_license_and_tou.html).

การเรียกใช้งาน [Zoom Meeting SDK] โดยเข้าไปที่ (https://marketplace.zoom.us/docs/sdk/native-sdks/web) เพื่อขอ "SDK_KEY" และ "SDK_SECRET"

![Zoom Meeting SDK Client View](https://marketplace.zoom.us/docs/images/sdk/msdk-web-client-view.gif)

## การตั้งค่าใช้งาน

1. หลังจากดาวน์โหลดไฟล์ .zip แล้วให้ทำการแตกไฟล์ไว้ตำแหน่งที่ต้องการ หรือจะคัดลอกด้วยคำสั่ง

`$ git clone https://github.com/command09/Zoom-meeting-on-web.git`

2. เปิดไฟล์เพื่อทำการแก้ไขด้วย Text Editer

3. เปิดไฟล์ `sample-app-web/CDN/js/index.js` : เพื่อแก้ไขค่า "SDK_KEY" และ "SDK_SECRET"


   | Key                   | Value Description |
   | -----------------------|-------------|
   | `SDK_KEY`     | Your SDK Key. Required. |
   | `SDK_SECRET`  | Your SDK Secret. Required. |

   Example:

   ```js
   var SDK_KEY = "YOUR_SDK_KEY"
   var SDK_SECRET = "YOUR_SDK_SECRET"
   ```
4. เปิดไฟล์บน Brower ตำแหน่งไฟล์หน้าแรกของ Zoom meeting คือ `CDN/index.html`
5. ทดสอบสร้างการประชุมผ่านแอพพลิเคชั่น Zoom หรือผ่านหน้าเว็บผู้ให้บริการหลัก แล้วสร้าง url สำหรับเชิญเข้าประชุม
6. นำหมายเลขห้องประชุม กับ รหัสผ่านมากรอกในหหน้า `index.html` และกรอกอีเมลย์ จากนั้นกดปุ่ม Join
7. หากไม่สามารถเรียกหน้าแสดงผลได้  ให้เข้าไปแก้ไขไฟล์ `sample-app-web/CDN/js/index.js` บรรทัด `var joinUrl = meeting.html?` แก้ไขตำปหน่งของไฟล์ `meeting.html` ให้ถูกต้อง
8. บันทึกแล้วทดสอบอีกครั้ง  จะเห็นว่าสามารถแสดงหน้าเข้าร่วมประชุมได้แล้วบนเว็บไซต์ของเราเอง


## Need help?

If you're looking for help, try [Developer Support](https://devsupport.zoom.us) or our [Developer Forum](https://devforum.zoom.us). Priority support is also available with [Premier Developer Support](https://zoom.us/docs/en-us/developer-support-plans.html) plans.
