---
layout : single
title : "엑셀 참조(reference)"
---

# 엑셀 상대 참조, 절대 참조, 혼합 참조 

## 0. 참조

"D2에 수식(B2+C2)을 입력하면 D2는 B2와 C2를 **참조**한다"

<img src="https://blog.kakaocdn.net/dn/b1GkZh/btqD1OUSLcM/KwTErVF9tkpNBJFQ1Rr03K/img.gif" alt="img" style="zoom:33%;" />

## 1. 상대 참조

입력한 식을 복사-붙여 넣기를 했을 때 **참조된 셀들도 따라서 이동하는 상태이다.**

<img src="https://blog.kakaocdn.net/dn/bsLJ3I/btqD1O1FmCp/ovWHMh1KK5K5fupFbRni70/img.png" alt="img" style="zoom:33%;" />

<img src="https://blog.kakaocdn.net/dn/dlf4uv/btqD1p8Xtqo/qwKOb494MLfZUlHGGU96jk/img.gif" alt="img" style="zoom:33%;" />

## 2. 절대 참조

참조된 셀들이 따라 이동하지 않고, 고정시킨다.

**식에 F4를 1번 누르면 $표시** 2개가 생긴다. 여기서 $표시는 자물쇠라고 생각하자.

<img src="https://blog.kakaocdn.net/dn/MZ8UI/btqDZNpkDY2/lYQRk1iKMxtg9HwOluSzVk/img.gif" alt="img" style="zoom:33%;" />

<img src="https://blog.kakaocdn.net/dn/denS0t/btqDYvbCIaz/AwQTpihFQL6okhH6gnE6cK/img.png" alt="img" style="zoom:25%;" /><img src="https://blog.kakaocdn.net/dn/kLo0X/btqDYujxRNw/FvgCrbz9DKFbJJrXiWV9k1/img.png" alt="img" style="zoom:25%;" />

이제 참조된 셀은 고정이 되어 어느 곳에 붙여 넣기를 해도 B2+C2의 값이 나오게 된다.

## 3. 혼합 참조_행 고정시키기

**F4를 2번 누르면 숫자 앞에만 $표시**가 생긴다. 행을 고정시킨다는 의미이다.

<img src="https://blog.kakaocdn.net/dn/ei46rJ/btqD1q02zMh/NfTZrLjCmrqlKTkS2KldEK/img.gif" alt="img" style="zoom:33%;" />

오른쪽과 아래쪽에 각각 붙여넣기를 해보면 오른쪽만 다른 값이 나온다.

옆으로 복사하면 참조된 셀도 따라 움직이고, 아래로 복사하면 참조된 셀이 고정된다.

<img src="https://blog.kakaocdn.net/dn/EvAmW/btqD0M4lvZE/B5o8h7XVMfW6S263iZEKD1/img.gif" alt="img" style="zoom: 33%;" />

## 4. 혼합 참조_열 고정시키기



**F4를 3번 누르면 ** **문자 앞에만 $표시**가 된다. 열을 고정시킨다는 의미이다.

<img src="https://blog.kakaocdn.net/dn/BNLDR/btqD1Nob4B4/dK1xNbLObQmIKuTvKJg6Ck/img.gif" alt="img" style="zoom:33%;" />

오른쪽과 아래쪽에 각각 붙여넣기를 해보면 아래쪽만 다른 값이 나온다.

옆으로 복사하면 참조된 셀이 고정되고, 아래로 복사하면 참조된 셀이 따라 움직인다.

<img src="https://blog.kakaocdn.net/dn/zWf8h/btqD2v8o2Aw/OqKSHAyW3dV90qsoX66dv0/img.gif" alt="img" style="zoom:33%;" />

## 5. 요약

F4를 1번 누르면 - $C$2 **(절대 참조)**

F4를 두 번 누르면 - C$2 **(혼합 참조 - 행 고정)**

F4를 세 번 누르면 - $C2 **(혼합 참조 - 열 고정)**

F4를 네 번 누르면 - C2 **(다시 상대 참조)**

