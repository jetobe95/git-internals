## Git bisect 🐞

[Using Git Bisect](https://www.youtube.com/watch?v=P3ZR_s3NFvM)

Encuentra un bug 🐞 con git

1. Iniciar el proceso  `git bisect start`
1.  Establecer cual fué el commit que no tenía el bug `git bisect good d5a6ab4`
1. Si el bug persiste `git bisect bad`
1. Si el bug no sale  `git bisect good `
1. Iterar los pasos 3 y 4 anteriores hasta que se obtiene
```
git bisect good        
4bf5c63a0289ea8184503f50726d6421a5953674 is the first bad commit
```
6. Para finalizar y  reiniciar el `HEAD` ejecutar `git bisect reset`
