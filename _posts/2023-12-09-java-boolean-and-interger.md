---
title : Boolean 자료형과 Interger 자료형
categories : [Dev, C#]
tags : [C#, development]
---


### ■ my Char Runner

---

> 기능 : myCharClass의 기능들을 작동시킬 수 있다.  
> ■ 메인 메서드를 선언해 줌으로서 myChar 클래스의 메서드를 작동시킬 수 있다.  
> ■ myChar 오브젝트를 new myChar 클래스에 선언해 줌으로서 charactor 파라미터를 받을 수 있다.  
> ■ System.out.println()을 선언해 줌으로 myCharClass안에 메서드들을 로그에 출력할 수 있다.

---

``` C#

public class myCharRunner {

	public static void main(String[] args) {
		
	  myChar myChar = new myChar('c');
	  System.out.println(myChar.isVowel());
	  
	  
	  // myChar에서 받은 레터럴값이 숫자인지 알파벳인지 boolean 값으로 출력
	  System.out.println(myChar.isNumber());
	  System.out.println(myChar.isAlphabet());
	  
	  // 반환되는 레터럴값이 소문자거나 대문자일 경우 엮으로 바꿔주고 출력
	  System.out.println("");
	  myChar.printLowerCaseAlphabets();
	  myChar.printUpperCaseAlphabets();
	}

}
```

### ■ my Char Classs

---

> 기능 : myCharRunner에 기능들을 구현 할 수 있다.  
> ■ 메서드를 만들어 줌 으로서  myCharRunner  메인메서드를 작동시킬 수 있다.  
> ■ myCharClass안에 다양한 메서드들을 제작할 수 있다.  
> ■ 다양한 문법을 활용해 경우의 수를 제작할 수 있다.

---

### 클래스 및 생성자 선언 

``` C# 

// 대문자 65 ~ 90

public class myChar {

	private char ch;
	
	public myChar(char ch) {
		this.ch = ch;
	}
```

-   private char 을 선언해줌으로서 charactor형 상수 선언
-   public 형으로 생성자 선언

### isVowel 메서드 

``` C# 
// 리터럴 값이 모음인지를 판단
	public boolean isVowel() {
		// a e i o u or A E I O U
		if(ch == 'a' || ch == 'e' || ch == 'i' ||ch ==  'o' ||ch ==  'u' ||
				ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U')
		return true;
		
		else
		return false;
	}
```

-   public boolean 으로 메서드 생성
-   if문을 통한 자음 판별

### isNumber 메서드 

``` C# 
	// 리터럴값의 숫자 여부 판단
	public boolean isNumber() {
			for(char i = 48; i <= 57; ++i ) {
				if(this.ch == i)
				return true;
			}	
		
			return false;
	}
```

-   for문에 유니코드 값 48(0) ~ 57(0) 을 지정해 줌으로서 this.ch 즉 지역변수가 숫자값인지 판별

### isAlparbet 메서드 

``` C#
// 리터럴값의 알파벳 여부판단
	public boolean isAlphabet() {
		 for(char i = 65; i <= 90; ++i ) 
		 {
			if(this.ch == i + 32 || this.ch == i)
			return true; 
		 }
		 return false;
	}
```

-   for문에 유니코드 값 65(a) ~ 57(b) 을 지정해 줌으로서 this.ch 즉 지역변수가 숫자값인지 판별
-   if문 내부코드 this.ch값 = i(for문 횟수) + 32를 하면 아스키 소문자 값이 나옴

### printLowerCaseAlphabets 메서드 

``` C#
public void printLowerCaseAlphabets() {
		for(char i = 65; i <= 90; ++i)
		{ 
			if(this.ch == i) {
				this.ch = (char)(this.ch + 32);
				System.out.println(ch);
				break;
			}
			
		}
	}
```

-   대문자 아스키 코드 포문을 돈 후에 if문 안으로 진입할 시 즉 아스키 코드가 대문자 일 시 + 32를 해줘 소문자로 변환
-   Sysout을 이용 출력 후 브레이크

### print UpperCase Alphabets 메서드 

``` C#
public void printUpperCaseAlphabets() {
		for(char i = 97; i <= 122; ++i )
			if(this.ch == i) {
				this.ch = (char)(this.ch - 32);
				System.out.println(ch);
				break;
			}
	
	}
```



