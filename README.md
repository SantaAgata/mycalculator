<!DOCTYPE html>
<html>
<head>
    <h1>Calculator</h1>
    <title>Kalkulator</title>
    <link rel="stylesheet" type="text/css" href="style.css">
    <script type="text/javascript" src="script.js"></script>
</head>
<body>
    <div class="wrapper">
        <div class="calculator">
            <form name="form">
                <input type="text" class="textView" name="textView">
            </form>
            <table>
                <tr>
                    <td><input type="button" class="button" value="C" onclick="c()"></td>
                    <td><input type="button" class="button del" value="Del" onclick="del()"></td>
                    <td><input type="button" class="button" value="x" onclick="insert('*')"></td>
                    <td><input type="button" class="button" value="/" onclick="insert('/')"></td>
                </tr>
                <tr>
                    <td><input type="button" class="button" value="7" onclick="insert(7)"></td>
                    <td><input type="button" class="button" value="8" onclick="insert(8)"></td>
                    <td><input type="button" class="button" value="9" onclick="insert(9)"></td>
                    <td><input type="button" class="button" value="-" onclick="insert('-')"></td>
                </tr>
                <tr>
                    <td><input type="button" class="button" value="4" onclick="insert(4)"></td>
                    <td><input type="button" class="button" value="5" onclick="insert(5)"></td>
                    <td><input type="button" class="button" value="6" onclick="insert(6)"></td>
                    <td><input type="button" class="button" value="+" onclick="insert('+')"></td>
                </tr>
                <tr>
                    <td><input type="button" class="button" value="1" onclick="insert(1)"></td>
                    <td><input type="button" class="button" value="2" onclick="insert(2)"></td>
                    <td><input type="button" class="button" value="3" onclick="insert(3)"></td>
                    <td rowspan="2"><input type="button" class="button equal" value="=" onclick="equal()"></td>
                </tr>
                <tr>
                    <td colspan="2"><input type="button" class="button zero" value="0" onclick="insert(0)"></td>
                    <td><input type="button" class="button" value="." onclick="insert('.')"></td>
                </tr>
            </table>
        </div>
    </div>
</body>
</html>

function insert(num){
    document.form.textView.value = document.form.textView.value+num;
}
function c(){
    document.form.textView.value = "";
}

function del(){
    var x = document.form.textView.value;
    document.form.textView.value = x.substring(0, x.length-1)
}

function equal(){
    var x = document.form.textView.value;
    if(x == ''){
        alert('Enter number')
    }
    if(x){
        document.form.textView.value = eval(x);
    }
}

*{
    margin: 0;
    padding: 0;
}

h1{
    position: absolute;
    top: 13%;
    left: 44.3%;
    color:mintcream;
}

body{
    background: gray;
}

.wrapper{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}

.calculator{
    background: rgb(238, 21, 76);
    padding: 10px;
    border-radius: 5px;
}

.textView{
    width: 255px;
    font-size: 25px;
    font-weight: bold;
    padding: 5px
}
