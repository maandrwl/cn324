# cn324 - Internet Technologies 2020 semester 1
เนื้อหาในรายวิชา cn324 Internet Techonologies นั้นครอบคลุมความรู้ที่จำเป็นของอินเทอร์เน็ตในยุคปัจจุบัน ซึ่งประกอบไปด้วยถึงความรู้ทางด้าน network เช่น อุปกรณ์เกี่ยวข้องกับการทำงานของอินเทอร์เน็ต หน่วยงานที่เกี่ยวข้องกับมาตรฐานโปรโตคอล ลักษณะและการทำงานของโปรโตคอลต่าง ๆ ความแตกต่างของ IPv4/IPv6 ตลอดจนถึงวิธีการส่งข้อมูลผ่าน network นอกจากนี้ยังได้เรียนรู้เกี่ยวกับสิ่งสำคัญซึ่งเพิ่มความปลอดภัยให้แก่อินเทอร์เน็ตในปัจจุบัน ซึ่งก็คือ Digital Signature ที่เกิดมาจากแนวคิดของ Key Pair Technology และ Hash Function รวมไปถึง IPFS ซึ่งเป็นอนาคตของอินเทอร์เน็ตที่ไม่จำเป็นต้องพึ่งพาระบบเครือข่ายแบบรวมศูนย์ (Centralized Server) อีกต่อไป

## Midterm exam
- [ข้อ 1](https://youtu.be/EIPNZAGMSZc)
- [ข้อ 2](https://youtu.be/2rz3v2JLqRU)
- [ข้อ 6](https://youtu.be/Ch9F8j0ZSlI)
- [ข้อ 7](https://youtu.be/lmtC7YhDqrs)

## Materials
### 1. ข้อสอบเก่า
[link](https://youtu.be/vAZFbvOROug)
### 2. TCP/IP headers 
อธิบายเกี่ยวกับ headers ของโปรโตคอล TCP และ IP ทั้ง IPv4 และ IPv6
[link](https://youtu.be/ki53k7tfotc)
### 3. TCP/IP headers (เพิ่มวิธีการส่งระหว่าง network)
อธิบายเพิ่มเติมในส่วนของการส่ง packet ระหว่าง network โดpกำหนดเป็น LAN network และ WIFI network ซึ่งเชื่อมกันด้วย router ที่อยู่ระหว่างเครือข่ายทั้งสอง <br>
[link)](https://youtu.be/7yGRjiYn2CM)
### 4. Hash functions and PKI
ศึกษาในส่วนของ Hash Function ซึ่งเป็นฟังก์ชันที่ใช้ digest ข้อมูลให้มีขนาดเท่ากัน และ PKI หรือ Public Key Infrastructure ซึ่งเป็นรูปแบบการเข้ารหัสข้อมูล ประกอบไปด้วยแบบ symmetric (ใช้กุญแจตัวเดียว) และ asymmetric (ใช้ private และ public key) รวมไปถึง Digital Signature ซึ่งเป็นการนำแนวคิดของ Hash Function มาผสมกับ PKI และได้ผลลัพธ์ออกมาเป็นการลงลายมือชื่อทางออนไลน์ นำไปใช้ในการตรวจสอบยืนยันตัวบุคคลได้<br>
[link](https://youtu.be/vAZFbvOROug)
### 5. Generating Key pair
ศึกษาในส่วนของการสร้าง key pair โดยใช้คำสั่ง ssh -keygen ใน git bash
[link](https://youtu.be/DPmdFAXuIBw)
### 6. Traceroute
ศึกษาการใช้คำสั่ง traceroute ในการหาเส้นทางที่ใช้ในการเดินทางไปยังเว็บไซต์ทั้ง 5 เว็บไซต์ โดยเริ่มจากการ ssh ไปยังเซิร์ฟเวอร์ แล้ว traceroute โดยที่ <br>
tail -n +2 คือการตัดมาเฉพาะบรรทัดที่ 2 ลงไป <br>
awk '{ print $2 }' คือการ print เฉพาะ column ที่ 2 (หมายเลข IP) <br>
grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" คือการเลืออกเฉพาะบรรทัดที่มีหมายเลข IP (บางทรรทัดเป็น \*) <br>
while read r; do echo "\"https://tools.keycdn.com/geo.json?host=$r\""; done คือการค้นหาข้อมูลเกี่ยวกับ IP address นั้น ๆ เช่น พิกัดที่ตั้ง ซึ่งจะได้ข้อมูลกลับมาเป็น json <br>
และ jq ช่วยในการแปลงข้อมูล json ให้มีโครงสร้างที่อ่านได้ง่ายขึ้น
[commands](https://github.com/keirace/cn324/blob/master/traceroute)<br>
[link](https://youtu.be/QBNvroTTlDU)
### 7. Git object structure
ศึกษาลักษณะโครงสร้างของวัตถุใน git และทดลองโดยการอ่านไฟล์ เพิ่มไฟล์ และแก้ไขไฟล์
[link](https://youtu.be/pszhYeB_qZg)
### 8. IPFS
ศึกษาเกี่ยวกับความหมายของ IPFS การทำงานของ IPFS ข้อดี-ข้อเสีย ตลอดจนถึงวิธีการแก้ปัญหาของข้อเสียนั้น
[link](https://youtu.be/gQ6CjGrtQUg)