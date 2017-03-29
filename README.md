# clipboard
复制剪贴板
`
<!DOCTYPE html>
<head>
    <meta charset="UTF-8">
    <title>clipboard示例</title>
    <script src="./clipboard.min.js"></script>
</head>
<body>
<!--data-clipboard-text属性的值将会被复制-->
<div id="btn" class="js-copy" data-clipboard-text="15260983827">
    <span>点击复制</span>
</div>

<script>
    var btn = document.getElementById('btn');
    var clipboard = new Clipboard(btn);//实例化

    //复制成功执行的回调，可选
    clipboard.on('success', function(e) {
        alert('复制成功')
    });

    //复制失败执行的回调，可选
    clipboard.on('error', function(e) {
        console.log(e);
    });
</script>
</body>
</html>
`
