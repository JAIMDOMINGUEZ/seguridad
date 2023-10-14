#  Scavenger Hunt
# Objetivos
There is some interesting information hidden around this site [http://mercury.picoctf.net:27278/](http://mercury.picoctf.net:27278/). Can you find it?

# Solucion
```bash
--HTML
|   |
|---|
||
|<p>I used these to make this site: <br/>|
||HTML <br/>|
||CSS <br/>|
||JS (JavaScript)|
||</p>|
||<!-- Here's the first part of the flag: picoCTF{t -->|
||</div>|
|||

--CSS
#tabintro { background-color: #ccc; }
#tababout { background-color: #ccc; }

/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */

--robots
User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?
--.htaccess
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
--.DS_Store
Congrats! You completed the scavenger hunt. Part 5: _a69684fd}
```

# Notas adicionales


# Referencias
