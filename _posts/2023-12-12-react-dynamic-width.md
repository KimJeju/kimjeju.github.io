---
title : "동적 웹페이즈 사이즈 계산"
categories : [Dev, react]
tags : [react,javascript]
---

### 동적 웹 페이지 크기 계산해보기

포트폴리오를 만드는 도중 OverFlow : scroll 이 두개의 컴포넌트에서 각각 작동하다보니
width가 작아짐에 따라 후자 컴포넌트가 원하는 대로 작동하지 않는 현상이 발생하였다.

이를 해결하기 위해 UseEffect를 사용하여 현재 웹페이지의 크기를 동적으로 계산하여 
조건문을 통하여 동적 컴포넌트 랜더링을 진행하였다.

---

> ■ UseEffect를 사용하여 현재 웹페이지의 크기 동적 계산
> - UseState 를 사용하여 현재 웹페이지값 상태로 저장
> - 자바 스크립트 내장함수 window를 통하여 width값을 가져왔다.

---

### 코드
```javascript

function MyCareer() {

    const [innerWidth, setInnerWidth] = useState(window.innerWidth);

    useEffect(() => {
        const resizeListener = () => {
            setInnerWidth(window.innerWidth);
        };
        window.addEventListener("resize", resizeListener);
    });

    console.log("innerWidth", innerWidth);

    if (innerWidth < 800) {
        return (
            <CareerContainerMaxWidth800 className="openContainer">
                <About />
                <Position />
                <Stack />
            </CareerContainerMaxWidth800>
        )
    } else {
        return (
            <CareerContainer className="openContainer">
                <About />
                <Position />
                <Stack />
            </CareerContainer>
        )
    }


}

export default MyCareer

```

