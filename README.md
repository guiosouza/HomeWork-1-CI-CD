# CI/CD com GitHub Actions

O Script backend é para listar simplesmente os arquivos dentro da backend e no caminho acima dele também.

## CI (contínuos integration neste projeto).
Neste exemplo, o `pipeline` é acionado sempre que houver `push` ou `pull request` no `branch` principal (main). O `job` "run-tests" é definido para ser executado em uma máquina virtual Ubuntu.

Observação: o `pipeline` irá rodar nas versões do Node.js: 12.x, 14.x e 16.x. 

Os passos incluem a verificação do repositório (actions/checkout), a configuração do ambiente `Node.js` (actions/setup-node), a exibição da lista de arquivos no diretório (ls -la) e a execução dos comandos necessários para instalar as dependências do projeto (yarn install) e executar os testes (yarn test) no diretório do frontend.



