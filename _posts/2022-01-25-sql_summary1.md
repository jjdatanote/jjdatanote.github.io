---
layout : single
title : "sql 정리 1"
---

# **데이터모델의 이해** 

**1.모델링의 이해** 

가. 모델링의 정의 : “다양한 현상을 표기법에 의해 표기하는 것”  

나. ★ 특징 3가지: 추상화, 단순화, 명확화  

다. 모델링의 3가지 관점: 데이터 관점, 프로세스 관점, 상관 관점 

**2.데이터모델링의 3단계**

가. 개념적 데이터모델링 : 추상화 수준이 높고 업무 중심적이고 포괄적인 수준의 모델링 진행  

나. 논리적 데이터모델링 : 시스템으로 구축하고자하는 업무에 대해 Key, 속성, 관계 등을 정확하게 표현, 높은 재사용  

다. 물리적 데이터모델링 : 실제로 데이터베이스에 이식할 수 있도록 성능, 저장 등 물리적인 성격 고려 설계

# **엔터티**

**1.엔터티의 특징**  

가. 업무에서 필요로 하는 정보  

나. 식별자에 의해 식별이 가능 해야함  

다. 인스턴스의 집합  

라. 업무프로세스에 의해 이용  

마. 속성을 포함  

바. 관계의 존재

 **2.엔터티의 분류**

가. 유무형에 따른 분류: 유형 엔터티, 개념 엔터티, 사건 엔터티  

나. 발생시점에 따른 분류: 기본 엔터티, 중심 엔터티, 행위 엔터티  

# **속성**

**1.속성의 개념**: “업무에서 필요로 하는 인스턴스로 관리하고자하는 의미상 더 이상 분리되지 않는 최소의 데이터 단위”

**2.엔터티, 인스턴스와 속성, 속성값에 대한 내용과 표기법**  

가. ★ 엔터티, 인스턴스, 속성, 속성값의관계  

- 한 개의 엔터티는 두개 이상의 인스턴스 집합이어야 한다.  
- 한 개의 엔터티는 두개 이상의 속성을 갖는다.  
- 한 개의 속성은 한 개의 속성값을 갖는다. 

나. 속성의 표기법: IE표기법, Barker 표기법

# **관계**

**1.관계의 개념** 

가. 관계의 정의  “엔터티의 인스턴스 사이의 논리적인 연관성으로서 존재의 형태로서나 행위로서 서로에게 연관성이 부여된 상태”  

나. 관계의 페어링: “패어링은 엔터티안에 인스턴스가 개별적으로 관계를 가지는 것이고, 이것의 집합을 관계로 표현”  

다. 관계의 분류  - ERD: 존재에 의한 관계 / 행위에 의한 관계  - UML(Unified Modeling Language): 연관 관계 / 의존관계

**2.관계의 표기법 ** 

가. 관계명: 관계의 이름  

나. 관계 차수: 1:1, 1:M, M:N  

다. 관계선택사양: 필수관계, 선택관계 

# **식별자**

**1.식별자 개념** 

가. 하나의 엔터티에 구성되어있는 여러 개의 속성 중에 엔터티를 대표할 수 있는 속성을 의미 

나. 하나의 엔터티는 반드시 하나의 유일한 식별자가 존재해야 한다.

**2.주식별자 도출기준**  

가. 해당업무에서 자주 이용되는 속성을 주식별자로 지정하도록함  

나. 명칭, 내역등과같이 이름으로 기술되는 것을 피함  

다. 속성의 수가 많아지지 않도록 함 

**3.식별자관계와 비식별자 관계에 따른 식별자**

가. 식별자관계와 비식별자 관계의 결정: 외부식별자는 Foreign Key역할을 한다.  

나. 식별자 관계: “자식엔터티의 주식별자로 부모의 주식별자가 상속이 되는 경우”  Null값이 오면 안되므로 반드시 부모엔터티가 생성되어야 자기자신의 엔터티 생성  

다. 비식별자 관계: “부모 엔터티로부터 속성으로 받았지만 자식엔터티의 주식별자로 사용하지않고  일반적인 속성으로만 사용하는 경우”  

