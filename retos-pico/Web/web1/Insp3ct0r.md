#  Insp3ct0r
# Objetivos
Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/9670/` ([link](https://jupiter.challenges.picoctf.org/problem/9670/)) or http://jupiter.challenges.picoctf.org:9670

# Solucion
```bash
--Html
<div id="tababout" class="tabcontent" style="display: none;">
	<h3>How</h3>
	<p>I used these to make this site: <br>
	  HTML <br>
	  CSS <br>
	  JS (JavaScript)
	</p>
	<!-- Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->
      </div>
}
--CSS
#tabintro { background-color: #ccc; }
#tababout { background-color: #ccc; }

/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */

--Js

window.onload = function() {
    openTab('tabintro', this, '#222');
}

/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?2e7b23e3} 
```

# Notas adicionales
Solo se requirió inspeccionar los archivos html, ccs y js para completar la bandera
# Referencias
