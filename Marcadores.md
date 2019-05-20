**Criar filtros fixos quando abrir o Painel.**

Formato da variável que indica o ano: "ABC 2019 - 2019" \
Formato da variável que indica o mês: "Abril" (nome dos meses em português)

Neste exemplo, o campo de mês está em português o que dificulta quando utiliza a função *monthname*. Então, foi criado a seguinte variável com o nome *vMesAnterior*: 

  *if(month(now())-1=1,'Janeiro', \
	if(month(now())-1=2,'Fevereiro', \ 
  if(month(now())-1=3,'Março',  \
  if(month(now())-1=4,'Abril',  \
  if(month(now())-1=5,'Maio',  \
  if(month(now())-1=6,'Junho',  \
  if(month(now())-1=7,'Julho',  \
  if(month(now())-1=8,'Agosto',  \
  if(month(now())-1=9,'Setembro',  \
  if(month(now())-1=10,'Outubro',  \
  if(month(now())-1=11,'Novembro',  \
  if(month(now())-1=12,'Dezembro'))))))))))))*
    
    
Teste colocar estes campos no filtro e selecionar utilizando as seguintes funções, lembrando que é necessário repetir o *"=[Ano]={expressão aqui}"*. \
Exemplo:

> [Ano]={"=Right([Ano],11) =  year(now()) & ' - ' & year(now())"} \
> [Mês]={"=[Mês]=$(vMesAnterior)"}>}

Depois fazer as seleções no filtro, vá para "Marcadores" > "Criar novo marcardor".
Ao final, a expressão abaixo representará o seu marcador.

> {<[Ano]={"=Right([Ano],11) =  year(now()) & ' - ' & year(now())"}, \
> [Mês]={"=[Mês]=$(vMesAnterior)"}>}