라. 식별자관계로만 설정할 경우의 문제점: 주식별자 속성이 지속적으로 증가, 복잡성과 오류 가능성 유발  

마. 비식별자관계로만 설정한 경우의 문제점: 쓸데없이 부모엔터티까지 찾아가야 하는 경우가 발생한다.



# **관계형 데이터베이스 개요**

**1.데이터베이스**: “특정기업이나 조직 또는 개인이 필요에 의해 데이터를 일정한 형태로 저장한 것”  

**2.SQL**: 관계형데이터베이스에서 데이터 정의, 데이터 조작, 데이터제어를 하기 위해 사용하는 언어  -데이터조작어(DML) - SELECT, INSERT, UPDATE, DELETE(NOT AUTO COMMIT) 

-데이터정의어(DDL) - CREATE, ALTER, DROP, RENAME(AUTO COMMIT)  

-데이터제어어(DCL) - GRANT, REVOKE  

-트랜잭션제어어(TCL) - COMMIT, ROLLBACK

**3.TABLE**: 테이블은 하나 이상의 칼럼을 가져야 한다  관계형 데이터베이스에서는 모든 테이터를 칼럼과 행의 2차원 구조로 나타낸다.

**4.ERD(Entity Relationship Diagram)**: “관계의 의미를 직관적으로 표현할 수 있는 수단” / 구성요소 3개는 -> 엔터티, 관계, 속성

# **DDL**

**1.CREATE TABLE**

**SQL>>**  CREATE TABLE 테이블 이름  

(칼럼명1 DATATYPE [DEFAULT 형식],  

칼럼명1 DATATYPE [DEFAULT 형식],  

칼럼명1 DATATYPE [DEFAULT 형식] ); 

* 제약조건(CONSTRAINT): “사용자가 원하는 조건의 데이터만 유지하기 위한 방법”  

  (CONSTRAINT 종류: PRIMARY KEY, UNIQUE KEY, NOT NULL, CHECK, FOREIGN KEY)

**2.ALTER TABLE**

**SQL>>**  ALTER TABLE 테이블이름 ADD 속성_이름 데이터타입 [DEFAULT]; //추가 

ALTER TABLE 테이블이름 ALTER 속성_이름 [SET DEFAULT];                     //속성명변경  

ALTER TABLE 테이블이름 DROP 속성_이름 [CASCADE | RESTRICT];              //속성 삭제

**3.RENAME TABLE**

**SQL>>**  ALTER TABLE 테이블명 

 RENAME COLUMN 변경해야할 컬럼명 TO 새로운 컬럼명;   

ALTER TABLE PLAYER  

RENAME COLUMN PLAYER_ID TO TEAM_ID; 

**4.DROP TABLE**

**SQL>>**  ALTER TABLE 테이블명 DROP COLUMN 삭제할 컬럼명; 

 DROP TABLE PLAYER; 

  ALTER TABLE PLAYER DROP COLUMN ADDRESS;

 -테이블의 모든 데이터 및 구조 삭제

**5.TRUNCATE TABLE**

**SQL>>**  TRUNCATE TABLE 테이블명 DROP COLUMN 삭제할 컬럼명;

-테이블 자체가 삭제되는 것이 아니고, 해당테이블에 들어있던 모든 행들이 제거되는 것(데이터만 제거) 

# **DML**

**1.INSERT**

**SQL>>**  INSERT INTO 테이블명 (COLUMN_LIST)VALUES (COLUMN_LIST에 넣을 VALUE_LIST);  INSERT INTO 테이블명VALUES (전체 COLUMN에 넣을 VALUE_LIST); 



PLAYER INSERT INTO PLAYER  (PLAYER_ID, PLAYER_NAME, TEAM_ID, POSITION, HEIGHT, WEIGHT, BACK_NO) 

VALUES ('2002007', '박지성', 'K07', 'MF', 178, 73, 7); 

**2.UPDATE**

**SQL>>**  UPDATE 테이블명 SET 수정되어야 할 칼럼명 = 수정되기를 원하는 새로운 값;  



