### 图片居中的方法：（四种方法）

##方法一：图片或者盒子放在table中<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        table {
            width: 600px;
            height: 400px;
            margin: 0 auto;

            border: 1px solid #CCC;
        }

        td {
            width: 300px;
            height: 300px;
            text-align: center;
            border: 1px solid #CCC;
        }

        td img {
            width: 200px;
            height: 100px;
        }
    </style>
</head>
<body>
    <table>
        <tr>
            <td>
                <img src="./images/1.png" alt="">
            </td>
        </tr>
    </table>
</body>
</html>
##方法二：模仿table(display: table)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title></title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #F7F7F7;
        }

        .wrap {
            width: 600px;
            height: 400px;
            margin: 80px auto;
            border: 1px solid #CCC;
            background-color: #FFF;

            display: table;
        }

        .cell {
            display: table-cell;
            
            text-align: center;
            vertical-align: middle;
        }

        img {
            width: 400px;
            height: 150px;
        }

    </style>
</head>
<body>
    <div class="wrap">
        <div class="cell">
            <img src="./images/1.png" alt="">
        </div>
    </div>
</body>
</html>
##方法三：把图片和span的基线对齐
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title></title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #F7F7F7;
        }

        .wrap {
            width: 600px;
            height: 400px;
            text-align: center;
            margin: 80px auto;

            border: 1px solid #CCC;
            background-color: #FFF;
        }

        img {
            /*对齐的两个元素的基线*/
            vertical-align: middle;
            width: 200px;
            height: 100px;
        }

        span {
            height: 100%;
            display: inline-block;

            vertical-align: middle;
        }
    </style>
</head>
<body>
    <div class="wrap">
        <img src="./images/1.png" alt="">
        <span></span>
    </div>
</body>
</html>
##图片定位+transform:
1.把图片定位，left:50%; top:50%;
2.用transform(-50%,-50%)