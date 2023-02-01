<link href="../style.css" rel="stylesheet"></link>

# React คืออะไร? 
## **<mark class="header">3 คุณสมบัตรของ React**</mark>
1. React เป็น <mark>UI Library</mark> ไม่ใช่ Framework — React เป็น Library ที่จัดการในส่วนของ View ต่างจาก Framework อย่าง Angular ที่มีการทำ Model, Routing และอื่นๆ ให้ด้วย  ดังนั้นถ้าเราอยากได้ของที่เป็น Routing หรือส่วนเสริมอื่นๆ ด้วย เราก็ต้องใช้ library อื่นเข้ามาเสริม เช่น <mark>React Router</mark>, <mark>Redux</mark> หรือ <mark>Style Component</mark> เป็นต้น

> <i><mark>Framework</mark> คือ ความหมายของ framework คือโครงร่างซึ่งก็ค่อนข้างตรงตัวในที่นี่ทีเดียว เพราะมันคือการเอาโครงร่างโค้ดของคนอื่นมาใช้กับงานของเรา ซึ่งจะทำให้เรา**ประหยัดเวลา**ขึ้นมากๆ เนื่องจากเรา**ไม่ต้องเริ่มคิดเองเขียนเองตั้งแต่ต้น**.  
> <mark>Library</mark> คือ
ความหมายของ library ตรงตัวเลยก็คือห้องสมุด ซึ่งมันก็จริงในแง่ของการโค้ดเพราะ library คือ**การรวบรวมชุดคำสั่งโค้ดที่จะทำให้การโค้ดของเรานั้นง่ายขึ้น** เราไม่จำเป็นต้องรู้ว่าชุดคำสั่งโค้ดนั้นข้างในทำงานยังไง แค่รู้ว่าใช้ยังไงก็พอ.</i>

2. React มีลักษณะเป็น <mark>Component-based</mark> — ข้อดีของ Library เป็น Component-based คือง่ายต่อการนำมาใช้งาน (Reusable) เช่น เราเขียน Component Button ขึ้นมา เราก็สามารถนำ Component นี้ไปใช้งานในหน้าอื่นๆได้ ข้อดีก็คือโค้ดของเราจะไม่ชนกันหมายถึงของที่เราเขียนใน Component ไหนๆ ก็จะอยู่ใน Component นั้นๆ และไม่มีการรบกวนของ Component อื่นๆโดยไม่ได้ตั้งใจ 

> <i><mark>**[Component-based Design](https://blog.skooldio.com/ui-design-component-based-design/)**</mark> คือการมองแยกส่วนประกอบต่างๆ ที่ร่วมกันเป็นหน้าเว็บไซต์หรือแอปฯ ที่เราออกแบบว่ามีส่วนประกอบมาจากอะไรบ้าง</i>

3. API ของ React เป็นแบบ <mark>Declarative</mark> — การใช้งาน React นั้น แทนที่จะบอกว่าต้องทำอย่างไร (Imperative) เราอยากจะบอกว่า<mark>อยากได้ผลลัพธ์อะไร</mark> ซึ่งเป็นการเขียนโปรแกรมแบบ Declarative สามารถอ่านเรื่องของ Declarative และ Imperative [เพิ่มเติมได้ที่](https://codeburst.io/declarative-vs-imperative-programming-a8a7c93d9ad2)

    - <mark>Imperative programming</mark> คือรูปแบบการเขียนโปรแกรมที่โฟกัสที่ **HOW** กล่าวคืออธิบายว่าโปรแกรมทำงานอย่างไร โดยโค้ดที่เขียนจะประกอบไปด้วย Statements หลายอันทำงานร่วมกันเป็นขั้นเป็นตอน เพื่อไปสู่เป้าหมายที่ต้องการ (reach a certain goal) 
    - <mark>Declarative programming</mark> คือรูปแบบการเขียนโปรแกรมที่โฟกัสที่ **WHAT** กล่าวคือสั่งเพียงแค่ว่าโปรแกรมต้องทำอะไร โดยไม่ลงไปถึงรายละเอียดวิธีการทำงาน

> <mark>Imperative approach</mark> — “หุงข้าวเตรียมขึ้นมาจานนึง แล้วเอาไก่ส่วนสะโพกไปหมักเครื่องปรุง นำไปชุบแป้ง แล้วลงทอดในหม้อน้ำมัน จนสุกกรอบ เอาขึ้นมาสับเป็นชิ้นเล็กพอดีคำ ละยำรวมกับขึ้นช่าย หัวหอม หอมแดง ข้าวคั่ว ผงชูรส เสร็จแล้วก็เอาไปโปะบนข้าว พร้อมเสิร์ฟ” 
> <mark>Declarative approach</mark> — “ขอข้าวยำไก่แซ่บหนึ่งจานครับ”

# React Concepts and Features

## **<mark class="header">Main concept</mark>**
Concept หลักของ React — <mark>UI เป็น Function ของ State</mark> นั่นหมายความว่าถ้าเราใส่ Input อะไรเข้าไปเราก็จะได้ Output เหมือนเดิมเสมอ

  ![](/documents/images/concept-react.PNG)
  <center><i>Concept React</i></center>
  <br/>

  ![](/documents/images/botton-state.PNG)
  <center><i>ตัวอย่าง Botton S</i></center>
  <br/>

## **<mark class="header">JSX</mark>**
JSX(JavaScript XML) — ทำให้เราสามารถเขียน HTML อยู่ใน JavaScript ได้เลย 

  ![](/documents/images/jsx.PNG)
  <br/>