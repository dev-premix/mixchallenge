# mix-challenge
## Problema:
Em um determinado confinamento temos a necessidade de saber qual vai ser a quantidade de ração a ser entregue no cocho, para isso a tecnologia precisa ajudar o tratador.

O tratador irá predefinir qual o numero de animais e seu tipo em cada confinamento, e com isso o sistema irá apontar qual seria a quantidade necessária de ração por dia.

## **Desafio:** 
Criar um sistema simples que auxilie o tratador em suas tarefas diárias.

Não é necessário implementar um banco de dados, estes dados podem ser armazenados em memória no backend.

Para os métodos de login, manter dois usuários cadastrados:
```json
[
	{
		"userName": "admin",
		"password": "admin",
		"admin": true
	},
	{	
		"userName": "tratador",
		"password": "tratador",
		"admin": false
	}
]
```
## 1 – Backend
Elaborar um backend em NodeJS com os seguintes serviços:

### - Autenticação
Criar um serviço de autenticação baseado em token, onde quando um usuário se autenticar o sistema devolva um token e nos serviços onde é necessário o login o sistema valide este token.

PS: Não é necessário implementar JWT, pode apenas criar um hash qualquer e validar este hash posteriormente.
### - Confinamento (CRUD)
Cadastro básico com os seguintes campos
```json
{
	"id": "Number",
	"nome": "String",
	"qtdBovinos": "Number",
	"qtdEquinos": "Number",
	"inicioConfinamento": "Date",
	"fimConfinamento": "Date",
	"usrCriacao": "String"
}
```
Lembrando que para efetuar o cadastro o usuário precisa estar logado com um usuário administrador.

Criar também todas as etapas de cadastro (CRUD).
### - Trato
Criar um serviço que poderá ser acessado por usuários admins ou não, onde passado um parâmetro com o código do confinamento o sistema seja capaz de retornar todas as quantidades de tratos diários projetado até a data final do confinamento.


Sabe-se que um Boi começa o confinamento com 400kg e um Cavalo começa o 200kg, o ganho de peso diário é em torno de 800gr para o cavalo e 1.1kg para o Boi, e o trato diário de cada animal é em torno de 0.005% do seu peso, com base nessas informações já é possível calcular o peso projetado do rebanho e a quantidade de ração necessária para cada dia.
## 2 – Front-end

- Elaborar um template administrativo (Header, footer, side-menu) utilizando React

- Tela de login que faz uso do serviço de autenticação

- Cadastro de Confinamento

- Listagem de confinamentos e tratos

## 3 – Mobile
- Elaborar um aplicativo utilizando ReactJS

- Tela de login

- Listagem de confinamentos e tratos


# Avaliação
## O que será avaliado
* Organização de código: Clareza, resultado funcional, limpeza do código, comentarios, etc...
* Separação das camadas de dados
* Reusabilidade de código e desacoplamento das camadas de negócios
* Fique a vontade para criar seu próprio layout e estilo
* *Ahh, não se esqueça de documentar os procedimentos para executar a aplicação.*
## Diferenciais
* Tornar o layout do front-end responsivo.
* Utilização de boas praticas de UX



Boa sorte,  
Equipe Premix  
dev@premix.com.br
