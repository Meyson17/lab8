<p></p>

<h2 align="center">ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ПРОФЕССИОНАЛЬНОГО ОБРАЗОВАНИЯ <br> «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ» <br> КАФЕДРА ИНФОРМАТИКИ </h2>
<p align="center">Лабораторная работа №8 <br>
по курсу «Web-технологии, языки и средства создания web-приложений» 

<p align="center"><b>"Java Script"</b><p>
<p align="right"><b>Выполнил: </b> студент 231 группы Рыжков Владимир </p>
<p  align="right"><b>Принял: </b> Соболев Е. И., старший преподователь</p>
<br>
<br>
<br>
<p align="center">Южно-Сахалинск <br> СахГУ <br> 2023</p>
<h2> Введение </h2>
<p>Лабораторные работы по дисциплине «Web-технологии, языки и средства создания web-приложений» предназначены для освоения полученных теоретических знаний на практике. Перед началом первой лабораторной работы были поставлены цели: <br>
<ol>
  <li>Овладеть навыками работы с языком гипертекстовой разметки HTML, в частности научиться основам Java Script, создаватьскрипты для решения задач.
</ol>
В соответствии с данными целями необходимо решить следующие задачи:
<ol>
   <li> Написать скрипты для решения данных задач.
   </ol>
Для реализации данной работы будет использоваться Notepad++. Выполнение кода будет происходить в браузере Microsoft Edge.
</p>

