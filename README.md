# Mysql2
### 1.SQL 문자열 함수들 
 
 - concat 문자열을 합치는 함수,select concat(컬럼명,'기호',컬럼명)이런식으로 쓸수 있다 as 를 써서 합친 컬럼명을 바꿀수 있다.
 - 아래 이미지 참고.
 
 ![mysql 이미지](https://user-images.githubusercontent.com/80316237/111279280-e242e180-867d-11eb-8fa9-05a192899793.PNG)

 - substring 문자열 안의 일부분을 가져올때,예시로 select substring('Hello World',7); 이렇게 쓰면 아래와 같이 나온다.
 
 - ![mysql 이밎](https://user-images.githubusercontent.com/80316237/111279663-449be200-867e-11eb-9165-78baf6ce7a0b.PNG)

 - replace 문자열의 일부를 내가 원하는 문자열로 바꾸는 함수이다 예시로 select replace('What the hell','hell','***');
 - 아래 이미지 참고.
 
 -![이미지 2](https://user-images.githubusercontent.com/80316237/111280018-ad835a00-867e-11eb-856b-3ea96acc8d55.PNG)
 
 - reverse 문자열의 순서를 바꾸는 함수 reverse 함수,예시로 select reverse('What the hell'); 아래와 같이 나온다.

 -![이미지](https://user-images.githubusercontent.com/80316237/111280296-fe934e00-867e-11eb-9594-03ad0c10a523.PNG)

 - char_length 문자열의 길이를 알려주는 함수이다, 예시로 select char_length('Hello World'); 아래와 같이 나온다.

 -![이미지 2](https://user-images.githubusercontent.com/80316237/111280471-38645480-867f-11eb-8ed4-53d7b5c951a7.PNG)

 - upper() 모든 문장을 대문자로 바꿔주는 함수이다 예시는 select upper('Hello World'); 아래와 같이 나온다.

 -![이미지 3](https://user-images.githubusercontent.com/80316237/111280819-9bee8200-867f-11eb-9da9-5e7aafe90dc4.PNG)
 
 - lower() 모든 문장을 소문자로 바꿔주는 함수이다 예시는 select lower('HELLO WORLD'); 아래와 같이 나온다.

 - ![이미지 4](https://user-images.githubusercontent.com/80316237/111280904-b45e9c80-867f-11eb-9d66-cd088b64e1f1.PNG)

 - distinct 유니크한 데이터로만 데이터 가져오는 함수이다,예시는 select distinct author_lname from books; 아래와 같이 나온다.
 
 - ![이미지5](https://user-images.githubusercontent.com/80316237/111281189-0273a000-8680-11eb-8b4d-de9d7890429e.PNG)

 ### 2.오름차순,내림차순 정렬과 여러 컬럼 정렬 방법
 
 - order by 함수는 정렬 할때 쓰는 키워드 이다 예시로 
 - select author_lname
 - from books
 - order by author_lname;
 - 이렇게 쓰면 오름차순이고 ace라는 함수를 써도 되고 안써도 된다.
 
 - select * from books
 - order by title desc;
 - 이렇게 쓰면 내림차순으로 정렬 된다.
 
 - 여러 컬럼을 정렬 할때는 order by 컬럼명,컬럼명 이런식으로 쓰고 내림차순이면 뒤에 desc를 붙인다.
 
 ### 3. limit와 Offset 사용법 (정렬과 함께 사용하는 예도 포함)
 
 - limit offset은 숫자를 정해놓고 계속 누르면 그 숫자대로 숫자가 증가되면서 화면에 보여준다. 예를 들어
 - select *
 - from books limit 5;
 - 처음엔 5개
 - select * 
 - from books limit 5,5;
 - 이런식으로 점점 증가하게 된다. 
 
 ### 4. 포함하는 단어 검색하는 like 키워드 사용법
 
 - 데이터에 포함된 단어를 검색해서 출력할때 쓰는 함수이다. 
 - select title,author_fname,author_lname
 - from books
 - where author_fname like 'da';
 - 이렇게 쓰면 데이터에 da 두글자가 있는 이름만 나온다. 우리가 하고싶은건 da가 들어간 문장을 찾을려고 하는것이다 아래와 같이 하면된다.
 
 - select title,author_fname,author_lname
 - from books
 - where author_fname like '%da%';
 - %는 다른 글자가 있어도 된다는 뜻을 의미해서 써야지만 da가 들어간 문자열데이터를 불러올수있다.









