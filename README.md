Nome : Lucas Gomes de Oliveira RGM:33596913

A seguir os comandos utilizados para criacao e consulta de rotas via POSTMAN:

criando usario POST 

localhost:8081/users/novouser

{
    "email": "exemplo@.com",
    "data_nasc": "2000-01-01", 
    "password": "123456789"
}
---------------------

fazendo login POST 

localhost:8081/users/login

{
    "email": "exemplo@.com", 
    "password": "123456789"
}

--------------------------

para consultar usuarios GET

localhost:8081/users/getUserById?id=1

none

-----------------------------------

1-rota para a criacao de um novo produto (post/products)

localhost:8081/products

{
    "nome": "Produto Teste",
    "descricao": "Descrição do Produto Teste",
    "preco": 99.99,
    "estoque": 100
}
----------------------------------------------

1-rota para listar todos os produtos (get/products)

localhost:8081/products

-----------------------------------------------

1-rota para atualizar um produto existente (PUT/products/9(ID))

localhost:8081/products/9(id)

{
    "nome": "Produto Atualizado",
    "descricao": "Nova descrição do produto",
    "preco": "79.99",
    "estoque": 80
}


---------------------------------------------

1-rota para deletar um produto(DELETE/products/9(id)

localhost:8081/products/9(id)

{
    "nome": "Produto Atualizado",
    "descricao": "Nova descrição do produto",
    "preco": "79.99",
    "estoque": 80
}

----------------------------------------------

2- Rota para adicionar um produto a cesta (POST/cart/add)

localhost:8081/cart/add

{
    "userId": 1,
    "item": {
        "id": 3,
        "nome": "Smartphone XYZ",
        "preco": 1999.99,
        "quantidade": 1
    }
}

--------------------------------------

2- rota para remover um produto da cesta (DELETE/cart/remove/id)


localhost:8081/cart/remove/{itemId}

{
    "userId": 1
}


----------------------------

2- rota para visualizar os iten na cesta (GET/cart)

none

localhost:8081/cart?userId=1


------------------------

3- rota para realizar o pagamento via cartao de credito POST

localhost:8081/payment/credit-card
{
    "userId": 1,
    "valorTotal": 100.00,
    "metodoPagamento": "cartao-de-credito"
}

-------------------------

3- rota para realizar o pagemento via pix POST 

localhost:8081/payment/pix

{
    "userId": 1,
    "valorTotal": 100.00,
    "metodoPagamento": "pix"
}

------------------------------------------------

3- rota para consultar a transacao GET

localhost:8081/payment/status/2

A seguir os comandos utilizados para consulta de rotas via MY SQL:

create database projetob1;
use projetob1;
create user 'projetob1'@'localhost' identified by 'qwerpoiu';
grant all privileges on *.* to 'projetob1'@'localhost' with grant option;
SELECT * FROM users;
SELECT * FROM products;
SELECT * FROM carts;
SELECT * FROM payments;
