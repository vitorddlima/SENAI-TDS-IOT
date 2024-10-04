# SENAI-TDS-IOT
Criação de repositório para as aulas de IOT

bancos de dados

CREATE DATABASE LojaOnline;
CREATE TABLE Clientes (
ClienteID INT PRIMARY KEY,
Nome VARCHAR(100) NOT NULL,
Email VARCHAR(100) UNIQUE NOT NULL,
DataCadastro DATE NOT NULL
);

INSERT INTO Clientes (ClienteID, Nome, Email,
DataCadastro) VALUES
(1, &#39;Ana Silva&#39;, &#39;ana.silva@example.com&#39;, &#39;2024-01-10&#39;),
(2, &#39;João Pereira&#39;, &#39;joao.pereira@example.com&#39;, &#39;2024-01-
12&#39;),
(3, &#39;Maria Oliveira&#39;, &#39;maria.oliveira@example.com&#39;, &#39;2024-
01-15&#39;),
(4, &#39;Carlos Santos&#39;, &#39;carlos.santos@example.com&#39;, &#39;2024-
01-20&#39;),
(5, &#39;Beatriz Lima&#39;, &#39;beatriz.lima@example.com&#39;, &#39;2024-02-
01&#39;),

(6, &#39;Pedro Costa&#39;, &#39;pedro.costa@example.com&#39;, &#39;2024-02-
05&#39;),
(7, &#39;Laura Almeida&#39;, &#39;laura.almeida@example.com&#39;, &#39;2024-
02-10&#39;),
(8, &#39;Fernando Silva&#39;, &#39;fernando.silva@example.com&#39;,
&#39;2024-03-01&#39;),
(9, &#39;Juliana Martins&#39;, &#39;juliana.martins@example.com&#39;,
&#39;2024-03-05&#39;),
(10, &#39;Marcos Pereira&#39;, &#39;marcos.pereira@example.com&#39;,
&#39;2024-03-10&#39;);

SELECT * FROM Clientes;
SELECT * FROM Clientes WHERE Nome = &#39;Ana Silva&#39;;
SELECT COUNT(*) AS TotalClientes FROM Clientes;
SELECT ClienteID, Nome
FROM Clientes
WHERE DataCadastro &gt;= &#39;2024-01-01&#39;;

2)
CREATE DATABASE LojaProdutos
GO
USE LojaProdutos
GO
CREATE TABLE Produtos(
ProdutosID INT IDENTITY,
Nome VARCHAR(150) NOT NULL,
Preco DECIMAL(10 ,2) NOT NULL,
Estoque INT NOT NULL
)
INSERT INTO Produtos(Nome, Preco, Estoque)VALUES
(&#39;FacaCozinhas&#39;,&#39;15.00&#39;,&#39;300&#39;),
(&#39;FacaSobrevivencia&#39;,&#39;10.00&#39;,&#39;250&#39;),
(&#39;FacaRambo&#39;,&#39;400&#39;,&#39;15&#39;),
(&#39;Canivetes&#39;,&#39;900&#39;,&#39;543&#39;),
(&#39;FacaColecionador&#39;,&#39;2000&#39;,&#39;1&#39;)
SELECT * FROM Produtos;
SELECT * FROM Produtos WHERE Preco &lt;= 50.00;
UPDATE Produtos SET Estoque = 0 WHERE Nome = &#39;FacaColecionador&#39;;
DELETE FROM Produtos WHERE Estoque = 0;

3) USE SistemaPedido
GO
CREATE TABLE Pedido(
PedidoID INT IDENTITY,
ClinteNome VARCHAR(50),
DataPedido DATE,
ValorTotal DECIMAL(10, 2),
)
INSERT INTO Pedido (ClinteNome, DataPedido, ValorTotal) VALUES
(&#39;Joao Silva&#39;, &#39;2024-05-20&#39;, 150.00),
(&#39;Maria Souza&#39;, &#39;2024-06-10&#39;, 300.00),
(&#39;Carlos Almeida&#39;, &#39;2024-07-01&#39;, 450.00),
(&#39;Ana Oliveria&#39;, &#39;2024-08-05&#39;, 200.00),
(&#39;PEdro Santos&#39;, &#39;2024-08-10&#39;, 150.00)
SELECT * FROM Pedido
SELECT *FROM Pedido
WHERE Datapedido &gt; &#39;2024-06-01&#39;;
UPDATE Pedido
SET ValorTotal =250.00
WHERE PedidoID =5;
DELETE FROM Pedido

WHERE ValorTotal &lt;200.00;
