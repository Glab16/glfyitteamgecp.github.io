<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title></title>
        <style type="text/css">
            
.firstBlock{
    width: 100%;
    height: 20%;
    position: fixed;
    background-color: #211e1e;
    text-align: center;
    top: 0%;
    left: 0%;
     outline: 2px solid #000;
}
.secondBlock{
    width: 30%;
    height: 67%;
    position: fixed;
    background-color: #211e1e;
    top: 20.2%;
    left: 0%;
    outline: 2px solid #000;
}
.input1SecondBlock{
    margin-left: 10%;
}
.thirdBlock{
    width: 100%;
    height: 67%;
    position: fixed;
    background-color: #211e1e;
    text-align: center;
    top: 87.2%;
    left: 0%;
    outline: 2px solid #000;
}
.fourthBlock{
    width: 34%;
    height: 67%;
    position: fixed;
    
    text-align: center;
    top: 23%;
    left: 31.5%;
    ;
}
.fifthBlock{
    width: 34%;
    height: 67%;
    position: fixed;
    
    text-align: center;
    top: 23%;
    left: 65.5%;
    
}
.button1{
  color: #DBA901;
  background-color: #212020;
  border-color: #212020;
}s
        </style>
    </head>
    <body style="background-color: #2E2E2E">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
        <div class="firstBlock">
 
        </div>
        <div class="secondBlock">
            <div class="input1SecondBlock">
                <form method="GET"  onsubmit="return false;" style=" font-size: 90%" >
                    <div style = "color: #DBA901; " >
                        <p>Введите M1 (кг)</p>
                             <label><input type="text" name="m1" id="m1"></label>
                        <p>Введите M2 (кг)</p>
                            <label><input type="text" name="m2" id="m2"></label>
                        <p>Введите тягу ДУ (кг)</p>
                            <label><input type="text" name="th" id="th"></label>
                        <p>Введите расход топлива (кг/с)</p>
                            <label><input type="text" name="r" id="r"></label>
                        <p>Введите массу полезной нагрузки (кг)</p>
                            <label><input type="text" name="m" id="m"></label>
                    </div>
                    <br />
                    <button value="Расчитать" onclick="cel()" class="button1"> Отправить</button>
                </form>
            </div>
        </div>
        <div class="thirdBlock">
            
        </div>
        <div class="fourthBlock">
                        <table border="1"  width="100%" style="color: #DBA901"> 
                            <tr> 
                                <td> 
                                    <p>Скорость</p> 
                                </td> 
                                <td> 
                                    <p>V</p>
                                </td> 
                                <td> 
                                    <p id="fast"> м/с </p> 
                                </td> 
                            </tr> 
        <!-------------------------------------------I---------------------------------------> 
                            <tr> 
                                <td> 
                                    <p>Удельный импульс</p> 
                                </td> 
                                <td> 
                                    <p>i</p> 
                                </td> 
                                <td> 
                                    <p id="im"></p> 
                                </td> 
                            </tr> 
        <!----------------------------------------T-------------------------------------------> 
                            <tr> 
                                <td> 
                                    <p>Время полета</p> 
                                </td> 
                                <td> 
                                    <p>t</p> 
                                </td> 
                                <td> 
                                   
                                    <p>Секунд</p> 
                                </td> 
                            </tr> 
        <!----------------------------------------H-----------------------------------------> 
                            <tr> 
                                <td> 
                                    <p>Высота полета</p> 
                                </td> 
                                <td> 
                                    <p>h</p> 
                                </td> 
                                <td> 
                                    
                                    <p>метров</p> 
                                </td> 
                            </tr> 
        <!----------------------------------------a-----------------------------------------> 
                            <tr> 
                                <td> 
                                    <p>Ускорение</p> 
                                </td> 
                                <td> 
                                    <p>a</p> 
                                </td> 
                                <td> 
                                    <p> м/с2 </p> 
                                </td> 
                            </tr> 
        <!----------------------------------------k-----------------------------------------> 
                            <tr> 
                                <td> 
                                    <p>Перегрузка</p> 
                                </td> 
                                <td> 
                                    <p>k</p> 
                                </td> 
                                <td> 
                                    <p> G </p> 
                                </td> 
                            </tr> 
        <!----------------------------------------------------------------------------------> 
                        </table> 
                   
       
        </div>
        <div class="fifthBlock">
            <table border="1" width="100%" style="color: #DBA901">
        <!---------------------------------M1--------------------------------------------> 
                            <tr> 
                                <td> 
                                    <p>M1</p> 
                                </td> 
                                <td> 
                                    <p>M1</p> 
                                </td> 
                                <td> 
                                    <p id="mass1"> кг </p> 
                                </td> 
                            </tr> 
        <!----------------------------------M2-----------------------------------------------> 
                            <tr> 
                                <td> 
                                    <p>M2</p> 
                                </td> 
                                <td> 
                                    <p>M2</p> 
                                </td> 
                                <td> 
                                    <p id="mass2"> кг </p> 
                                </td> 
                            </tr> 
        <!----------------------------------th-----------------------------------------------> 
                            <tr> 
                                <td> 
                                    <p>Тяга ДУ</p> 
                                </td> 
                                <td> 
                                    <p>th</p> 
                                </td> 
                                <td> 
                                    <p id="thr">кг</p> 
                                </td> 
                            </tr> 
        <!------------------------------------r-------------------------------------------> 
                            <tr> 
                                <td> 
                                    <p>Расход топлива</p> 
                                </td> 
                                <td> 
                                    <p>R</p> 
                                </td> 
                                <td>
                                    <p id="con">кг/с</p> 
                            </td> 
        <!-----------------------------------m3--------------------------------------------------> 
                            <tr> 
                                <td> 
                                    <p>Масса полезной нагрузки</p> 
                                </td> 
                                <td> 
                                    <p>M</p> 
                                </td> 
                                <td>
                                    <p id="mass">кг</p> 
                                </td> 
                            </tr>  
             
            </table>
        </div>
    <script type="text/javascript">
            let m1 = +document.getElementById('m1').value;
            let m2 = +document.getElementById('m2').value;
            let th = +document.getElementById('th').value;
            let r = +document.getElementById('r').value;
            let m = +document.getElementById('m').value;
        function cel(){
    const g = 10;
    const v0 = 0;
    let i;
    
    if (th && r) {
        i = th / r;   
    }
    let v;
    if (m1 && m2 && i) {
        v = i * Math.log((m1 + m) / (m2 + m));
    }
    let t = (m1 - m2) / r;
    let h = t * v;
   let a = (v - v0) / t;
   let k = (g + a);
            document.getElementById('mass1').innerHTML = m1;
            document.getElementById('mass2').innerHTML = m2;
            document.getElementById('thr').innerHTML = th;
            document.getElementById('con').innerHTML = r;
            document.getElementById('mass').innerHTML = m;
           // document.getElementById('im').innerHTML = i;
           // document.getElementById('fast').innerHTML = v;
          //  document.getElementById('mass1').innerHTML = m1
          alert(v);
        }
    </script>
    </body>
</html>
