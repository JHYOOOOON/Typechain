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

### **🏃‍♀️ 2일차**<br/>

#### ✔️ 형식으로 배열 지정<br/>

    const hello: string[] = ["hello"];

- string[]
  - hello는 string만 들어있는 배열 형식이라는 뜻
  - 마찬가지로 class/interface도 이런 형태로 지정 가능
    <br/>
    <br/>

#### ✔️ Class<br/>

    class Block {
      public index: number;
      public hash: string;
      public previousHash: string;
      public data: string;
      public timestamp: number;
      ...
    }

- class 선언
  - interface와 다르게 javascript에서 지원
  - 접근제한자 public, private, protected로 설정 가능
    <br/>
    <br/>

#### ✔️ class 내부 static 메소드 선언<br/>

    class Block {
        ...
      static calculateBlockHash = (
        index: number,
        previousHash: string,
        timestamp: number,
        data: string
      ): string =>
        CryptoJS.SHA256(index + previousHash + timestamp + data).toString();
        ...
    }

- static 선언시 Block을 만들지 않고도 static 함수 호출 가능
  <br/>
  <br/>

#### ✔️ Class constructor<br/>

    class Block {
        ...
      constructor(
        index: number,
        hash: string,
        previousHash: string,
        data: string,
        timestamp: number
      ) {
        this.index = index;
        this.hash = hash;
        this.previousHash = previousHash;
        this.data = data;
        this.timestamp = timestamp;
      }
    }

    const newBlock: Block = new Block(
      newIndex,
      newHash,
      previousBlock.hash,
      data,
      newTimestamp
    );