UPDATE PLAYER SET BACK_NO = 99;  

UPDATE PLAYER SET POSITION = 'MF'; 

**3.DELETE**

SQL>>  DELETE FROM 삭제를 원하는 정보가 들어있는 테이블명 WHERE 조건절;   



DELETE FROM PLAYER; 

**4.SELECT**

**SQL>> ** SELECT 칼럼명 FROM 테이블;  

SELECT PLAYER_ID, PLAYER_NAME, TEAM_ID, POSITION FROM PLAYER;  

SELECT DISTINCT POSITION FROM PLAYER; —>(DISTINCT: 중복데이터를 1건으로 표시) 

SELECT * FROM PLAYER; —>(*: 모든 칼럼명 선택) 

SELECT PLAYER_NAME AS 선수명 FROM PLAYER;



# **TCL**

**1.트랜잭션 개요**: “데이터베이스의 논리적 연산 단위” 

- 트랜잭션은 데이터베이스의 논리적 연산단위이다. 
- 트랜잭션(TRANSACTION)이란 밀접히 관련되어  분리될 수 없는 한 개 이상의 데이터베이스 조작을 가리킨다. 
- 하나의 트랜잭션에는 하나 이상의 SQL 문장이 포함된다.  
- 트랜잭션은 분할할 수 없는 최소의 단위이다. 그렇기 때문에 전부 적용하거나 전부 취소한다. 

**2.트랜잭션 특성**: 원자성, 일관성, 고립성, 지속성

-원자성 : 트랜잭션에서 정의된 연산들은 모두 성공적으로 실행되던지 아니면 전혀 실행되지 않은 상태로 남아 있어야 한다.

-일관성 : 트랜잭션이 실행되기 전의 데이터베이스 내용이 잘못 되어 있지 않다면 트랜잭션이 실행된 이후에도 데이터베이스의 내용이 잘못되면 안 된다.

-고립성 : 트랜잭션이 실행되는 도중에 다른 트랜잭션의 영향을 받아 잘못된 결과를 만들어서는 안된다.

-지속성 : 트랜잭션이 성공적으로 수행되면 그 트랜잭션이 갱신한 데이터베이스의 내용은 영구적으로 저장된다.

**3.TCL 종류**

-커밋(COMMIT): 올바르게 반영된 데이터를 데이터베이스에 반영시키는 것  

-롤백(ROLLBACK): 트랜잭션 시작 이전의 상태로 되돌리는 것  

-저장점(SAVEPOINT): 저장점 기능

**4.COMMIT**

**Oracle SQL>>**  

UPDATE PLAYER SET HEIGHT = 100;  

COMMIT; 

**SQL>>**  UPDATE PLAYER SET HEIGHT = 100;  

-★ Oracle은 DML문장 수행 후 사용자가 임의로 COMMIT 또는 ROLLBACK 수행해줘야 함  

-★ SQL Server는 기본적으로 AUTO COMMIT

**5.ROLLBACK** 

**Oracle SQL>>**  

UPDATE PLAYER SET HEIGHT = 100;

ROLLBACK; ———>(롤백 완료)  

**SQL>>**  

BEGIN TRAN UPDATE PLAYER SET HEIGHT = 100;  

ROLLBACK; ———>(롤백 완료)   

-테이블 내 입력한 데이터나, 수정한 데이터, 삭제한 데이터에 대하여 COMMIT 이전으로 되돌려,  변경 사항을 취소할 수 있는데 데이터베이스에서는 롤백(ROLLBACK) 기능을 사용한다. 

**6.SAVEPOINT** 

**SQL>>**  

SAVEPOINT 세이브포인트명;  

SAVEPOINT SVPT1;  

ROLLBACK TO SVPT1; 

 -저장점(SAVEPOINT)을 정의하면 롤백(ROLLBACK)할 때 트랜잭션에 포함된 전체 작업을 롤백하는 것이 아니라  현 시점에서 SAVEPOINT까지 트랜잭션의 일부만 롤백할 수 있다. 
