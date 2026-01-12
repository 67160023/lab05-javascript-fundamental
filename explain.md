## Explain Code 5: JavaScript Fundamentals

# 01-variables.js - 6. Challenge: Create a Person Object

โค้ดนี้เป็นการสร้าง object ชื่อ student ในภาษา JavaScript เพื่อเก็บข้อมูลนักเรียน เช่น ชื่อ นามสกุล อายุ เกรดเฉลี่ย และรายวิชา จากนั้นมีการสร้างฟังก์ชันภายใน object คือ `getFullName()` สำหรับรวมชื่อและนามสกุล และ `getInfo()` สำหรับแสดงข้อมูลรวมทั้งหมด ``เมื่อใช้`console.log()`โปรแกรมจะแสดง object ทั้งหมดออกมาก่อน ต่อด้วยชื่อเต็มจาก getFullName() ข้อมูลรวมจาก getInfo() และรายวิชาที่เรียน โดยใช้ .join(", ") รวม array ให้เป็นข้อความเดียว

สรุปคือ โค้ดนี้สาธิตการใช้ object, method และการเข้าถึงข้อมูลภายใน object ด้วย this พร้อมแสดงผลออกทางหน้าจออย่างเป็นระบบ

# ผลลัพธ์

=== Challenge: Person Object ===
Student object:
{
firstName: 'Alice',
lastName: 'Smith',
age: 20,
gpa: 3.8,
courses: [ 'HTML', 'CSS', 'JavaScript' ],
isActive: true,
getFullName: [Function: getFullName],
getInfo: [Function: getInfo]
}
Full name: Alice Smith
Info: Alice Smith, Age: 20, GPA: 3.8
Courses: HTML, CSS, JavaScript

# 02-functions.js - 8. Returning Objects, 9. Function as Parameter (Callback)

โค้ดส่วนที่ 8 เป็นการสาธิตการ คืนค่าเป็น `object` จากฟังก์ชัน (Returning Objects) โดยฟังก์ชัน `createUser()` รับค่า ชื่อ นามสกุล และอายุ จากนั้นนำข้อมูลเหล่านี้ไปสร้างเป็น object ผู้ใช้ใหม่ พร้อมสร้างอีเมลอัตโนมัติจากชื่อและนามสกุล โดยแปลงเป็นตัวพิมพ์เล็ก และคั่นด้วยจุด นอกจากนี้ยังมี `method getFullName()` สำหรับรวมชื่อ-นามสกุล และ `getAge()` สำหรับคืนค่าอายุ เมื่อเรียกใช้ฟังก์ชัน
โค้ดส่วนที่ 9 เป็นการสาธิตการใช้ `Callback Function` โดยฟังก์ชัน `processArray()` รับ array และฟังก์ชันอีกตัวหนึ่งเป็นพารามิเตอร์ จากนั้นวนลูปนำค่าทุกตัวใน array ไปประมวลผลผ่าน callback แล้วเก็บผลลัพธ์ไว้ใน array ใหม่ เช่น เมื่อส่งฟังก์ชันคูณ 2 เข้าไป จะได้ผลลัพธ์เป็นตัวเลขที่ถูกคูณสองทั้งหมด และเมื่อส่งฟังก์ชันยกกำลังสองเข้าไป จะได้ค่ากำลังสองของตัวเลขแต่ละตัว

# ผลลัพธ์

Returning Objects:
{
firstName: 'John',
lastName: 'Doe',
age: 30,
email: 'john.doe@example.com',
getFullName: [Function: getFullName],
getAge: [Function: getAge]
}
Email: john.doe@example.com
Full name: John Doe

Callback Function:
Original: [ 1, 2, 3, 4, 5 ]
Doubled: [ 2, 4, 6, 8, 10 ]
Squared: [ 1, 4, 9, 16, 25 ]
