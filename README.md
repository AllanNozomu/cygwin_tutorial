# Instalando e Utilizando o Cygwin no Windows

### 1. Requisitos mínimos

- Caso utilize Windows 10, sugere-se a instalação do Bash - http://www.ic.unicamp.br/~mc102/tutorial-bash.html. Esta instalação é recomendada para quem utiliza versões anteriores do Windows.
- É necessário aproximadamente 150MB de memória disponível

### 2. Introdução

Cygwin é um emulador de terminal com uma grande coleção de ferramentas GNU e Open Source, que disponibilizam funcionalidades similares às disponíveis em distribuições Linux no ambiente Windows. 
Este tutorial oferece um passo a passo para instalação e utilização do Cygwin, porém outras informações estão disponíveis neste [site](https://cygwin.com/install.html). Ao final deste tutorial você será capaz de compilar e rodar programas .c no terminal Cygwin diretamente no Windows, sem a necessidade de utilizar uma máquina virtual.

### 3. Instalando o Cygwin
Acesse https://cygwin.com/install.html e baixe o instalador - [setup-x86.exe](https://cygwin.com/setup-x86.exe) para Windows 32-bit e [setup-x86_64.exe](https://cygwin.com/setup-x86_64.exe) para Windows 64-bit

![alt text][img1]

Execute o arquivos de instalação - **setup-x86.exe** ou **setup-x86_64.exe**

![alt text][img2]

Clique em **Avançar** pelas próximas telas, selecionando as configurações de preferência em cada passo. Para a maioria dos usuários, as configurações que já vem por padrão são as mais adequadas.

![alt text][img3]
![alt text][img4]
![alt text][img5]

Selecione um diretório para salvar os arquivos de configuração do Cygwin. Neste diretório serão salvos também os pacotes (que iremos baixar logo menos). Coloque em um lugar que você não excluirá, pois isso afetará nos pacotes. Continue em **Avançar**;

![alt text][img6]

![alt text][img7]

Na tela para selecionar o site de download (mirror), clique **Avançar**. O instalador irá então fazer o download (pode demorar algum tempo).

![alt text][img8]

O instalador irá abrir uma tela para selecionar os pacotes que se quer instalar.

### 4. Instalando Pacotes

Pacote obrigatório: para compilar os programas, é necessário o pacote **gcc**.
1. Selecione na caixa de seleção a opção **Category**
2. Na caixa de busca **search**, digite o nome do pacote gcc. 
3. Na categoria Devel, selecione os pacotes **colorgcc** (4) e **gcc-core** (5), clicando sobre o Skip (bem embaixo do new).

![alt text][img9]

Pacotes sugeridos: além do gcc, há outros pacotes que podem adicionar funcionalidades interessantes. Algumas sugestões abaixo (procure na janela search):
- **gdb**: debugger de programas. Muito útil, porém requer realizar algum tutorial para aprender a utilizar. Há inúmeros tutoriais disponíveis na rede mundial, como [este](https://www.cs.umd.edu/~srhuang/teaching/cmsc212/gdb-tutorial-handout.pdf). Pacote está disponível na categoria **Devel**
- **openssh**: permite fazer conexão remota. Disponível na categoria **Net**
- **wget**: faz o download de arquivos da Web pela linha de comando. Disponível na categoria **Web**.

Concluída a seleção de pacotes, clique **Avançar**. Será mostrada uma tela com os pacotes selecionados para download. Mantenha selecionada a opção ``Select required packages (RECOMMENDED)`` e clique em avançar para fazer a instalação. A primeira instalação é bastante demorada, cerca de uma a duas horas. Vá tomar um lanche, faça uma caminhada! =)

![alt text][img10]

Se algum comando útil visto nas aulas ou laboratórios não estiver disponível no Cygwin ou você queira instalar outros pacotes posteriormente, rode novamente o arquivo de setup e utilize o selecionador de pacotes visto acima. O Cygwin não irá instalar tudo de novo, somente as novas adições.

Conclua a instalação adicionando o atalho à area de trabalho, será bem útil para facilitar seu uso.

### 5. Como utilizar

Para utilizar, basta rodar o atalho do programa. Será aberto um novo terminal. A pasta em que você estará, se encontra em `C:/cygwin64/home/NOME_DO_USUARIO/`. É nele que você deve inserir seus arquivos **.c** para serem compilados.

![alt text][img11]

Para saber se o **gcc** foi instalado corretamente, basta rodar o comando ``gcc -v``. Caso tudo esteja configurado corretamente, uma mensagem desse tipo sairá.

![alt text][img12]

Pronto, você configurou corretamente o Cygwin e ele está pronto para uso. Basta colocar os seus códigos na pasta `C:/cygwin64/home/NOME_DO_USUARIO/`, compilá-los usando o terminal e testá-los.

Qualquer dúvida ou erro de instalação, mande um e-mail para ra163527@students.ic.unicamp.br.

[img1]: imgs/img1.png ""
[img2]: imgs/img2.png ""
[img3]: imgs/img3.png ""
[img4]: imgs/img4.png ""
[img5]: imgs/img5.png ""
[img6]: imgs/img6.png ""
[img7]: imgs/img7.png ""
[img8]: imgs/img8.png ""
[img9]: imgs/img9.png ""
[img10]: imgs/img10.png ""
[img11]: imgs/img11.png ""
[img12]: imgs/img12.png ""
