# Explain Code 5: JavaScript Fundamentals

## 01-variables.js - 6. Challenge: Create a Person Object

โค้ดนี้เป็นการสร้าง object ชื่อ student ในภาษา JavaScript เพื่อเก็บข้อมูลนักเรียน เช่น ชื่อ นามสกุล อายุ เกรดเฉลี่ย และรายวิชา จากนั้นมีการสร้างฟังก์ชันภายใน object คือ `getFullName()` สำหรับรวมชื่อและนามสกุล และ `getInfo()` สำหรับแสดงข้อมูลรวมทั้งหมด ``เมื่อใช้`console.log()`โปรแกรมจะแสดง object ทั้งหมดออกมาก่อน ต่อด้วยชื่อเต็มจาก getFullName() ข้อมูลรวมจาก getInfo() และรายวิชาที่เรียน โดยใช้ .join(", ") รวม array ให้เป็นข้อความเดียว

สรุปคือ โค้ดนี้สาธิตการใช้ object, method และการเข้าถึงข้อมูลภายใน object ด้วย this พร้อมแสดงผลออกทางหน้าจออย่างเป็นระบบ

### ผลลัพธ์

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

## 02-functions.js - 8. Returning Objects, 9. Function as Parameter (Callback)

โค้ดส่วนที่ 8 เป็นการสาธิตการ คืนค่าเป็น `object` จากฟังก์ชัน `(Returning Objects)` โดยฟังก์ชัน `createUser()` รับค่า ชื่อ นามสกุล และอายุ จากนั้นนำข้อมูลเหล่านี้ไปสร้างเป็น object ผู้ใช้ใหม่ พร้อมสร้างอีเมลอัตโนมัติจากชื่อและนามสกุล โดยแปลงเป็นตัวพิมพ์เล็ก และคั่นด้วยจุด นอกจากนี้ยังมี `method getFullName()` สำหรับรวมชื่อ-นามสกุล และ `getAge()` สำหรับคืนค่าอายุ เมื่อเรียกใช้ฟังก์ชัน

โค้ดส่วนที่ 9 เป็นการสาธิตการใช้ `Callback Function` โดยฟังก์ชัน `processArray()` รับ array และฟังก์ชันอีกตัวหนึ่งเป็นพารามิเตอร์ จากนั้นวนลูปนำค่าทุกตัวใน array ไปประมวลผลผ่าน callback แล้วเก็บผลลัพธ์ไว้ใน array ใหม่ เช่น เมื่อส่งฟังก์ชันคูณ 2 เข้าไป จะได้ผลลัพธ์เป็นตัวเลขที่ถูกคูณสองทั้งหมด และเมื่อส่งฟังก์ชันยกกำลังสองเข้าไป จะได้ค่ากำลังสองของตัวเลขแต่ละตัว

### ผลลัพธ์

