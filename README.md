# js_digitalWatch
<br></br>
let handleId = 0; // 동작에 대한 id 저장
<br></br>
const h1 = document.getElementById("time")<p></p>
const go = document.getElementById("go")<p></p>
const stop = document.getElementById("stop")<p></p>
time, go , stop 변수 선언 
<br></br>

사용한 함수
<br></br>
getTime(){
시간,분,초를 선언하고 불러온다
<p></p>
선언된 시간,분,초를 동적쿼리로 time부에 선언한다.
<p></p>
const time = `${hour}:${minutes}:${seconds}`
<p></p>
}

<br></br>
go.onclick = function(){
    if(handleId == 0){
    <p></p>
    handleId = setInterval(getTime, 1000)
    } //1000ms마다 getTime을 사용하겠다. 어떤 코드를 일정한 시간 간격을 두고 반복해서 실행하고 싶을 때 사용한다.
}
<br></br>

stop.onclick = function(){
    clearInterval(handleId) //스탑버튼 클릭시 반복중단
        <p></p>
    handleId = 0;}
    <p></p>

