![logo](https://github.com/user-attachments/assets/ee1ece32-0168-4a52-835c-e50308a7c57c)


Use o Gerenciador de Senhas para facilitar sua vida e ficar sempre seguro!

<br>
<h2>Funcionamento do Gerador de Senhas (v1.0):</h2> 
<br>

https://github.com/user-attachments/assets/e2a94fb0-20e6-476c-8015-73eded22418c

<br>

<img width="1552" alt="Captura de Tela 2024-10-18 às 16 46 11" src="https://github.com/user-attachments/assets/2e205261-5396-472d-9c69-80383cc31796">

<h1>Modernização do Gerador de Senha:</h1>

Colocamos em volta do #slider e do #input uma Box:

![Captura de Tela 2024-10-19 às 00 32 49](https://github.com/user-attachments/assets/3444c361-b633-4074-8af8-e73e4f54431f)

Explicação do que fiz:

![Captura de Tela 2024-10-19 às 01 24 19](https://github.com/user-attachments/assets/5e48850a-3023-41bf-9d7a-4f90f409885d)

<h3>CSS personalizado para o slider:</h3> <br>

![Captura de Tela 2024-10-19 às 00 37 55](https://github.com/user-attachments/assets/1888000b-d0ba-4a2a-ae33-3a6088bf23cb)

<br>

Explicação do que fiz:

![Captura de Tela 2024-10-19 às 01 29 16](https://github.com/user-attachments/assets/e71755c5-3af4-44b0-aee5-9823124cd6f3)

Porque eu usei isso?

![Captura de Tela 2024-10-19 às 01 29 30](https://github.com/user-attachments/assets/a8fe461e-19bd-4e63-8644-b3ac6225adfe)

<br>

<h1>Como fiz a lógica para gerar a senha aleatoriamente:</h1> <br>

![Captura de Tela 2024-10-19 às 02 07 54](https://github.com/user-attachments/assets/ce6f68e8-e33c-4c5c-95c5-d456cb30ac72)


```
let charset = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890!@#*-";
```

![Captura de Tela 2024-10-19 às 02 08 59](https://github.com/user-attachments/assets/599c21af-00f2-4f4f-a990-ee088eee6db5)


```
let sliderElement = document.querySelector("#slider");
```

![Captura de Tela 2024-10-19 às 02 10 19](https://github.com/user-attachments/assets/d12eca2c-73f5-4960-b035-4377b4804d1f)

```
function generatePassword() {
    let pass = "";  // Inicializa a variável que vai armazenar a senha gerada
    let n = charset.length;  // Armazena o tamanho do charset (quantidade de caracteres disponíveis)
    for (let i = 0; i < sliderElement.value; ++i) {
        // Sorteia um número aleatório baseado no tamanho do charset
        pass += charset.charAt(Math.floor(Math.random() * n));
    }
    containerPassword.classList.remove("hide");  // Mostra a senha gerada na tela
    password.innerHTML = pass;  // Exibe a senha gerada no HTML
    novaSenha = pass;  // Armazena a senha para uso posterior (cópia)
}

```
![Captura de Tela 2024-10-19 às 02 11 42](https://github.com/user-attachments/assets/5889fac0-1b66-4405-bc7c-84b9994a568e)

```
pass += charset.charAt(Math.floor(Math.random() * n));

```
![Captura de Tela 2024-10-19 às 02 12 44](https://github.com/user-attachments/assets/984084b8-8cbc-47ed-89f3-7538f83d95bc)

```
function copyPassword() {
    alert("Senha copiada com sucesso!");
    navigator.clipboard.writeText(novaSenha);  // Copia a senha gerada para o clipboard
}
```
![Captura de Tela 2024-10-19 às 02 14 57](https://github.com/user-attachments/assets/5c217c23-21ef-424e-a7d4-999878cf3f3a)



<br>
<h2>Final Versão (v2.0):</h2> 
<br>


<img width="776" alt="Captura de Tela 2024-10-19 às 00 43 32" src="https://github.com/user-attachments/assets/3696ccac-ce4f-41f6-92fb-294b421d2b37">





