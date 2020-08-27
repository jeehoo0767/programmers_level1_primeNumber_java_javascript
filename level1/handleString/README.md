# 프로그래머스 레벨1 문자열 다루기 기본 풀이 java

## 문자열 다루기 기본

### 문제 설명
    문자열 s의 길이가 4 혹은 6이고, 숫자로만 구성돼있는지 확인해주는 함수, solution을 완성하세요. 예를 들어 s가 a234이면 False를 리턴하고 1234라면 True를 리턴하면 됩니다.

### 제한 사항
    s는 길이 1 이상, 길이 8 이하인 문자열입니다.
    입출력 예
    s	return
    a234	false
    1234	true

## solution

### java
    class Solution {
    public boolean solution(String s) {
        int count = s.length();
        boolean answer = true;
        if(s.length()!=4 && s.length()!=6) return false;
        for(int i = 0; i<s.length(); i++){
            if(s.charAt(i)<48 || s.charAt(i)>57)
                return false;
            
        }     
        return true;
        }
    }
### javascript
    function solution(s) {
        var answer = true;
        if (s.length != 4 && s.length != 6) return false; //문자열 길이가 4또는 6이 아니면 false를 리턴
        for (var i = 0; i < s.length; i++) {
            if (s.charCodeAt(i) < 48 || s.charCodeAt(i) > 57)//각 인덱스 문자의 아스키코드 값이 숫자의 범위 내에 들어오는게 있다면 false를 리턴
                return false;
        }
        return true; //위 조건을 만족하지 못하고 넘어 온다면 true 리턴
        }