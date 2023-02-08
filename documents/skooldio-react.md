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
  <p align="center"><i>Concept React</i></p>
  <br/>

  ![](/documents/images/botton-state.PNG)
  <p align="center"><i>ตัวอย่าง Botton State</i></p>
  <br/>

## **<mark class="header">JSX</mark>**
JSX(JavaScript XML) — ทำให้เราสามารถเขียน HTML อยู่ใน JavaScript ได้เลย 

  ![](/documents/images/jsx.PNG)
  <br/>

จุดเด่นหลักๆ ของ JSX คือ เราสามารถใส่ Expression เข้าไปได้ในโค้ดของเรา

> Expression คือ Result Out ออกมาเป็นค่าได้ ไม่ว่าจะเป็นค่าคงที่, ตัวแปร หรือการใช้ฟังชันก์ ซึ่งเวลาเราจะเรียกใช้คือเราจะใส่ {...} แล้วข้างในก็จะเป็น Expression ที่เราเรียกใช้

  ![](/documents/images/expression.PNG)
  <br/>

  ![](/documents/images/conditional.PNG)
   <p align="center"><i>การใช้ Syntax JavaScript ในการทำ Conditional</i></p>
  <br/>

  ![](/documents/images/loop.PNG)
   <p align="center"><i>การใช้ Syntax JavaScript ในการทำ Loop จุดสำคัญคือการใส่ Key และต้องไม่ซ้ำกัน</i></p>
  <br/>


## **<mark class="header">React Element & Component</mark>**
Component และ Element — React Element เป็นสิ่งที่เราบอกว่าเราต้องการให้ DOM หรือ HTML หน้าตาเป็นยังไงและแสดงผลอย่างไร ซึ่ง React Element จะถูกเขียนได้โดย Syntax JSX 

  ![](/documents/images/element-and-component.PNG)
  <br/>

ตัว React Element จะถูกสร้างมาจากไหน? ก็คือมันจะถูกสร้างมากจาก React Component โดยตัว React Compoenent จะมีค่าอยู่ 2 ค่าที่สามารถเปลี่ยนแปลงได้คือ

1. ค่า State ในตัวมันเอง
2. ค่า Props ที่รับเข้ามาจากด้ายนอก


## **<mark class="header">State & Props</mark>**
ใน React มีวแปรที่ใช้ในการ Render อยู่ 2 อัน ได้แก่ <mark>State</mark> และ <mark>Props</mark> โดยสองตัวนี้แตกต่างกันคือ State เป็นตัวแปรภายในของ Component เอง แปลว่า**สามารถเปลี่ยนแปลงแก้ไขได้** ส่วน Props เป็นสิ่งที่รับเข้ามาจาก Compoment ด้านนอก แปลว่าเรา**ไม่สามารถเปลี่ยนแปลงแก้ไขได้**

  ![](/documents/images/state-and-props.PNG)
  <br/>

<mark>Props</mark> หรือชื่อเต็มๆมันคือ <mark>Properties</mark> หากเปรียบกับ HTML แล้ว ตัว Props จะเป็นคล้ายๆ attributes ของ HTML ดัง เช่น <mark>src, href หรือ class</mark>

  ![](/documents/images/props.PNG)
  <p align="center"><i>ตัวอย่างการใช้ Props</i></p>
  <br/>
  
ตัวอย่างในการส่ง <mark>Props</mark> ในรูปแบบของ <mark>Parameter</mark>
```js
export default class TestProps extends Component {

    render() {
        return (<Passprops name="NerdKung"/>)
    }
}

class Passprops extends Component {
    render() {
        return (
            <div>
                <h1>Hello : { this.props.name }</h1>
            </div>
        )
    }
}
```

ตัวอย่างในการส่ง <mark>Props</mark> ในรูปแบบของ <mark>Function</mark>
```js
export default class TestProps extends Component {
    Alert = () => {
        alert("Hello World!");
    }
    render() {
        return (<Passprops name="NerdKung" handleAlert={ this.Alert }/>)
    }
}

class Passprops extends Component {
    render(){
        return (
            <div>
                <h1>Helle : { this.props.name }</h1>
                <button onClick = { this.props.handleAlert }>Click</button>
            </div>
        )
    }
}
```
<mark>State</mark> นั้นเสมือนเป็น data ที่มีการ**ใช้แค่ภายใน Component นั้นๆ** 

มันคือ**ส่วนประกอบการทำงานภายในของ Components** เก็บข้อมูลและ**ยังสามารเปลี่ยนแปลงระหว่างการทำงาน**ได้อีกด้วย

<mark>State</mark> เป็น JavaScript Object        
<mark>Default State</mark> ด้วยคำสั่ง <mark>this.state = {}</mark>

```js
export default class TestState extends Component{
    constructor(props) {
        super(props);
        // default state
        this.state = {name: "Hello World!"};
    }

    render(){
        return (<h1>{this.state.name}</h1>);  
    }
}
```

<mark>State</mark> มีหน้าที่ default state แค่นั้น หัวใจของมันคือการ <mark>setState</mark> 

```js
class MyComponent extends React.Component {
  handleClick = e => {
    this.setState({ clicked: true })
  }

  render() {
    return (
      <a href="#" onClick={this.handleClick}>
        Click me
      </a>
    )
  }
}
```

  ![](/documents/images/state.PNG)
  <p align="center"><i>ตัวอย่างการใช้ State</i></p>
  <br/>

## **<mark class="header">Virtual DOM</mark>**
- การแก้ไข DOM จะต้องทำการวาด (render) DOM ที่ทำการแก้ไขทั้งหมด ซึ่งใช้เวลานาน
- React มีวิธีาแก้ปัญหานี้ เรียกว่า Vitual DOM
- เป็ย algorithm ในการ update เฉพาะ DOM node ที่มีการเปลี่ยนแปลงข้อมูลเท่านั้น 

## **<mark class="header">Creating React App Using create-react-app</mark>**
React Component — จะประกอบไปด้วย Class และสิ่งที่ทุก Component จะต้องมีคือ render() เป็นฟังชันก์ที่บอกว่า Component นี้จะ return HTML หน้าตาเป็นยังไงออกมา