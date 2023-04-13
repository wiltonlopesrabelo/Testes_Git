## Informações da Task (YouTracker):
[SP-XXXXX](https://tracker.casamagalhaes.com.br/youtrack/issue/SP-XXXXX)

Verificar se a Task (YouTracker) que originou esse PR, contem os seguintes tópicos:
- Raiz do Problema (hotfix).
- Ajustes.
- Testes Realizados (Funcionais e/ou Unitários).
    OBS.: Caso não esteja preenchido, solicitar ao desenvolvedor que descreva na tarefa o motivo.
- Testes Sugeridos.

## Informações Sobre a Revisão:

* [] Review da funcionalidade para o revisor.
* [] Verificar se o implementado condiz com o solicitado na Task (YouTracker).
* [] Revisão do código com o revisor.

## Pontos de Verificação:
    
### Padrões de Codificação ([Unit Modelo](https://gist.github.com/AnselmoMS/6381d271a134122ee76dcb47abbfd5a6)):
* [] Units, por padrão, sem cabeçalhos.
* [] Verificar se os objetos criados, estão sendo liberados.
* [] Seção uses: colocar uma após a outra na mesma linha.
* [] Usar o prefixo L para variáveis locais (procedure e function).
* [] Máximo 120 linhas no código.
* [] Nomenclatura de arquivos:
        Form/Frame -> ViewCadastroProduto (objeto)
                   -> View.CadastroProduto.pas
                   -> View.CadastroProduto.dfm
        DataModule -> Module.[NomeDoModulo].pas
                   -> Module.[NomeDoModulo].dfm
        Controller -> Controller.[NomeDaClasse].pas
        Model      -> Model.[NomeDaClasse].pas
        Units Sem Container -> Server.Model.Produto.pas
                            -> PDA.Controller.Menu.pas
                            -> Comum.Helpers.DateTime.pas
### Verificações Gerais:
* [] Verificar a ortografia, principalmente dos textos visíveis aos usuários.
* [] Não criar restrições nos bancos de dados SYSPDV_CAD.fdb nem SYSPDV_MOV.fdb.
* [] Toda vez que adicionar um campo a ITEVDA e ITEVDA_DESCONTO, ajustar os envio dessas novas informações pelo Sysnet para o SYSPDV_SRV.fdb.
* [] No SysPDV PDV, ao precisar realizar consultas nas tabelas que descem na carga, utilizar a conexão FmDadcx.TQGeralCAD. Essa conexão, é alterada conforme a configuração da carga.
* [] Não implementar/utilizar classes que herdam de TEntity e TModule no SysPDV PDV. 
* [] Verificar se o SysPDV PDV continua funcionando mesmo depois do SysPDV Server ficar offline.
* [] Caso exista alteração em código com a query TQCupom, analisar o impacto sobre os eventos dessa query (AfterPost, BeforePost e etc).
