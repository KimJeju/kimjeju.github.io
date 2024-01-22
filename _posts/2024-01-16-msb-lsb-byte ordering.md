---
title : "비트와 바이트, MSB, LSB"
categories : [Computer, cs]
tags : [os, cs]
---


### MSB (촤싱위 빌드), LSB (최하위 빌드)
> - MSB : Most Significan Bit 라 하며 가장 왼쪽에 있는 비트이다, 
숫자의 크기에 가장 큰 영향을 미친다.
> - LSB : Least Significan Bit 라 하며 가장 오른쪽에 있는 비트이다,숫자의 가장 작은 영향을 미친다.
>
> |MSB|내용|설명|설명|설명|설명|설명|설명|LSB|
> |---|---|---|---|---|---|---|---|
> |0|1|0|0|0|1|0|0|1|

### Byte Ordering (바이트 오더링)
> - 바이트 이상의 데이터는 메모리에 연속적으로 저장된다. 이때 각 바이트가 메모리에 정렬되는 방식을 Byte Ordering 이라 한다.
>> - 바이트 오더링의 데이터 저장 두가지 방식
>> - - Big Endian (빅 에디안)
>> - - Little Endian (리틀 에디안)

> Big Endian
> - 큰 바이트부터 낮은 주소로 저장됨

> Little Endian
> - 작은 바이트부터 큰 주소로 저장됨

> Byte Ordering 비트의 순서가 아닌 바이트의 순서를 고려하는 것으로, 바이트 내 비트의 순서는 동일하고 바이트의 순서만 달라진다.

