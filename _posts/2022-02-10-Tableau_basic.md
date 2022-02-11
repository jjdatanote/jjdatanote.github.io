---
layout : single
title : "태블로 기초"
---


# **<u>태블로 기본 개념</u>**



##   **1. 데이터 불러오기**

**목표** : 엑셀 슈퍼스토어 샘플 데이터를 불러와 데이터를 시각화

1. 데이터를 엑셀 데이터로 연결해 PC에 있는 슈퍼스토어-샘플 데이터를 불러온다.

2. 주문과 관련된 반품 데이터를 시각화해보고자 두개의 테이블을 JOIN으로 연결해줍니다.

![img](https://blog.kakaocdn.net/dn/yqfuS/btqZyvVqyZw/MPGg778pK7bilaPa7fiBk0/img.png)

3. 현재 그림에서 두개의 테이블을 PK를 기준으로 left, right, inner, outer 등 원하는 join 방식을 설정할 수 있다.

(추가적으로 또 다른 DB에 저장된 데이터를 연결하고자 한다면 연결 부분의 추가를 클릭해 불러올 수 있다.)

(태블로의 장점 중 하나는 **서로 다른 DB에 저장된 데이터를 join 시킬 수 있다.**)

4. 주문에 관련된 데이터만을 다루고자 다시 반품 테이블의 데이터는 제거한다.

5. 데이터 준비가 끝났으니 아래 그림처럼 데이터 작업 시트로 이동한다.

   (좌측 하단의 시트1으로 이동하면 이전에 작업했던 데이터가 추가된 작업시트로 변경된다.)

   ![img](https://blog.kakaocdn.net/dn/EMRg6/btqZEBgdRmE/3PwPRVNe8oc7M9rvlCOWq0/img.png)

   

   ## **2. 데이터 작업하기**

![img](https://blog.kakaocdn.net/dn/bpxyiO/btqZvOgCpnU/ceyVu3CDTegKxGoKpNTNK0/img.png)

위의 그림과 같이 화면 좌측에서 데이터의 필드명을 확인할 수 있다.



##  **2.1 측정값**

데이터 중 **측정값**의 특징은 **집계**하거나 **계산**할 수 있다는 점이다.

예를 들어, 측정값 매출 필드를 더블클릭한다.

![img](https://blog.kakaocdn.net/dn/QTajF/btqZBc2mML8/c29DEkB0kjehp9xMG967Y0/img.png)

위의 그림처럼 하나의 막대 그래프가 그려지게 되는데 그림 상단의 레이블 표시 버튼(T)을 클릭하여 매출액을 확인해보면 전체 매출액이 **집계**되어 **총 합계 매출액**이 약 35억 정도가 된다는 것을 알 수 있다.



##   **2.2 차원값이란?**

(테이블)**차원**의 경우는 **범주정보**이다. 즉, 집계는 **불가능**하지만 **측정값**을 **분할**하는 역할을 한다.

예를 들어, 제품 대분류 별 매출정보를 그린다.

![img](https://blog.kakaocdn.net/dn/bmP6RO/btqZBc89tNu/ZaRzqM3c9rWkkCf7lhsINK/img.png)

**매출액(측정값)의 전체**가 **집계**된 하나의 바차트가 **대분류(차원)**로 나누어져 가구, 기술, 사무용품으로 막대 그래프가 3개로 **분할**된 것을 확인할 수 있다. 이처럼 **차원 데이터**는 **범주형 데이터**로 **측정값(수치)데이터**를 **분할**할 때 사용한다.



이번에는 **차원**에서 **중분류**를 선택에 열로 이동시킨다.

![img](https://blog.kakaocdn.net/dn/265Xm/btqZtzYmiGK/KdhuivQ8Z135kNZhWtRmyK/img.png)

위의 그림처럼 **대분류, 중분류 별**로 나누어진 **매출액의 집계 상태**가 막대 그래프로 그려진다.

위 차트를 통해 **제품군 별** 가장 높은 매출액을 보이는 제품은 의자라는 것을 알 수 있다.



##  **2.3 열과 행 바꾸기**

상단 메뉴에서 열과 행 바꾸기를 클릭하면 아래의 그림처럼 **x축과 y축의 데이터가 바뀌어 행방향**으로 뻗어진 막대 를 확인할 수 있다.

![img](https://blog.kakaocdn.net/dn/byfS1Q/btqZtAQw6iz/8rn0yKhNMv6pAcPgMJ8T01/img.png)





##  **2.4 정렬**

아래 그림처럼 **정렬된 그래프**를 그리기 위해 상단 메뉴의 **내림차순 정렬**을 이용한다. 바로 왼쪽의 버튼으로 오름차순 정렬도 가능하다.

![img](https://blog.kakaocdn.net/dn/bpZyGZ/btqZBcOSbZL/Xi2LcYKva7K4AfwyealyF1/img.png)



##  **2.5 측정값 추가**

위의 차트만으로는 실제 비즈니스에 이용하기는 부족하다.

따라서, 추가적으로 다른 측정값인 **수익**을 **추가적**으로 확인한다.

![img](https://blog.kakaocdn.net/dn/b4qZ7P/btqZvMDbLlX/fLYjLGVVuy6mkEAzkZWkf1/img.png)

수익에 해당하는 측정값을 **열로 추가한** 결과 위 그림과 같은 **두개의 측정값**을 보여주는 막대 그래프가 그려진다.



다시 이전으로 돌아가 이번에는 수익에 해당하는 필드를 열에 추가하지 않고, **수익 필드**를 **마크 카드의 색상**으로 추가한다. 

![img](https://blog.kakaocdn.net/dn/leSbJ/btqZJ6GldLN/e65p2NDn0VzrsHi2J7S5x1/img.png)

**수익 필드**를 **마크 카드의 색상**으로 가져다 놓은 결과 태블로 자체적으로 해당 데이터에 대한 가장 이상적인 차트를 그려준다. 위 차트를 통해 기본적으로 **막대의 길이**를 통해 **매출액을 비교**할 수 있고, **차트의 색상**을 통해 **수익에 대한 정보**를 얻을 수 있다. 또한, 가구 중 **테이블**이 **수익성에 문제**가 있다는 것을 알 수 있다.



##  **2.6 마크 카드**

 ![img](https://blog.kakaocdn.net/dn/pkk2n/btqZFuurEQv/3SnmYTZirnGwjg69TU6jN1/img.png)

**마크 카드**를 통해 차트가 그려지는 방법을 조정할 수 있다. 현재 합계(수익) 필드가 색상으로 입력되어 위와 같은 차트가 그려졌음을 알 수 있다.



##  **2.7 특정 항목 남기기**

![img](https://blog.kakaocdn.net/dn/kMKG5/btqZDPy5U63/Da1F5qdDRb2ql9XrxkytDK/img.png)

위 차트는 지역 차원 필드를 열정보로 넘겨서 그려진 차트이다. 위 차트에서 **빨간색 막대**로 표시된 부분만을 남겨서 자세하게 확인한다.



![img](https://blog.kakaocdn.net/dn/CS00h/btqZGlxgSf3/uZrRO8hYPInQvFG9YzmBK0/img.png)

해당 막대를 클릭하면 위와 같은 창이 나타난다.



**이 항목만 유지**를 선택해 해당 데이터를 자세하게 살펴본 결과는 아래와 같다.

![img](https://blog.kakaocdn.net/dn/dCfrPV/btqZvMQNbIU/iVXWiisqrXbdJ6Ohl9BPfK/img.png)



##  **2.8 계층 겹치기**

![img](https://blog.kakaocdn.net/dn/bIyDwX/btqZDPTqyFs/Hu6QgZ9ZkjQIkEB4Hgkva0/img.png)

위 그림처럼 해당 데이터에 대해서 다른 사람들이 이해하기 쉽게 여러 계층을 하나의 계층으로 합칠 수 있다.

**하위 계층에 해당하는 중분류 필드**를 **대분류 필드**에 **끌어놓으면** 위와 같은 **계층 만들기**라는 창이 생성된다. 여기서 계층의 이름을 **제품 이름**으로 지정한다.



![img](https://blog.kakaocdn.net/dn/W3jZl/btqZIzB3ZBW/t6FicPmk6HkNTKxV3VZnF0/img.png)

결과적으로 위 그림에서 이전에는 보지 못했던 행 부분의 **(-) 버튼이 생성**된 것을 알 수 있다. 이 버튼을 이용해 **하위 계층정보**로 자유롭게 **이동**할 수 있게 된다.



![img](https://blog.kakaocdn.net/dn/bKr7O5/btqZEBHpf2p/iRQGWoPK75HmtKJwSKKFfK/img.png)

위 결과를 토대로 **가장 수익이 낮은 제품**을 선택에 **데이터 전체 보기**를 이용해 **세부 데이터를 확인**할 수 있다.



 

## **3. 필드의 데이터 타입**

![img](https://blog.kakaocdn.net/dn/0rVT8/btqZGmiHxuI/BOQ2Lo6PymLGAuYlARrFiK/img.png)

위 그림에서 차원에 해당하는 각각의 필드를 살펴보면 **고객ID, 고객 이름** 등의 데이터는 왼쪽에 **Abc** 라는 아이콘이 있고, 이는 **문자열**에 해당하는 데이터를 의미한다.

배송날짜, 주문날짜와 같은 데이터는 달력 모양 아이콘 형태로 **시계열 데이터**를 의미한다.



##  **3.1 지리 데이터**

국가/지역 및 시/도 필드를 확인한다.

![img](https://blog.kakaocdn.net/dn/bMWkou/btqZEAod8e6/78D0oXmHxPOLPU7KK9cHf1/img.png)

위의 그림에서 **국가/지역, 시/도 데이터**는 **문자열 데이터**이고, 이 필드들의 **데이터 타입**을 **지리적 역할**로 바꿀 수 있다.

![img](https://blog.kakaocdn.net/dn/baSs9b/btqZGmJMvp0/LNxvUXF74qmEqdHJVaQRA1/img.png)

위 그림처럼 해당 필드의 Abc 아이콘을 클릭해 **지리적 역할 -> 해당 지리에 맞는 옵션**으로 지정한다.



아래 그림과 같이 기존의 워크시트를 지우고 다시 위 필드들을 입력한다.

![img](https://blog.kakaocdn.net/dn/6HggQ/btqZEAoeIpG/f7KjBcQkh6gNGLkwImSIQk/img.png)

필드의 특성을 **지리적 역할**로 바꾸고 다시 시각화를 진행한 결과 위 그림처럼 지도에 **위도와 경도**를 이용한 **산점도**가 찍힌 것을 확인할 수 있다.



다음으로, 측정값으로 **수익**을 **색상**으로 넘긴다.

![img](https://blog.kakaocdn.net/dn/bACojT/btqZEB1JvDl/ujiQKep0mHqxR5DBmk1J7K/img.png)

수익 필드를 색상으로 넘긴 결과 위와 같은 시각화 결과가 나타난다.

각 지역에서 어떤 지역이 **수익이 높고 낮은지**를 쉽게 파악할 수 있다.



![img](https://blog.kakaocdn.net/dn/cu84rV/btqZBelPidO/K4KzLdzBNE8hHcG6haBCg0/img.png)

위 그림처럼 수익이 가장 낮은 지역은 **Pakistan**으로 확인된다.



아래 그림처럼 이제 **매출**을 마크 카드에서 **크기**로 넘기고, 매출액의 **필터값**으로 **최대값을 0**으로 지정하면 수익성에 **문제**가 있는, **수익성이 -인 지역**만 확인할 수 있
다.

![img](https://blog.kakaocdn.net/dn/OFBnq/btqZGmwgVzW/0gBP1ke0je0a5BrfHDxf1k/img.png)

![img](https://blog.kakaocdn.net/dn/owJS1/btqZGmiJVRH/tzBKpKDtuxzV0aYqCRRodK/img.png)

위에서 수익 필드를 해제하고, 아래 그림과 같이 필터에 다시 **대분류 필드를 넘겨 ****특정 제품군에 대해서 **필터링**이 가능하다.

![img](https://blog.kakaocdn.net/dn/uwMYD/btqZFuH7t3R/wAvAvDpVpOk7zn03hZ1U40/img.png)



##  **4. 날짜 데이터**

![img](https://blog.kakaocdn.net/dn/cf9fdo/btqZFtoVRoG/rInoaYS3fNcTmr5O5XVzgK/img.png)

위 그림처럼 행에 매출, 열에 주문 일자를 넘기게 되면 주문 일자에 따른 **매출액의 추이**를 **라인 그래프**로 그릴 수 있다.

**날짜**를 포함한 데이터를 분석할 때 태블로는 자동으로 **연도별, 분기별, 월별, 일별 **등으로 계층을 생성해서 보여준다.

아래 그림과 같이 **(+)버튼**을 통해 **특정 계층**에 따른 **여러 라인 그래프**를 그릴 수 있다.

![img](https://blog.kakaocdn.net/dn/bBuqs3/btqZFunOf3v/Fvu7ePfEsZDzT5Kcqt6GQk/img.png)

추가적으로 분석에 필요없는 **일별, 분기별 필드를 제거**하면 **각 연도별 월별 매출액 동향**을 나타내는 그래프를 그릴 수도 있다.



## **5. 분석탭의 활용**

![img](https://blog.kakaocdn.net/dn/kQ6y9/btqZIzvp3mH/kURpQQkGGg0pekELzFF88K/img.png)

**분석 탭**은 뷰의 **요약정보나 분석 정보를 추가**하기 위해 사용한다.

 

예를 들어 **연도별 매출액의 평균**을 구하고 싶은 경우 분석 탭에 있는 **평균 라인**을 끌어다가 **패널**로 가져다 놓게 되면 아래 그림의 그래프가 그려진다.

![img](https://blog.kakaocdn.net/dn/npBMM/btqZBeF5mPu/q0BE8K9SUSSYIbB1HLbpm1/img.png)

**매출액의 평균값이 해마다 상승**하고 있다는 **추세선**을 그리기 위해선 **분석탭의 추세선**을 **화면 중앙**에 끌어다 놓으면 아래 그림에 추세선이 **추가**되어 그려진다.

![img](https://blog.kakaocdn.net/dn/3U0yQ/btqZGmpzxFg/2ekGHIgKyocNCBoKofRRnk/img.png)



##  **6. 연속형 필드와 불연속 필드**

**처음**으로 돌아가서 **주문 일자** 데이터를 조작해보자.

열 항목 위의 **주문 날짜 필드**를 **우클릭** 후 열린 창을 확인해보면 **월**이라고 표시된 부분이 **2개**가 나타난다. 아래 그림은 **첫 번째 월**을 클릭 후 출력된 화면이고, **필드의 색**이 **파란색**으로 나타난다.

![img](https://blog.kakaocdn.net/dn/0Z8FA/btqZJ5gxB1V/DBSgkZIIpKzzRfnAjiDUK0/img.png)

또한, 아래 그림과 같이 **두 번째 월**을 클릭하면 **필드의 색**이 **초록색**으로 변하고, **그래프의 모양**이 달라지는 것을 알 수 있다.

![img](https://blog.kakaocdn.net/dn/LpX4x/btqZBelThz7/JUoaREbMCXkLWJSWQy98b0/img.png)

태블로에서 **파란색 필드**는 **불연속성**을 뜻하고, **초록색 필드**는 **연속성**을 의미한다.

즉, **불연속형 월**은 각 **연도별 매출액**을 **월별로 집계**해서 보여주고, **연속형 월**을 선택한 경우에는 시간의 흐름대로 끊김없이 **월별 매출액**을 보여준다.



## **7. 표현 방식**

![img](https://blog.kakaocdn.net/dn/chLfmd/btqZGlqF95v/GYOTozA9wR1bUxt2ubYUrK/img.png)

표현 방식 메뉴는 태블로에서 자동으로 **현재 포함된 필드를 기준**으로 **가장 적합한 차트**를 추천해주는 기능이다.



이번에는 **매출**과 **수익**간 관계를 파악한다. 이 관계를 **고객별**로 어느 **고객 집단**이 **매출액이 높으면서 수익성도 높은지** 혹은 **매출액이 높지만 수익성이 낮은지**에 대해 시각화한다.



![img](https://blog.kakaocdn.net/dn/UszVh/btqZDPF4GPf/D7GRNKshK1UDdD0qTt1rK0/img.png)

위의 그림처럼 **측정값**으로 **매출**과 **수익**, **차원값**으로 **고객 이름**을 선택하면 **표현 방식 메뉴**에서 몇개의 차트가 활성화된다.

이 중에서 **빨간색 테두리**로 표현된 **분산형 차트를 태블로가 권장한다는 의미**이다.

분산형 차트를 그려보면 아래 그림과 같은 차트가 그려진다.

![img](https://blog.kakaocdn.net/dn/MTFXV/btqZBdULTXV/JtyOdG8aZJ4cEk5VClDty0/img.png)



동일한 필드를 선택한 상황에서 **트리맵**이나 **버블차트**로도 표현할 수 있다.

![img](https://blog.kakaocdn.net/dn/McgFc/btqZDONViXV/ynLyvami7o5TaEHcvz1RQK/img.png)

![img](https://blog.kakaocdn.net/dn/pDGmR/btqZyvg2hoB/VPtDabqGMnJsmC39HkPZ9K/img.png)

결과적으로 태블로가 추천한 **분산형 차트**가 가장 이상적으로 그려지는 모습을 확인할 수 있다.

 

##  **8. 대시보드**

지금까지 만들었던 워크시트들을 이용해 대시보드를 제작할 수 있다. 

대시보드를 만드는 목적은 **첫 번째**로 분석결과들을 모아 하나의 대시보드로 만드는 경우가 있고.

**두 번째**로는 각각의 분석 결과에서는 보지 못했던 큰 그림을 보고자 하는 경우가 있다.

대시보드 제작은 화면 하단의 새로운 대시보드를 클릭하여 생성할 수 있다.

![img](https://blog.kakaocdn.net/dn/daH6Sy/btqZKzoaR1Q/W56da9XEjsBO75XJEYkv21/img.png)

위 그림에서 새로운 대시보드 창에서 왼쪽 영역을 보면 지금까지 생성했던 시트들이 나열되어 있는 것을 확인할 수 있다.

이 중에서 대시보드에 추가하고자 하는 시트들을 끌어다 놓을 수 있다.



![img](https://blog.kakaocdn.net/dn/qZrNl/btqZDQkGSKv/3GlBfyY3Nf01DgtQwquN10/img.png)

위 그림처럼 **우측의 대분류**에 따른 **필터 조건**이 적용되는 하나의 대시보드가 완성되었다.

현재 이 필터는 **하나의 시트**에만 적용된다. 

**모든 시트**에 대해서 적용된다면 더욱 좋을 것 같다.



![img](https://blog.kakaocdn.net/dn/DYR6N/btqZDOtDJzH/4dWRt9VMQ4eMTkzlVXrqV1/img.png)

위 그림처럼 필터조건으로 이동해서 **워크시트에 적용 -> 이 데이터 원본을 사용하는 모든 항목**으로 지정한다.

대시보드에 포함된 **모든 시트**들이 **필터조건에 따라 변하는 하나의 대시보드**를 만들 수 있다.
