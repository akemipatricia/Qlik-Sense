
**Objetivo:** \
Ao selecionar um filtro de Ano ou Região as categorias selecionadas aparecerão no título.
Isto facilitará na organização visual do usuário.



> ='Municípios que Implantaram a Rede Simples' &
>	if(getfieldselections([UF - DSIGPM])>0,
>    	(if(GetFieldSelections([Ano - DSIGPM])>0,
>        	(' - ' & GetFieldSelections([UF - DSIGPM]) & ', ' & GetFieldSelections([Ano - DSIGPM])),
>            (' - ' & GetFieldSelections([UF - DSIGPM])))),
>        (if(GetFieldSelections([Ano - DSIGPM])>0,
>        	(' - ' & GetFieldSelections([Ano - DSIGPM])),
>            '')))
        
        
  
