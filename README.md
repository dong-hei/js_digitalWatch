# js_digitalWatch

let handleId = 0; // 동작에 대한 id 저장

const h1 = document.getElementById("time")
const go = document.getElementById("go")
const stop = document.getElementById("stop")

function getTime(){
    const date = new Date()
    const hour = date.getHours(); //현재 시간을 불러온다
    const minutes = date.getMinutes(); //현재 분을 불러온다
    const seconds = date.getSeconds(); //현재 초를 불러온다
    const time = `${hour}:${minutes}:${seconds}`
    h1.textContent = time;
}

go.onclick = function(){
    if(handleId == 0){
        handleId = setInterval(getTime, 1000 
    } //1000ms마다 getTime을 사용하겠다. 어떤 코드를 일정한 시간 간격을 두고 반복해서 실행하고 싶을 때 사용한다.
}

stop.onclick = function(){
    clearInterval(handleId) //스탑버튼 클릭시 반복중단
    handleId = 0;
}
