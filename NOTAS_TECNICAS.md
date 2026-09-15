# Notas técnicas

## Alterações feitas nesta cópia organizada

Os arquivos originais enviados pela autora foram preservados. Esta pasta contém cópias preparadas para portfólio.

### Caminhos relativos

Os caminhos locais usados nas transformações originais foram substituídos por `${Internal.Entry.Current.Directory}` para que os arquivos possam ser movidos junto com o projeto.

### Codificação do arquivo Clientes.csv

O arquivo fornecido está em uma codificação compatível com Windows-1252. As transformações 04 e 05 foram configuradas com essa codificação para preservar caracteres acentuados.

### Integração de vendas

Na planilha `vendas_pentaho_4_abas.xlsx`, a aba `Clientes` possui `idCliente`, enquanto `idRegiao` está na aba `Vendas`. Por isso, a cópia `06_integracao_vendas.ktr` foi organizada com a seguinte lógica:

`Vendas.idRegiao -> Regiao.idRegiao`, seguida da junção `Vendas.idCliente -> Clientes.idCliente`.

Esse ajuste evita relacionar campos semanticamente diferentes e mantém o fluxo coerente com a estrutura real da planilha.

## Recomendações antes de publicar

1. Abra cada `.ktr` no Spoon e execute uma vez na sua máquina.
2. Faça prints dos fluxos 03, 04, 05 e 06 e coloque na pasta `imagens`.
3. Se as bases forem material de treinamento com restrição de redistribuição, não publique `dados/entrada`.
4. Não publique apostilas/transcrições completas das aulas no repositório.