<p>В первой части были выполнены первые 20 коротких задач, с решением которых можно ознакомиться в файле. </p>
<h2>Решение задач:</h2>
<script>
          
            function num1()
            {
            if(true)
                console.log(true)
            else
                console.log(false)

            if(false)
                console.log(true)
            else
                console.log(false)
        }

        function num2()
        {
            let m = Math.floor(Math.random() * 100);
            if (m > 50) console.log("большое " + m)
            else console.log("маленькое " + m)
        }

        function num3()
        {
            var i = 2;
            var j = 0;
            while( i < 9 ){
 	            console.log( i++ );
                j++;
            }
            console.log("Цикл выполнился "+j+" раз");
        }

        function num4()
        {
            for(let i = 45; i < 68; i++ )
                console.log(i);
        }

        function num5()
        {
            for(let i = 45; i < 671; i++ )
                if(i % 10 == 0) console.log(i);
        }

        function num6()
        {
            for(let i = 45; i < 671; i++ )
                if(i % 10 == 0 || i < 68) console.log(i);
        }

        function num7()
        {
            var n = Math.floor(Math.random()*10);
            console.log("Число " + n)
            switch(n){
                case 1: {
                    console.log('один')
                    break;
                }
                case 2: {
                    console.log('два')
                    break;
                }
                case 3: {
                    console.log('три')
                    break;
                }
                case 4: {
                    console.log('четыре')
                    break;
                }
                case 5: {
                    console.log('пять')
                    break;
                }
                case 6: {
                    console.log('шесть')
                    break;
                }
                case 7: {
                    console.log('семь')
                    break;
                }
                case 8: {
                    console.log('восемь')
                    break;
                }
                case 9: {
                    console.log('девять')
                    break;
                }
                case 0: {
                    console.log('ноль')
                    break;
                }
            }
        }

        function num8()
        {
            for(let i = 0; i < 8; i++)
                document.write('<img src="mops.jpg" alt="mops" />')
        }

        function num9()
        {
            let size = 120;
            let unit = "Кб";
            switch(unit)
            {
                case "Кб":
                    size = size * 1024;
                    break;

                case "Мб":
                    size = size* 1024 * 1024;
                    break;

                case "Гб":
                    size = size * 1024 * 1024 * 1024;
                    break;
            }
            console.log(size);
        }

        function num10()
        {
            let style = "<style>\n table,th,td,caption \n{\n border: 2px solid black;\n border-collapse: collapse; \n}\n</style>\n"
            let str = '<table>\n<caption>Май</caption>\n<tr>\n';
            for(let i = 1; i<=7; i++)
            {
                switch(i){
                    case 1:
                        str+="<th>Пн</th>\n";
                        break;
                    case 2:
                        str+="<th>Вт</th>\n";
                        break;
                    case 3:
                        str+="<th>Ср</th>\n";
                        break;
                    case 4:
                        str+="<th>Чт</th>\n";
                        break;
                    case 5:
                        str+="<th>Пт</th>\n";
                        break;
                    case 6:
                        str+="<th>Сб</th>\n";
                        break;
                    case 7:
                        str+="<th>Вс</th>\n";
                        break;   
                }
            }
            str+="</tr>\n"
            for(let i = 1; i <= 31; i++)
            {
                str+=`<td>${i}</td>\n`;
                if(i % 7 == 0 ) str +="</tr>\n<tr>\n";
                if(i == 31) str += "</tr>"
            }
            str+="</table>";
            document.write(style + str);
        }

        function hello1()
        {
            return "Привет, JavaScript!";
        }

        function num11()
        {
            console.log(hello1());
        }

        function hello2(name)
        {
            if(name == "") return "Привет, гость";
            return "Привет, " + name;
        }

        function num12()
        {
            console.log(hello2(prompt("Введите ваше имя")));
        }

        function mul(n,m)
        {
            return n*m;
        }

        function num13()
        {
            let n = prompt("n=");
            let m = prompt("m=");
            console.log(mul(n,m));
        }

        function repeat(str,n)
        {
            if(n=="") n = 2;
            let result = "";
            for(let i = 0; i < n; i++)
                result += str;
            return result;
        }

        function num14()
        {
            let str = prompt("str=");
            let n = prompt("n=");
            console.log(repeat(str,n));
        }

        function rgb(r=0,g=0,b=0)
        {
            return `rgb(${r},${g},${b})`;
        }

        function num15()
        {
            let r = prompt("r=");
            let g = prompt("g=");
            let b = prompt("b=");
            console.log(rgb(r,g,b));
        }

        function avg(...args)
        {
            let result = 0;
            for(let i = 0; i < args.length; i++)
                result+= args[i];
            return result / args.length;
        }

        function num16()
        {
            console.log(avg(1,2,3,4,5,6));
        }

        function m(a,b)
        {
            return `${a} * ${b} = ${mul(a,b)}`;
        }

        function log(str)
        {
            console.log(str);
        }

        function num17()
        {
            let a = parseInt(prompt("a="));
            let b = parseInt(prompt("b="));
            log(m(a,b));
        }

        function operation(m,n,o)
        {
            return o(m,n);
        }

        function num18()
        {
            console.log(operation(5,4,mul));
        }

        function addN(n)
        {
            return x => x + n; 
        }

        function num19()
        {
            let n = parseInt(prompt("n="));
            let x = parseInt(prompt("x="));
            let func = addN(n);
            console.log(func(x));
        }

        function words(n)
        {
            let temp = n % 100;
            if(temp == 11 
            || temp == 12 
            || temp == 13 
            || temp == 14 ) return `${n} товаров`;

            temp = n % 10;

            switch(temp)
            {
                case 1: return `${n} товар`;
                
                case 2:
                case 3: 
                case 4: return `${n} товара`;

                default: return `${n} товаров`;
            } 
        }

        function num20()
        {
            let n = parseInt(prompt("n="));
            console.log(words(n));
        }

        
    </script>

<p>Во второй части были выполнены задачи с ресурса codewars.com:</p>
  <p>https://www.codewars.com/users/Meyson172/completed_solutions</p>
<h2>Вывод</h2>
<p>В ходе лабораторной работы были изучены элементы языка Java script. Были рассмотрены способы задания переменных, операций над ними, была проведена работа с циклами и функциями. Результатом лабораторной работы являются решенные задачами.</p>
