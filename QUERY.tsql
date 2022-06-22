create database Db_Aula10x03
use Db_Aula10x03

1)Desenvolva um script em sql que mostre um contador até 100 e pare no numero 62

DECLARE @contador as int
SET @contador = 1
WHILE @contador <- 100
BEGIN
	IF @contador = 62
	BEGIN
		SELECT @contador
		BREAK
	END
SET @contador = @contador + 1

END
--------------------------------------------------------------------------------------------
2) Elabore um script em sql que apresente um contador até 1000 e mostre a soma dos
números multiplos de 3 e multiplos de 5 no final mostrar a soma de cada um deles

DECLARE @num as int
DECLARE @soma3 as int
DECLARE @soma5 as int
SET @num = 1
SET @soma3 = 0
SET @soma5 = 0

WHILE @num <=1000
BEGIN
	IF @num%3 = 0 --armazena a somatoria dos multiplos de 3
	BEGIN
		SET @soma3 = @soma3 + @num
	END
	IF @num%5 = 0 --armazena a somatoria dos multiplos de 5
	BEGIN
		SET @soma5 = @soma5 + @num
	END
SET @num = @num + 1 --contador
END
SELECT 'Soma dos multiplos de 3 =>' = CONVERT(CHAR(10), @soma3)
SELECT 'Soma dos multiplos de 5 =>' = CONVERT(CHAR(10), @soma5)

3) Crie um script em pl/sql que mostre os números de 1 até 100 e mostre se o número é par ou ímpar

DECLARE @num as int
SET @num = 1
WHILE @num <= 100
BEGIN 
	IF @num%2 = 0
	BEGIN
		SELECT 'Numero Par = ' + CONVERT(CHAR(10), @num)
	END
	ELSE
	BEGIN
		SELECT 'Numero Impar = ' + CONVERT(CHAR(10), @num)
	END
SET @num = @num + 1
END

4) Desenvolva um script em PL/SQL que apresente o resultado da variável idade que será
formada pela data atual, ou seja, dia + mês + 21 do ano igual a 4 + 3 + 21 e
mostrar como resultado:
-Menor que 10 = Criança
-De 10 até 17 = Jovem
-De 18 até 60 = adulto
-Acima de 61 = idoso

DECLARE @idade as int

SET @idade = DAY(GETDATE()) + MONTH(GETDATE()) +
CONVERT(int, SUBSTRING (CONVERT(CHAR(4), YEAR(GETDATE())), 3 , 2))

SELECT YEAR (GETDATE())

SELECT @idade,
CASE
WHEN @idade < 10 THEN 'Criança'
WHEN @idade >= 10 AND @idade <= 17 THEN 'Jovem'
WHEN @idade >= 18 AND @idade <= 60 THEN 'Adulto'
ELSE 'Idoso'
END as Resultado

5)Mostrar um PL/SQL se o aluno Mário da Silva está contido em uma variável,
bem como seu salário e calcular aumento de 10% para ele e mostre o nome em
letras maiúsculas

CREATE TABL

DECLARE @nome varchar (100)
DECLARE @salario NUMERIC (10,2)
DECLARE @NomeAluno varchar (100)

--define o valor de cada variavel
SET @nome = 'Mario da Silva'
SET @salario = 3000
SET @NomeAluno = (SELECT NomeAluno FROM Aluno WHERE @nome = NomeAluno)
select @NomeAluno

IF @NomeAluno = @nome
BEGIN
	SELECT 'Aluno contido ' + @nome
	SELECT 'Salario com 10% ' + CONVERT(CHAR(10), @salario * 1.1)
	SELECT 'Aluno ' + UPPER (@nome)
END

6)Elabore um laço de repetição usando PL/SQL que use while e quando o valor for 8, 
pare e finalize o programa;

DECLARE @contador as int
SET @contador = 1
WHILE @contador <= 10
BEGIN
IF @contador = 8
BEGIN
	SELECT @contador
	BREAK
END
SET @contador = @contador + 1
END

7)Desenvolva um script em PL/SQL que use duas variáveis e verifique se a media for
acima de 6, o aluno está aprovado. Se não, reprovado.

DECLARE @nota1 AS NUMERIC (3, 1)
DECLARE @nota2 AS NUMERIC (3, 1)
DECLARE @media AS NUMERIC (3, 1)
SET @nota1 = 8
SET @nota2 = 2
SET @media = (@nota1 + @nota2)/2

IF (@nota1 + @nota2)/2 > 6
BEGIN
	SELECT 'Aprovado' + CONVERT(CHAR(5), @media)
END
ELSE
BEGIN
	SELECT 'Reprovado' + CONVERT(CHAR(5), @media)
END

8)Elabore um script em PL/SQL que verifique os números de 1 até 100 e mostre a
quantidade de pares e impares no final, bem como a soma de todos os pares e também a soma
dos ímpares

DECLARE @contador AS INT
DECLARE @somapar AS INT
DECLARE @qtdepar AS INT
DECLARE @somaimpar AS INT
DECLARE @qtdeimpar AS INT

SET @contador = 1
SET @somapar = 0
SET @qtdepar = 0
SET @somaimpar = 0
SET @qtdeimpar = 0

WHILE @contador <= 100
BEGIN
IF @contador % 2 = 0 --par
BEGIN
	@somapar = @somapar + @contador
	@qtdepar = qtdepar + 1
END
ELSE --impar
BEGIN
	SET @somaimpar = @somaimpar + @contador
	SET @qtdeimpar = @qtdeimpar + 1
END
SET @contador = @contador + 1
END

SELECT 'Qtde de par: ' + CONVERT(char(10), @qtdepar)
SELECT 'Soma de par: ' + CONVERT(char(10), @somapar)
SELECT 'Qtde de impar: ' + CONVERT(char(10), @qtdeimpar)
SELECT 'Soma impar: ' + CONVERT(char(10), @somaimpar)

9)Crie um script em PL/SQL usando case que mostre um laço de repetiçao de 1 até 5000 e 
apresente a seguinte mensagem:
-Numero entre 1000 e 2000 = Analista Junior
-Numero entre 2500 e 4000 = Analista Pleno
-Else, Analista Sênior
