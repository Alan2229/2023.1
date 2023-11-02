function verify(){
    console.log("X, Y")
    let X = parseFloat(x.value);
    let Y = parseFloat(y.value);
    console.log(X, Y);
    if(X>Y){
        let Z=X*Y;
        check=true;
        result = "X умножаем на Y"+" Z = "+ Z;
        document.getElementsByName('result')[0].value=result;
        document.getElementById("result").innerText = message_Text + " Z = " + Z;
    }
    else{
        if((X+Y)<=0){
            result = "Не существует логарифм от отрицательного числа";
            document.getElementById("result").innerHTML = message_Text;
            document.getElementsByName('result')[0].value=result;
            check=false;
        }else
        {
            check=true;
            let Z=Math.log(X+Y);
            result = " Берем натуральный логарифм от X+Y" + "Z = " + Z;
            document.getElementById("result").innerText = message_Text + " Z = log( " + Z + " )";
            document.getElementsByName('result')[0].value=result;
        }
    }
}
function send() {
    if (check) {
        let textCondition = document.getElementsByTagName('p')[0].innerText
        document.getElementsByName('formulation')[0].value = textCondition;
        document.getElementsByName('result')[0].value = result;
        document.getElementById("UserEnter").submit();
    } else {
        alert("Есть недостатки. Повторите ввод")
    }
}
function verify_send() {
    verify();
    send();
}
let message_Text = document.getElementById("result").innerText;
let result;
let check = false;
const x = document.getElementById("x");
x.addEventListener('input', verify);
const y = document.getElementById("y");
y.addEventListener('input', verify);
const elementSend = document.getElementById("send");
elementSend.addEventListener('click', verify_send)


