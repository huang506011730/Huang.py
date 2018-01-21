# Huang.py

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <link rel="stylesheet" href="css/main.css">
    <script src="../js/jquery-1.12.4.min.js"></script>
    <script>
     // 请写出实现的代码：
    $(function(){
        // 按钮单击，显示内容 -- 位移top上到居中；透明度opacity 0 - 1
        $('#btn').click(function(){
            $('.pop_main').show();
            // 规定死最初始的状态
            $('.pop_con').css({'top':0,'opacity':0})
            $('.pop_con').animate({'top':'50%','opacity':1})
        })
        // 动画反向
        // $('x').click()
        // $('quxiao').click()
        // h1,h2{}  -- css选中jq中都有，含义都相同
        $('.pop_title a,.cancel').click(function(){
            $('.pop_con').animate({'top':0,'opacity':0},600,function(){
                $('.pop_main').hide();
            })
            // $('.pop_main').hide(2000);
        })
    })
    </script>
</head>
<body>
    <input type="button" value="弹出弹框" id="btn">
    <div class="pop_main">
        <div class="pop_con">
            <div class="pop_title">
                <h3>系统提示</h3>
                <a href="#">×</a>
            </div>
            <div class="pop_detail">
                <p class="pop_text">亲！确定要这么做吗？</p>
            </div>
            <div class="pop_footer">
                <input type="button" value="取 消" class="cancel">
                <input type="button" value="确 定" class="confirm">                
            </div>
        </div>
        <div class="mask"></div>
    </div>
</body>
</html>