Returning Objects:  
 {
irstName: 'John',  
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

## 03-control-flow.js - 5. Short-Circuit Evaluation, 7. Form Validation

โค้ดนี้แสดงหลักการ Short-Circuit Evaluation ใน JavaScript โดยเริ่มจากกำหนด user เป็น object และ admin เป็น null จากนั้นใช้คำสั่ง
admin?.name || user.name || "Anonymous"
โปรแกรมจะตรวจจากซ้ายไปขวา เมื่อ admin เป็น null จึงได้ค่า undefined แล้วข้ามไปใช้ user.name ซึ่งเป็น "John" ทำให้หยุดทันทีและนำค่านี้ไปใช้เป็นผลลัพธ์ต่อมาใช้คำสั่ง
user && user.profile
เมื่อ user มีค่า true โปรแกรมจึงไปตรวจ user.profile ต่อ แต่ไม่มีข้อมูลนี้อยู่ จึงได้ค่า undefined
สรุป
|| หยุดเมื่อเจอค่า true, && หยุดเมื่อเจอค่า false และ ?. ใช้ป้องกัน error จากค่า null/undefined

## ผลลัพธ์

Short-Circuit Evaluation:  
User name: John  
User profile: undefined

Form Validation:  
Valid user: { isValid: true, errors: [] }  
Invalid user: { isValid: false, errors: [ "Name must be at least 3 characters", "Valid email is required", "Must be 18 or older", "Password must be at least 6 characters", "Must agree to terms" ] }

## 04-loops.js - 9. Chaining methods, 10. Challenge: Student Grades

โค้ดส่วนที่ 9 เป็นการสาธิตการใช้ Method Chaining ในภาษา JavaScript โดยนำเมธอดหลายตัวมาเรียกต่อกันในบรรทัดเดียว เริ่มจากใช้ `filter() `เพื่อคัดเฉพาะเลขคู่ จากนั้นใช้ `map()` แปลงตัวเลขเป็นข้อความแสดงค่ากำลังสอง และใช้ `join()` รวมข้อมูลทั้งหมดเป็นสตริงเดียว นอกจากนี้ยังมีการใช้ `reduce()`เพื่อหาผลรวมของตัวเลข แล้วนำไปคำนวณค่าเฉลี่ยโดยหารด้วยจำนวนสมาชิกใน array

โค้ดส่วนที่ 10 เป็นการวิเคราะห์ข้อมูลนักเรียนจาก array ของ object โดยใช้ `map()` เพื่อดึงรายชื่อทั้งหมด ใช้ `filter()`คัดกรองนักเรียนที่ได้คะแนนตั้งแต่ 85 ขึ้นไป และใช้ `reduce()` เพื่อคำนวณค่าเฉลี่ยของคะแนนทั้งห้อง รวมถึงใช้ reduce() อีกครั้งเพื่อหานักเรียนที่ได้คะแนนสูงสุด สุดท้ายมีการสร้างสรุปข้อมูลโดยเพิ่มเกรดให้แต่ละคนด้วย `map()` จัดเรียงคะแนนจากมากไปน้อยด้วย `sort()` และแสดงผลรายชื่อนักเรียนทีละคนด้วย `forEach()`

## ผลลัพธ์

Method chaining:
Even numbers squared: 2²=4, 4²=16, 6²=36, 8²=64, 10²=100
Average: 30

Challenge: Student Analysis
Students: [
{ name: 'Alice', score: 95 },
{ name: 'Bob', score: 75 },
{ name: 'Charlie', score: 85 },
{ name: 'Diana', score: 92 },
{ name: 'Eve', score: 88 }
]
Names: Alice, Bob, Charlie, Diana, Eve
High scorers: Alice (95), Charlie (85), Diana (92), Eve (88)
Class average: 87.00
Top scorer: Alice (95)
Summary (sorted):
Alice: 95 (A)
Diana: 92 (A)
Eve: 88 (B)
Charlie: 85 (B)
Bob: 75 (C)

✅ Activity 4 completed!

## 05-integration.js - Activity 5: Integration - Quiz Application

โค้ดนี้เป็นโปรแกรม Quiz ที่เริ่มจากแสดงชื่อแอป จากนั้นกำหนดชุดคำถามในรูปแบบ array ของ object แล้วสร้างตัวแปร results เพื่อเก็บผลลัพธ์ โปรแกรมใช้ `forEach()` วนลูปแต่ละข้อ สุ่มคำตอบผู้ใช้ด้วย `Math.random()` ตรวจว่าถูกหรือไม่ แล้วบันทึกข้อมูลลงใน results
เมื่อทำครบทุกข้อ โปรแกรมจะแสดงผลลัพธ์รายข้อ นับจำนวนข้อที่ถูกด้วย `filter()` คำนวณคะแนนเป็นเปอร์เซ็นต์ แล้วกำหนดเกรดด้วยเงื่อนไข `if-else` ต่อมาจะแสดง Feedback และสถิติการทำแบบทดสอบ สุดท้ายใช้ `reduce()` สรุปจำนวนข้อที่ถูกและผิดก่อนจบการทำงาน

## ผลลัพธ์

🎯🎯 === QUIZ APPLICATION === 🎯🎯  
QUIZ RESULTS:  
Q1: What is 5 + 3?  
Your answer: 8  
✅ CORRECT

Q2: What is the capital of Thailand?  
Your answer: Phuket  
Correct answer: Bangkok  
❌ WRONG

Q3: What is the largest planet?  
Your answer: Jupiter  
✅ CORRECT

Q4: What is 2^8?  
Your answer: 256  
✅ CORRECT

Q5: Which is NOT a JavaScript data type?  
Your answer: class  
❌ WRONG

FINAL SCORE: 3/5 (60.0%)  
GRADE: D

FEEDBACK:  
📚📚 Good effort. Review the material and try again.

📊📊 STATISTICS:  
Total questions: 5  
Correct: 3  
Incorrect: 2  
Success rate: 60.0%

Answer breakdown:  
✅ Correct: 3  
❌ Incorrect: 2
