# Local Authority
# Objetivos
Can you get the flag?Go to this [website](http://saturn.picoctf.net:50920/) and see what you can discover.
# Solucion
```bash
  
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```
![[Pasted image 20231024000431.png]]
# Notas adicionales

# Referencias
