# MySQL-Stydy-6

7.역순 정렬하기
(https://school.programmers.co.kr/learn/courses/30/lessons/59035)

답:
SELECT NAME,DATETIME FROM ANIMAL_INS
ORDER BY ANIMAL_ID DESC

8.강원도에 위치한 생산공장 목록 출력하기
(https://school.programmers.co.kr/learn/courses/30/lessons/131112)

답:
SELECT FACTORY_ID,FACTORY_NAME,ADDRESS FROM FOOD_FACTORY
WHERE ADDRESS LIKE '강원도%'
ORDER BY FACTORY_ID
👉like를 사용하여 강원도 주소만 뽑기 (like'강원도%': 강원도 뒤에 아무거나)

9.나이 정보가 없는 회원 수 구하기
(https://school.programmers.co.kr/learn/courses/30/lessons/131528)

답:
SELECT COUNT(*) AS USERS FROM USER_INFO
WHERE AGE IS NULL
👉나이 정보가 없는 사람이니 Null인 것만 뽑아내면 됨

10.경기도에 위치한 식품창고 목록 출력하기
(https://school.programmers.co.kr/learn/courses/30/lessons/131114)

답:
SELECT WAREHOUSE_ID,WAREHOUSE_NAME, ADDRESS ,
CASE WHEN FREEZER_YN IS NULL THEN 'N' ELSE FREEZER_YN END
as FREEZER_YN FROM FOOD_WAREHOUSE
WHERE ADDRESS LIKE '경기도%'
ORDER BY WAREHOUSE_ID
👉8번문제를 응요한 상태에서 CASE 문법을 사용하여 조건을 걸어줌

11.조건에 맞는 회원수 구하기
(https://school.programmers.co.kr/learn/courses/30/lessons/131535)

답:
SELECT COUNT(*) AS USERS FROM USER_INFO
WHERE JOINED LIKE '2021%'
AND AGE BETWEEN 20 AND 30
👉BETWEEN을 사용하여 범위값을 정해준다.

12.이름이 없는 동물의 아이디
(https://school.programmers.co.kr/learn/courses/30/lessons/59039)

답:
SELECT ANIMAL_ID FROM ANIMAL_INS
WHERE NAME IS NULL
ORDER BY ANIMAL_ID
