การใช้งาน Git และ GitHub ในการทำงานจริงอาจดูซับซ้อนในตอนแรก แต่เมื่อเข้าใจขั้นตอนพื้นฐานแล้ว จะสามารถช่วยให้การจัดการโค้ดและโปรเจคต่างๆ เป็นระเบียบและง่ายขึ้นมาก นี่คือการอธิบายการใช้งาน Git และ GitHub ในรูปแบบที่เข้าใจง่าย:

1. ติดตั้ง Git
ก่อนที่เราจะใช้งาน Git ต้องติดตั้ง Git ก่อน:
ดาวน์โหลดและติดตั้ง Git จาก git-scm.com.
หลังจากติดตั้งเสร็จ สามารถตรวจสอบเวอร์ชันได้จาก: git --version

2. ตั้งค่า Git เบื้องต้น
กำหนดชื่อและอีเมลสำหรับ Git (จะใช้ในการระบุว่าใครทำการเปลี่ยนแปลงในโค้ด):
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

3. เริ่มโปรเจคใหม่ด้วย Git
การสร้าง Git repository ใหม่:
ไปที่โฟลเดอร์โปรเจคของคุณ (ใช้คำสั่ง cd ไปที่โฟลเดอร์โปรเจค)
ใช้คำสั่งนี้เพื่อเริ่มต้น Git ในโปรเจค:
git init
การเชื่อมต่อกับ GitHub:
สร้าง repository ใหม่บน GitHub.
ใช้คำสั่งนี้เพื่อเชื่อมต่อ local repository กับ GitHub:
git remote add origin https://github.com/username/repository.git

4. การทำงานกับ Git (Commit และ Push)
การเพิ่มไฟล์ที่เปลี่ยนแปลง (Stage Changes):
git add .
หรือถ้าต้องก
git add <file_name>
การบันทึกการเปลี่ยนแปลง (Commit):
เมื่อคุณทำการเปลี่ยนแปลงไฟล์และเพิ่มไฟล์ลงไปแล้ว ให้ทำการ commit:
git commit -m "ข้อความที่อธิบายการเปลี่ยนแปลง"
การส่งข้อมูลขึ้น GitHub (Push):
หลังจากที่ commit แล้ว อย่าลืม push การเปลี่ยนแปลงขึ้นไปยัง GitHub:
git push origin main
หรือถ้าใช้ชื่อ branch อื่นๆ เช่น master หรือ develop ก็สามารถเปลี่ยนคำสั่งได้เช่น:
git push origin develop

5. การดึงข้อมูลจาก GitHub (Pull)
หากมีการเปลี่ยนแปลงบน GitHub โดยคนอื่น และคุณต้องการดึงข้อมูลมาใช้:
git pull origin main

6. การสร้าง Branch
การใช้ branch ช่วยให้เราทำงานแยกกัน โดยไม่กระทบกับโค้ดหลัก (main):
สร้าง branch ใหม่:
git checkout -b <branch_name>
การสลับไปยัง branch ที่มีอยู่แล้ว:
git checkout <branch_name>

7. การ Merge Branch
เมื่อเสร็จสิ้นการทำงานใน branch นั้นๆ และต้องการรวมการเปลี่ยนแปลงกลับมาที่ main:
สลับไปที่ branch หลัก (เช่น main):
git checkout main
ใช้คำสั่ง merge:
git merge <branch_name>

8. การดูสถานะของ Git
หากต้องการดูสถานะของไฟล์ที่มีการเปลี่ยนแปลงหรือยังไม่ได้ commit:
git status

9. การดูประวัติ Commit
เพื่อดูประวัติการ commit ทั้งหมดใน repository:
git log

10. การยกเลิกการเปลี่ยนแปลง
หากต้องการยกเลิกการเปลี่ยนแปลงที่ยังไม่ได้ commit:
git checkout -- <file_name>
หรือถ้าต้องการยกเลิกการ commit ล่าสุด (แต่ยังคงอยู่ในเครื่อง):
git reset --soft HEAD~1
ถ้าต้องการลบ commit ล่าสุดทั้งหมด:
git reset --hard HEAD~1

11. การ Clone Repository จาก GitHub
หากคุณต้องการทำงานกับโปรเจคที่มีอยู่แล้วบน GitHub:
Edit
git clone https://github.com/username/repository.git

สรุปการทำงานจริง
เริ่มโปรเจค: git init
เพิ่มไฟล์: git add <file>
ทำการ commit: git commit -m "message"
ส่งข้อมูลไป GitHub: git push origin main
ดึงข้อมูลจาก GitHub: git pull origin main
สร้าง branch ใหม่: git checkout -b <branch_name>
รวมการเปลี่ยนแปลง: git merge <branch_name>
การใช้งาน Git และ GitHub อย่างต่อเนื่องจะช่วยให้การทำงานร่วมกับทีมง่ายขึ้น และการติดตามการเปลี่ยนแปลงก็สามารถทำได้สะดวก
