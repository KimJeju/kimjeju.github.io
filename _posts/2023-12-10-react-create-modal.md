---
title : "리액트 모달 만들어보기"
categories : [Dev, react]
tags : [react,javascript]
---

### 포트폴리오 경력사항 작성을 위한 모달 창 구현해보기

---

> ■ 상태 라이브러리를 통한 show 모달 상태 관리
> - UseState 를 사용하여 모달에 show 여부를 저장
> - showModal 함수와 button을 통해 show modal 이벤트 트리거 발생 시키기

---

### 코드
```javascript

function Intro()
{
    //Modal 영역
    const [ openModal, setOpenModal ] = useState(false);

    //모달의 open, hide 속성을 담당할 메서드
    function showModal(){
        //console.log 로 이벤트 발생 여부 확인해보기
        alert("모달 이벤트 발생");
        setOpenModal(true);
    }

    return (
        <div className="intro-body">
            <div className="intro-left-body">
                    ㅎㅇ
            </div>
            <div className="intro-right-body">
                    <button onClick={showModal}>View More</button>
                     
                    //oe
                     {openModal && <ModalPage setOpenModal={setOpenModal} />}

            </div>
        </div>
    )
}

```

```javascript
import styled from "styled-components";

const Button = styled.button`
    background-color : #3A00F5; 
    color : white;
    border : none;
    width : 10rem;
    height : 50px;
    font-size : 15px;
    transition : 0.5s;
    margin-top : 20px;
    border-radius : 5px;

    &:hover{
        background-color : white;
        border-radius : 25px;
        color : black;
    }
`

```


---

> ■ 모달페이지 ( 자식 요소 ) 에 props로 상태 전달 및 창 띄우기
> - 필자의 경우 ModalPage 라는 js 페이지를 하나만든 후 prop로 Modal 상태 전달
> - close Modal 이라는 함수를 버튼 이벤트로 등록해 X 버튼을 누를 시 부모요소에게 false 를 전달 이 후 모달창이 꺼지도록 함
> - style component 를 사용해 modal 최상단에 위치

---

### 코드
```javascript

import { useState } from "react"
import ModalPage from "../Modal/ModalPage";


function ModalPage({ setOpenModal }) {

    function closeModal() {
        setOpenModal(false);
    }

    return (
        <Background>
            <OpenContainer>
                <Close onClick={closeModal}> X </Close>
            </OpenContainer>
        </Background>
    )
}
```

### 스타일
```javascript

import styled from "styled-components";

//뒷배경 어둡게 해주기
const Background = styled.div`
    position : fixed;
    top : 0;
    left : 0;
    width : 100vw;
    height : 100vh;
    background-color : rgba(0,0,0,0.8);
    z-index : 100;
`

//모달 최상단 위치 시켜주기
const OpenContainer = styled.div`
    width: 40rem;
    height : 40rem;
    background-color : black;

    //최상단 위치
    z-index : 999;

    //가운데 위치 시키기
    position : absolute;
    top : 50%;
    left : 50%;
    transform : translate(-50%, -50%);

    border : 1px solid white;


    transition : 0.5s;

    &:hover{
        box-shadow: 10px 10px white;
    }
`


//닫기 버튼
const Close = styled.button`
    // 버튼 오른쪽 최상단에 위치하도록 만들어주기
    position : absolute;
    top : 10px;
    right : 10px;
    
    //디자인 영역
    transition : 0.5s;
    width : 25px;
    height : 25px;
    transition : 0.5s;
    background-color : #3A00F5;
    color : white;
    border : none;

    &:hover{
        background-color : white;
        color : black;
    }
`

```




