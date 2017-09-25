# CocosCreator-LearnSimplePhysic
เป็น project สำหรับศึกษาการใช้ Physic engine ใน Cocos Creator เริ่มทำใน Cocos Creator v1.5.2

## prerequisite
* Cocos Creator v1.5.2 or above

## How to open project
1. Download as zip
1. Extract
1. Open Cocos Creator -> Click Open Other... tab
1. Browse to extracted folder -> Click open
1. That's it.

## หลักการทำงานหลัก
1. Character node (or node ที่ต้องตกลงมาตามแรงโน้มถ่วง)
   * Add Collider component เป็น box (คือสมมุติว่าวัตถุเป็นสีเหลี่ยม)
   * set property Type (ส่วน Rigid body component) ให้เป็น dynamic ทำให้วัตถุนี้ร่วงลงตามแรงโน้มถ่วง
   * set property Allow Sleep uncheck เพื่อให้มันคำนวณตลอดว่าต้องร่วงตอนไหน default มันจะ check มาให้ซึ่งทำให้เวลาเดินเลยคานด้านบนมันไม่ยอมร่วง
1. Ground node (or node ที่เป็นพื้นหรือที่ไม่ต้องตกลงมาตามแรงโน้มถ่วง)
   * Add Collider component เป็น box
   * set property Type (ส่วน Rigid body component) ให้เป็น static ทำให้วัตถุนี้ไม่ร่วงลงตามแรงโน้มถ่วง มักใช้กับวัตถุที่ต้องลอยอยู่ที่ตำแหน่งของมัน
1. สุดท้ายขาดไม่ได้ต้อง enable ระบบ physic ผ่าน code (ถ้าไม่ enable ระบบ physic จะไม่ทำงาน)
   * ไฟล์ script ในให้ add ไว้ที่ Canvas node (rootnode ของ scene นั้นๆ นั่นเอง)

<br />
เวลา add Collider component จะได้ component เพิ่มมา 2 ตัวที่ node นั้นๆ คือ <br />
- RigidBody component
- PhysicBoxCollider component

<br />
<br />
Rigid body = ส่วนร่างของวัตถุที่แข็งๆ (เท่าที่คิดได้แปลได้สวยสุดเท่านี้ :) <br />
Box collider = เป็น component ไว้ detect collider (หรือการชน) 
