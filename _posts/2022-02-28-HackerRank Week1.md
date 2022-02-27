---
layout: post
title: HackerRank - Week1 ( 3 Months Preparation Kit )
subtitle: 말랑말랑 뇌운동
categories: HackerRank
tags: [HackerRank, Algorithm]
published: true

---



알고리즘 연습 하기로 했다.  
고객님 요구사항 개발만 하다보니 자꾸 뭔가를 잊어가는 것 같다. 종종 풀어서 기록해야지. 나중에 보면 뭔가 계속 했단 사실만으로도 좀 뿌듯할 것 같다. 얼마나 할 수 있을까 3개월 다 채워서 할 수 있는 사람 되고싶다,,,

## 1. Breaking the Records

![image](https://user-images.githubusercontent.com/98747932/155892666-064d794d-5ad3-4f56-ad00-fcb80d4dbee6.png)

농구선수의 기록 갱신 횟수 구하기 문제.

시즌의 첫 게임 기록을 기준으로 최저점 갱신 횟수와 최고점 갱신횟수를 구해야하는 문제였다.

첫 게임이 기준이기 때문에 첫 게임(index 0) 점수를 min,max 값으로 처리하고 index 1부터 scores를 선형 탐색으로 처리했다.

![image](https://user-images.githubusercontent.com/98747932/155892727-8a80116f-cff7-4b6b-9f18-b46d0d501ac1.png)

~~근데 해커랭크는 다른 사람 풀이 못보나...난 항상 다른 답도 궁금한데...~~

일단은 처음 준비하는거고 난 좀 쫄보라 자신감이 필요하니 통과율 높은 것부터 풀어야지...


## 2. Sparse Arrays

![image](https://user-images.githubusercontent.com/98747932/155892745-9f1c1fa0-0555-42c9-b28b-5a75aa463ea9.png)

strings 배열에서 queries 배열과 완전히 같은 요소의 수를 구하는 문제.

나는 두가지 방법으로 풀었다.

1. Array를 사용해서 matchCnt를 넣은 뒤, return할 때 List<Integer> 타입으로 변환
    
    ![image](https://user-images.githubusercontent.com/98747932/155892818-68a93be1-fb08-4a59-8050-235989f0eb65.png)
    
2. return 할 List<Integer> 타입을 먼저 선언한 뒤 matchCnt를 List에 add
    
    ![image](https://user-images.githubusercontent.com/98747932/155892765-dbc3a7ef-fa87-463b-a7fe-4399bc92f6c6.png)
    

형변환을 이런저런 방식으로 할 줄 아는 것도 중요하니까 다 해봐야지...

어떤 게 좋은 방식인지는 무슨 기준으로 판단하는 걸까,,,


## 3. Divisible Sum Pairs

![image](https://user-images.githubusercontent.com/98747932/155892839-e122d96c-3704-410c-a142-6e490a7894c5.png)

n개의 요소로 이루어진 배열 ar에서 k로 나누어 떨어지는 두 숫자의 조합을 찾는 문제.

두 index의 조합의 조건이 i < j 이므로 같은 index의 조합이나, 순서만 뒤집어진 조합은 제외

![image](https://user-images.githubusercontent.com/98747932/155892861-6ee4f119-4959-4dd5-a894-79067bfed7e1.png)

나는 그냥 중첩 for문을 이용해서 풀었다.

나는 문제에 주어진 그대로 두 숫자의 합을 k로 나눠 떨어지는 지만을 생각했는데, discussion을 보니 혹자는 하나의 숫자만을 이용하여 k로 나누어 떨어지게 할 수 있는 숫자를 구하고 ar에서 해당 숫자가 있는 지를 찾더라..

그 과정에서 Map도 사용하고,,,

풀었어도 discussion 보면서 다른 사람들의 생각도 한번씩 들여다보는 것도 좋은 듯하다


## 4. Time Conversion

![image](https://user-images.githubusercontent.com/98747932/155892881-54966f76-5fd9-414f-8b46-bddfdd8ef184.png)

12시간 format의 시각을 24 format으로 변경하는 문제

![image](https://user-images.githubusercontent.com/98747932/155892886-bc09d463-45f1-4978-b3bf-dfe571f29f1e.png)

\+ 연산자는 String과 만나면 문자열 결합으로 사용된다. int 와 결합시에도 자동 형변환이 일어나 int → String으로 쉽게 형변환 할 수 있다.

형변환 맨날 까먹으니까 관련된거 나올 때 마다 써야지

- String → int
    1. Integer.parseInt(str)
        
        *int (primitive Type) 반환*
        
    2. Integer.valueOf(str)
        
        *Integer 반환*
        
- int → String
    1. Integer.toString()
    2. String.valueOf()
    3. \+ “”
        
        → 빈 문자열을 더해줌으로써 자동 형변환이 일어나도록 함
        

+) 아무래도 나는 java를 쓰니까 java 내장함수를 사용하는 게 좋았을까?
![image](https://user-images.githubusercontent.com/98747932/155892900-cb66cd9c-5acf-419d-9e8d-aa2248a7b86d.png)


## 5. Mini-Max Sum

![image](https://user-images.githubusercontent.com/98747932/155892913-ada310d4-0fbb-4278-bb31-7791b50fc03f.png)

주어진 5개의 숫자 중 4개의 합으로 만들 수 있는 최소값, 최대값 구하는 문제.

5개 숫자의 총합에서 최대값, 최소값을 빼는 방법으로 풀었다.

![image](https://user-images.githubusercontent.com/98747932/155892925-966c9278-474d-4eeb-806a-587b9794a724.png)

정렬도 할 때마다 긴가민가한다... 정렬 문제 많이많이 풀어보기,,,

그리고 min,max는 java Math 함수써도 될 것 같다. 이번 문제는 요소가 5개인데 많아지면,,,,정렬이 낫나 minmax가 낫나.......?


## 6. Plus Minus

![image](https://user-images.githubusercontent.com/98747932/155892973-c163680c-827d-4dc2-a434-f75877aa86ca.png)

주어진 배열 요소 중 양수,음수,0 비율 구하는 문제

소수점 아래 6자리로 만들어서 출력해야했다

소수점이 가능한 자료형은 float(32bit), double(64bit)이 있는데 그냥 아무생각없이 double로 사용했다...

낭비했네..쩝 생각 한 번만 더 할 걸...

![image](https://user-images.githubusercontent.com/98747932/155893001-6f72b0eb-e048-4916-bc45-bb9402a0f9a4.png)

그리고 소수점 아래 자릿수 고정할 땐 String.format 사용하기 잊지말기~


## 7. Camel Case 4

![image](https://user-images.githubusercontent.com/98747932/155893013-17958b37-accc-4344-bcb3-0e43f100aab1.png)

![image](https://user-images.githubusercontent.com/98747932/155893024-b056b03a-c3a7-4395-a320-792d1e91cc19.png)

앗 너무 방심했다

키보드 입력받는 건 너무 옛 일이라 다 잊었는데,,,,키보드 입력을 받으라니,,,,

암튼, 입력받은 text에 따라 Camel표기법 일반 text 표기법 양방향으로 변환하는 문제.

1. 세미콜론(;)기준으로 첫번째 글자
    - S : split 대상. Camel표기법을 일반 Text로 바꿔야함
    - C : combine 대상. 일반 표기법을 Camel 표기법으로 바꿔야함
2. 세미콜론(;)기준으로 두번째 글자
    - M : Method 형식
    - C : Class 형식
    - V : Variable 형식

일단 나는 두 번,,,당황했는데 console입력을 받아서 하는 건 안 써먹은지 오래라 당황했다...

hackerRank내 다른 문제들 다 입력받아서 하는 부분이 main에서 이미 구현되어있어서 잘 안 보고 넘어왔는데,,잘 봐둘걸,,,생각했고😞 while 문 없이 입력을 받았더니 한 줄만 받고 끝나버렸다

그리고 대소문자 변경도 단어단위로나 해봤지 한 글자씩??은 좀 당황스러웠다..String에서 charAt으로 한글자씩 확인해서 바꿨는데,,,잘한걸까ㅠ

```java
public static void main(String[] args) throws IOException {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */

    BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
    String inputText = "";
    while((inputText = bufferedReader.readLine()) != null)
    {
camelCase(inputText);
    }

}

static void camelCase(String inputText) {
    String[] aInput = inputText.split(";");
    String output = "";

    if("S".equals(aInput[0])) {
        // 대문자 기준으로 띄어쓰기 후 소문자로 변환

        // Method의 경우 괄호 생략 처리
        if("M".equals(aInput[1])){
            aInput[2] = aInput[2].substring(0, aInput[2].length()-2);
        }

        // 첫 글자 빼고 대문자 앞 띄어쓰기
        output += aInput[2].charAt(0);
        for(int i = 1 ; i < aInput[2].length() ; i++) {
            char tmp = aInput[2].charAt(i);

            if(Character.isUpperCase(tmp)){
                output += " " + tmp;
            } else {
                output += tmp;
            }
        }

        // 다른 경우에는 추가로 처리할 것 없음

        output = output.toLowerCase(Locale.ROOT);

    } else { //C
        // 띄어쓰기 뒷문자 대문자로 변환 후 띄어쓰기 생략
        boolean isCapital = false;
        for(int i = 0 ; i < aInput[2].length() ; i++) {
            char tmp = aInput[2].charAt(i);

            if(Character.isSpaceChar(tmp)){
                output += "";
                isCapital = true;
            } else {
                if(isCapital){
                    output += (""+tmp).toUpperCase(Locale.ROOT);
                    isCapital = false;
                } else {
                    output += tmp;
                }
            }
        }

        // Method의 경우 끝에 괄호 추가, class의 경우 맨 앞 글자 대문자 전환
        if("M".equals(aInput[1])){
            output = output + "()";
        } else if ("C".equals(aInput[1])){
            output = (""+output.charAt(0)).toUpperCase(Locale.ROOT) + output.substring(1);
        }
        // V는 추가로 처리할 것 없음
    }

    System.out.println(output);
}
```

풀어서 통과했는데도 더 나은 방법이 있지 않을까 아쉬워서 자꾸 생각하게 된다...흠...