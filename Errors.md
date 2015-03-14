**if error Access Denied during loading programm.**

**Если ошибка "отказано в доступе" во время загрузки**

Например: При запуске выдает ошибку:
_"Во время выполнения произошла ошибка. Запустить отладку?
Строка такая-то,
Ошибка: отказано в доступе"_

тогда попробуйте в файле kernel.txt в каталоге bin в самом конце код:

**then try to find next code in bin/kernel.txt (at the end of file)**

> if(kernel.vars.user.mda){
> > kernel.fns.loadUser();

> }else{
> > window.close();

> }
}
window.setTimeout("kernel.fns.loader()", 200);


замените на:

**replace to the following**

> if(kernel.vars.user.mda){
> > window.setTimeout("kernel.fns.loadUser()", 500);

> }else{
> > window.close();

> }
}
window.setTimeout("kernel.fns.loader()", 200);


может быть поможет...

у меня тоже бывает, но редко...