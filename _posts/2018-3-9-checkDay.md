---

layout: post

title: 백준 알고리즘 1924번 - 요일 체크하기

---

오늘은 2007년 1월 1일 월요일이다. 그렇다면 2007년 x월 y일은 무슨 요일일까? 이를 알아내는 프로그램을 작성하시오.




function checkDay(date){
    if(date%7 == 1) return "월요일";
    else if(date%7 == 2) return "화요일";
    else if(date%7 == 3) return "수요일";
    else if(date%7 == 4) return "목요일";
    else if(date%7 == 5) return "금요일";
    else if(date%7 == 6) return "토요일";
    else return "일요일";
}

//month, date를 변경하면 됨
var month = 10;
var date = 18;
//1월 1일이 월요일 && 2월은 28일이라고 가정
var arr = [31,28,31,30,31,30,31,31,30,31,30,31];
var argument = 0;

for(i = 1 ; i<month ; i++) argument += arr[i-1];
argument += date;

console.log("%d월 %d일의 요일은 " + checkDay(argument) +"입니다",month, date);

출력값입니다
![_config.yml]({{haloyoonjae.github.io }}/images/checkDay_result.JPG)
