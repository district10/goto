# goto

用于重定向。

## Template

```html
<!DOCTYPE html>
<html>
<head>
    <meta HTTP-EQUIV="REFRESH" content="10; url=http://tangzx.qiniudn.com/...">
    <style> .target { color: red; } </style>
    <script>
    var target = "Post: Title";
    var seconds = 10-1;
    window.onload = function() { countdown('countdown'); }

    function countdown(element) {
        setInterval(function() {
            var el = document.getElementById(element);
            if(seconds <= 0) {
                el.innerHTML = "Redirecting to '<strong class='target'>" + target + "</strong>'...";
                return;
            }
            var second_text = seconds > 1 ? "seconds" : "second";
            el.innerHTML = "Will be redirected to '<strong class='target'>"
                         + target
                         + "</strong>' in "
                         + seconds + " " + second_text + ".";
            --seconds;
        }, 1000);
    }
    </script>
</head> <body> <div id='countdown'>TZX Redirection Page.</div> </body> </html>
```
