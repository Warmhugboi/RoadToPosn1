# นนท์ซ่าล่าท้าผี
หลังจากที่เหน็ดเหนื่อยจากการทำเว็บ TNTGradering.com มาเป็นเวลานาน \
อ้ายนนท์ซ่า007จึงได้ตัดสินใจพักผ่อนมารีแล็กซ์โดยการล่าท้าผีที่บ้านผีสิงแห่งหนึ่งโดยที่ ณ ทางเข้า นนท์ซ่าได้พบกับแปลนบ้าน \
จึงได้ทราบว่าบ้านหลังนี้มีห้องเรียงกันเป็นเส้นตรงทั้งหมด n ห้อง แต่ละห้องมีหมายเลขของตัวเองกำกับไว้ด้วยสีแดงปริศนาตั้งแต่ 1 2 3 ไปเรื่อยๆจนถึง n \
ด้วยความที่เป็นคนกลัวผี (แล้วจะมาทำไม) จึงอยากทราบว่าห้องที่ l ถึง r มีพลังงานลึกลับ k อยู่กี่ตน 
### input
บรรทัดแรด จำนวนเต็ม n และ q แสดงถึง จำนวนห้อง และจำนวนคำถาม \
บรรทัดถัดมา จำนวนเต็ม n ค่า \
q บรรทัดถัดมา จำนวเต็ม l , r และ k แสดงถึงห้องเริ่มต้น ,ห้องสุดท้าย และ k คือพลังงานลึกลับที่สนใจ
### output
มีทั้งหมด q บรรทัด ในแต่ละบรรทัดให้แสดงผลรวมตั้งแต่ตัวที่ l ถึง r

### Constraint:

1 <= n , q <= 500000


for each 0 <= i < n


-2147483648 <= a[i] <= 2147483647

1 <= l <= r <= n

-2147483648 <= k <= 2147483647

<br>

Time limit: 1 second

Memory limit: 64 MB

<br>

### input:

10 5

1 2 1 3 2 5 6 9 8 0

1 5 2

2 10 0

3 3 1

7 8 6

1 2 3


### output:

2

1

1

1

0

# หนูจะกลับบ้าน 
## ยังแต่งไม่หมด - (ยากมาก)
เรื่องมีอยู่ว่าหนูนิดคิดถึงบ้านที่อยู่กรุงเทพ จึงได้ลำบากตรากตรำหาทางกลับบ้านจากต่างจังหวัดที่แสนสุขสบาย 
โดยหลังจากที่ขึ้นรถทัวร์จากขอนแก่นมาลงที่กรุงเทพฯ หนูนิดก็ได้พบกับปัญหาใหญ่ นั่นก็คือการขึ้นรถไฟฟ้าสายมหา ณ เธอ ที่มีเส้นทางที่ซับซ้อนและยุ่งเหยิง 
โดยรถไฟฟ้าแห่งนี้มีอยู่ทั้งหมด n สถานี และมีข้อมูลการเดินรถอยู่ E เส้นทาง โดยในแต่ละเส้นทางมีข้อมลที่หนูนิดรู้อยู่ 3 อย่าง คือ l, r และ k 
แสดงถึงมีรถไฟฟ้าจากสถานี l ไปที่สถานี r แบบ one way และมีค่าใช้จ่ายเท่ากับ k
โดยที่ k เป็นจำนวนเต็ม เป็นค่าใช้จ่ายสำหรับการเดินทาง หากตัวเลขติดลบหมายถึงหนูนิดจะเก็บเงินได้จากเส้นทางนั้น และสามารถเก็บไว้ใช้ในการเดินทางสำหรับสำหรับครั้งถัดไป 
จากนั้น start และ end แสดงถึงสถานีต้นทางที่หนูนิดขึ้น และสถานีปลายทางที่หนูนิดลง

แต่ใครจะรู้ บางทีการกลับบ้านในครั้งนี้อาจทำให้หนูนิดเป็นเศรษฐีได้ หากมีเส้นทางที่สามารถเก็บเงินบนรถไฟฟ้าได้เรื่อยๆไม่มีที่สิ้นสุด กรณีนี้ให้แสดงผลว่า I'M RICH

แต่หากสิ่งนั้นเป็นแค่เรื่องเพ้อฝันของหนูนิด ให้แสดงเงินที่น้อยที่สุดที่หนูนิดจำเป็นต้องใช้ในการเดินทางกลับบ้าน
จากนั้นบรรทัดต่อมาแสดงแสดงทางการเดินทางของหนูนิดโดยแสดงในรูปแบบ start"path"end
โดยที่นิยามpathคือการเลี้ยวข้อรถไฟฟ้า, หากรถไฟฟ้าเดินทางจากสถานี s ไปยังสถานี e , เส้นทางจะถือเป็นการเลี้ยวซ้าย 'L' เมื่อ s < e และจะถือเป็นการเลี้ยวขวา 'R' เมื่อ s > e


ตัวอย่าง:

5LLRR10

เมื่อ 5 -> 4 -> 3 -> 6 -> 10

