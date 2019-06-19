
**Objetivo:** \
Ao selecionar um filtro de Ano ou Região as categorias selecionadas aparecerão no título.
Isto facilitará na organização visual do usuário.

**Exemplo:** \
Neste exemplo foram utilizadas dois campos, o de Ano e o de UF. Para aplicar no seu título basta copiar e substituir pelos seus campos corretamente.

```bash
 ='Média de carros por metro quadrado' &
	if(getfieldselections([UF])>0,
    	(if(GetFieldSelections([Ano])>0,
        	(' - ' & GetFieldSelections([UF]) & ', ' & GetFieldSelections([Ano])),
            (' - ' & GetFieldSelections([UF])))),
            
        (if(GetFieldSelections([Ano])>0,
        	(' - ' & GetFieldSelections([Ano])),
            '')))
```
        
**Resultado:** \
No final, supondo que tenha sido selecionado a UF de DF com o ano de 2019 o resultado do título seria: \
*Média de carros por metro quadrado - DF, 2019*. 

O *default*, sem nenhuma seleção de UF ou Ano, é: \
*Média de carros por metro quadrado - DF, 2019*
  
