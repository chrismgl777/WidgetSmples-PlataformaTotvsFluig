
![Green Modern Corporate Personal Vlog YouTube Banner (4)-Photoroom](https://github.com/user-attachments/assets/a4885042-7c9b-434b-987f-4e561538aa3d)


<h1> Criando o projeto no Eclipse</h1>
Começamos criando o projeto no Eclipse: <br>
Primeiro, dentro da aba "Project Explorer" , com o botão direito, abrimos uma aba, que possibilita realizarmos algumas tarefas.<br>
Dentro dela, clicamos na opção "New", logo após, clicamos no "Projeto Fluig".<br>

 ![image](https://github.com/user-attachments/assets/d62cb22c-be86-436c-b35e-291e19b4630e)<br>
Depois, inserimos o nome do projeto que queremos.<br>

![image](https://github.com/user-attachments/assets/c5a62c6e-ae17-4fc3-ad3d-129c50041bd0)<br>

<h1> Criando o Widget dentro do projeto</h1> 
Já com o projeto criado, vamos até a pasta de Widget e criar um novo. <br>

![image](https://github.com/user-attachments/assets/52bdf04d-3c15-461a-a943-3ac1b0c18589)<br>

 ![image](https://github.com/user-attachments/assets/06d1479a-c320-4fe6-b2cb-1d961f720d35) <br>
Após clicarmos no  "Other" buscando mais opções, encontramos a que estamos buscando , o "Widget" : <br>
![image](https://github.com/user-attachments/assets/dc6f06d3-cd1e-433a-a6fc-d05017d805d8) <br>
Após iniciarmos a escolha do Widget,precisamos inserir algumas informações, tais como: <br>
![image](https://github.com/user-attachments/assets/27e173f3-d235-40aa-bf93-8fa7d8c8c873) <br>

°  Código <br>
°  Nome <br>
°  Descrição <br>
°  Template <br>

Utilizamos o código para legitimizar um nome para o Widget, funciona da mesma forma que um Dataset.. com nomes em estilos underscore. <br>
O nome, podemos colocar algo que seja ligado ao Widget. <br>
A descrição é aonde colocamos uma frase ou texto curto evidenciando o widget. <br>
O template, possui algumas formas de instanciar o Widget, com alguns templantes prontos, porém, desta vez, vamos instanciar com o tamplete padrão, zerado. <br>
Já com o Widget criado, podemos acessar sua pasta e iniciar. <br>
Essa é a estrutura do Widget que criamos: <br>

![image](https://github.com/user-attachments/assets/22d5c5b7-239b-467d-93b9-b9c9da1cef07) <br>

Essa é a instancia padrão ao criar uma Widget:<br> 

![image](https://github.com/user-attachments/assets/e8818727-d565-48d0-b143-8c401e47e310) <br>

Podemos analisar, que ao criar a Div, a instancia esta com o nome padrão, criado pelo Eclipse, com ID chamado:"MyWidget_${instanceId}". <br> 
É recomendado, que coloquemos o nome da instancia que estamos criando o widget ou algo que arremate a isso. <br>
Sendo assim, troquei para WdgUsuariosAtivos<br>

![image](https://github.com/user-attachments/assets/36267fd9-b4c9-48b7-a814-27cc71303322) <br>

Vamos fazer isso no Edit.ftl e View.ftl: <br>

![image](https://github.com/user-attachments/assets/e2a1a0e8-a192-4dd2-a487-2f83edfee89a) <br>

No Edit.ftl, vamos iniciar com um H3, criando um titulo para separar o Edit do View : <br>

![image](https://github.com/user-attachments/assets/914acdb1-6b19-48b2-b8ab-479996127007) <br> 

Vamos até o JavaScript da nossa aplicação ?? <br>

![image](https://github.com/user-attachments/assets/3cb9c820-7613-4d1b-869f-902ca0293081) <br>

Lembra que trocamos o nome da instancia no edit.ftl e view.ftl ? Vamos fazer a mesma coisa no JavaScript. <br>
Colocamos o mesmo nome da instancia anterior : <br>

![image](https://github.com/user-attachments/assets/26ece01b-641f-4be5-91f7-6998280478d0) <br>

<h1> Breve Explicação sobre o  Código Default do JavaScript da Widget</h1>

![image](https://github.com/user-attachments/assets/7bfba9ed-e62c-4e73-a0c1-d85591bd6cbc) <br>
Colocamos o nome da viravel principal da Widget, e extendemos uma classe chamada SuperWidget. <br>
Podem saber mais neste link: https://style.fluig.com/javascript.html <br>
Aqui, podemos localizar alguns váriaveis ja criadas por default, vamos retirar elas e criar, por hora, somente uma: <br>

![image](https://github.com/user-attachments/assets/5303a522-f747-43cb-84a6-82bdd759532d)
Vamos criar a variavel usarTable, que mais pra frente, você vai entender o porque. <br>

![image](https://github.com/user-attachments/assets/408f0ffc-63ae-45bd-a49a-9b997ab35452) <br>
Oque esse Script vai fazer para nossa Widget ? Ele vai chamar um dataset e apresentar dentro da nossa wWidget. Para isso, necessitamos de um componente. <br>
Também precisamos criar uma estrutura que vai ficar em volta desses dados que o Dataset vai fornecer, então precisamos criar uma estrutura no View.ftl, para que possa receber e estruturar corretamente os dados. <br>
Vamos precisar de um Componente chamado Panels, podemos encontrar todos os componentes nesse link da Totvs: https://style.fluig.com/components.html#panels <br>

![image](https://github.com/user-attachments/assets/f37f0de7-04e8-4a6f-82ba-ba9f53fc9192) <br>
Colocamos um panels em modo default, podemos alterar o tipo de cor dele, trocando o default para Info: <br>

![image](https://github.com/user-attachments/assets/7a7df64d-6bc6-4b46-bd81-36bab8d710aa) <br>
Agora que ja estruturamos uma parte do Front, precisamos voltar para a estrutura de JavaScript, dentro da pagina do Totvs Fluig Developer, possui o menu JavaScript, dentro dele, vamos procurar o componente chamado dataTable. <br>
Vocês podem aprender melhor na parte "Usage" dentro da aba do dataTable<br>
Dentro do panels que criamos, precisamos utilizar o dataTable agora : <br>

![image](https://github.com/user-attachments/assets/7a71dc20-c98b-4555-b46a-93601aa79e65) <br>
Dentro do Id, que por default no site vem como Target, precisamos alterar para UserTable, que é a tabela de usuario e instanciar o ID dinamico. <br>

![image](https://github.com/user-attachments/assets/f6f57108-dc7b-4bcd-8099-2680f72e4c1b) <br>
Agora, precisamos criar um metodo inicial, precisamos montar a estrutura para chamarmos o dataset. <br>
Aqui possuimos uma estrutura pronta, que vamos utilizar para iniciar <br>
Vamos falar sobre essa estrutura no decorrer do tutorial.  <br>

![image](https://github.com/user-attachments/assets/0f59ad93-68c9-444f-be68-3af21e95829a)
Precisamos realizar alguns passos : <br>

![image](https://github.com/user-attachments/assets/b7bda835-febf-459f-a210-82277b7cd514) <br>
Vamos chamar um metodo inicial, chamado "loadTable();". Lembrando que ja instanciamos o userTable, no View.ftl, agora precisamos iniciar toda a parte do back. <br>
 
 ![image](https://github.com/user-attachments/assets/2a5b38b3-3812-4b09-9c76-68f604ffdba9) <br>
Dentro dessa função que estamos criando, vamos inserir aquele código que pegamos anteriormente no Fluig Developer. <br> 
Dentro da função, inserimos ele : <br>

![image](https://github.com/user-attachments/assets/8cb74277-16e2-4cee-a409-acf5c7374769) <br>

Como estamos instanciando uma chamada de Dataset, precisamos realizar essa configuração no Front. Vamos utilizar um script e utilizar o XML. <br>
![image](https://github.com/user-attachments/assets/d0615faa-12b6-4ced-9b00-b62eacc882c0) <br>
Vamos voltar para a função ! <br> 
Dentro do JavaScript do Widget, vamos realizar algumas configurações e retirar o execesso de código que vieram por default da Totvs Fluig Developer <br>
![image](https://github.com/user-attachments/assets/265cd104-78b8-4b7b-b166-c37edc873da1) <br>
Inserimos o "this." no loadTable(). <br>
Vamos retirar essa parte : <br> 
![image](https://github.com/user-attachments/assets/a04a54f3-a7e7-477d-93c2-6c3caa9d9043) <br>
Como ja possuimos a função logo acima,também não precisamos desta, então vamos apagar : <br>
![image](https://github.com/user-attachments/assets/5d3a0393-2bec-41e1-9a16-d0e59d48a4bc) <br>
Vamos apagar suas chaves abaixo também : <br>
Vamos apagar essas duas : <br>
![image](https://github.com/user-attachments/assets/33b992b1-4227-426f-b6fd-e3bb1b6789f6) <br>
Lembra que recentemente, instanciamos o table dentro do panels ? Configuramos a estrutura: <br>

![image](https://github.com/user-attachments/assets/27498de7-c998-4bf5-8d7b-8ba9a5ba74ea) <br>
Pode reparar, que  no código a seguir, eles pedem o id do table e a instancia: <br>
![image](https://github.com/user-attachments/assets/6cf46a93-83f4-4dda-8e78-ebd93c98c85f) <br>
Vamos inserir  conforme o view.ftl !! <br>

![image](https://github.com/user-attachments/assets/4b5a26d2-9b7d-40db-941a-f4376adf127f) <br>
Que veio desse código: <br>
![image](https://github.com/user-attachments/assets/525ec3ba-95f0-4102-8922-49001669a69e) <br>

Após instanciarmos corretamente a tabela, vamos configurar os dados e o dataset que vai aparecer. <br>
Vamos utilizar um dataset ja existente no FluigAcademy, porém, podemos utilizar qualquer um. <br>
Vou explicar o passo a passo. <br>
Entendendo a estrutura: <br>
Primeiro,vamos consultar o dataset "Colleague" no eclipse ? Vamos estender como ele esta funcionando: <br>
Esse é o Dataset Colleague e seus dados armazenados: <br>
![image](https://github.com/user-attachments/assets/8ec64c4a-1061-4c6b-98ac-1ef6677d95f3) <br>

![image](https://github.com/user-attachments/assets/0973d63c-dbc4-4678-8098-9b6958bde92d) <br>
O "dataRequest" é aonde vamos inserir qual o Dataset que vamos fazer a chamada, quen esse caso , é o "colleague". <<br>
O "renderContent" é o nome das colunas que vamos apresentar, sendo assim:  <br>
No  dataResquet, vamos por qual colunas queremos requisitar e no renderContent, colocamos um titulo para elas, então os dados vão vir do dataRequest e o renderContent vai dar um nome. <br>
Vamos exportar para o Fluig ! <br>
Já com a exportação realizada ( Eu ensinei no tutorial sobre os Datasets ), vamos entrar no Fluig, criar uma pagina e por para visualizarmos nosso widget. <br>

<h1> Criando uma pagina na Plataform Fluig</h1>

Já com o Fluig aberto, precisamos ir no Painel de Controle. <br>
No painel de controle, localizar a coluna com o nome de "Personalização" <br>
![image](https://github.com/user-attachments/assets/cf5731ab-bf9e-40fa-b8ad-9318b061cbda) <br>
Dentro dessa coluna, localizar a tarefa chamada "Minhas paginas" <br>
![image](https://github.com/user-attachments/assets/b75cc79a-fa1b-4200-9e7e-1c9cef74396a) <br>
Com a tarefa aberta, vamos criar nossa pagina ! <br>
![image](https://github.com/user-attachments/assets/f3beaa38-1455-4a97-92f7-82cdd0f0f296) <br>
Aqui escolhemos qual lauyout ela vai possuir, nesse caso, escolhi a "meio a meio", para que widget possua um tamanho bom. <br>
![image](https://github.com/user-attachments/assets/8828c029-66b2-4b56-969c-9ec938131ee9)
Agora vamos configurar a pagina: <br>
![image](https://github.com/user-attachments/assets/2b0d27c6-d152-4e97-a7b3-3d360487d537) <br>
Podemos colocar o nome da pagina, descrição, identificador unico e escolher a forma que vai ficar a url. <br>
Agora, com a pagina criada, precisamos instanciar o widget criado por nós: <br>
![image](https://github.com/user-attachments/assets/b92dfa5e-690d-4515-9b97-5e6b1f65fa51) <br>
Dentro da coluna Widgets, vamos achar a aba "SYSTEM", é lá onde esta nossos widgets exportados. <br>
![image](https://github.com/user-attachments/assets/f6cba298-e044-4e0c-8fd7-9bb5dfef105e) <br>
Escolhemos o widget, arrastamos para dentro do layout e publicamos. Ficando desta forma: <br>
![image](https://github.com/user-attachments/assets/c88149f2-2cb9-4598-9634-67b5229bfe1e) <br>
Pronto, criamos um widget que instancia dados de um Dataset. 




































 




