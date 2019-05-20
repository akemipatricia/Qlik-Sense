Formato da variável que indica o ano: "ABC 2019 - 2019"
Formato da variável que indica o mês: "Abril" (nome dos meses em português)

Teste colocar estes campos no filtro e selecionar utilizando as seguintes funções, lembrando que é necessário repetir o *"=[Ano]={expressão aqui}"*.
Exemplo:

> [Ano]={"=Right([Ano],11) =  year(now()) & ' - ' & year(now())"}

> [Mês]={"=[Mês]=$(vMesAtual)"}>}

Depois fazer as seleções no filtro, vá para "Marcadores" > "Criar novo marcardor".
Ao final, a expressão abaixo representará o seu marcador.

> {<[Ano]={"=Right([Ano],11) =  year(now()) & ' - ' & year(now())"},

> [Mês]={"=[Mês]=$(vMesAtual)"}>}
