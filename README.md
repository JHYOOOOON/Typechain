# Typechain

### **✍️ Description**

Study Typescript with Nomad Coders course
<br/>
<br/>

### **🏃‍♀️ 1일차**<br/>

#### ✔️ 매개변수 자료형 지정

    const Hello = (name: String): void => {
        console.log(`Hello, ${name}!`)
    }

- name: String
  - 매개변수로 String형만 받겠다는 의미
- : void
  - return이 없다는 뜻
  - : string이면 string형 자료를 return 한다는 뜻
    <br/>
    <br/>

#### ✔️ 매개변수 선택

    const Hello = (name?: String): void => {
        console.log(`Hello, ${name}`)
    }

- name? (← 매개변수 뒤 물음표)
  - 매개변수(name)가 있어도 되고 없어도 된다는 뜻
  - 매개변수가 들어오지 않았을 때는 undefined로 뜸
    <br/>
    <br/>

#### ✔️ 매개변수를 Object로 보내기

1️⃣ Interface 선언<br/>

    interface Human {
        name: string;
        age: string;
    }

2️⃣ Interface에 맞는 Object 선언

    const person = {
        name: "JHYOON",
        job: "frontend developer"
    }

3️⃣ 매개변수로 넘기기

    const Hello = (person: Human): void => {
         console.log(`Hello, ${person.name}! You are ${person.job}:)`);
    }
