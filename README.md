# CI/CD com GitHub Actions

O Script backend é para listar simplesmente os arquivos dentro da backend e no caminho acima dele também.

## CI (contínuos integration neste projeto).
Neste exemplo, o `pipeline` é acionado sempre que houver `push` ou `pull request` no `branch` principal (main). O `job` "run-tests" é definido para ser executado em uma máquina virtual Ubuntu.

Observação: o `pipeline` irá rodar nas versões do Node.js: 12.x, 14.x e 16.x. 

Os passos incluem a verificação do repositório (actions/checkout), a configuração do ambiente `Node.js` (actions/setup-node), a exibição da lista de arquivos no diretório (ls -la) e a execução dos comandos necessários para instalar as dependências do projeto (yarn install) e executar os testes (yarn test) no diretório do frontend.

## RODANDO UM TESTE:

1 - cicd.yaml alterado para rodar um teste.
2 - Esse teste verifica a existência das pastas dentro da raiz "frontend" e das pastas no caminho acima.

![image](https://github.com/guiosouza/HomeWork-1-CI-CD/assets/78989152/54133298-9737-486b-88ab-4b5c683bc13d)

TESTANDO:

![image](https://github.com/guiosouza/HomeWork-1-CI-CD/assets/78989152/f6e5120f-22bf-45b1-9bc2-2a81eea7da86)

Passando no teste:

![image](https://github.com/guiosouza/HomeWork-1-CI-CD/assets/78989152/21963fca-2320-419a-8c03-0b543b2f7519)


![image](https://github.com/guiosouza/HomeWork-1-CI-CD/assets/78989152/fd656a97-de48-4510-8b5f-bfd21ce1d22f)

Havia modificado somente para rodar 'ls & la':

![image](https://github.com/guiosouza/HomeWork-1-CI-CD/assets/78989152/d687e6aa-8e76-40bb-8922-7f9568ed9ccb)


# ÚLTIMO TESTE:

1 - run: la - la (varredura pelas pastas)
2 - run: cd ./frontend && yarn install && yarn test && ls - la (navega até a pasta "frontend", dá o yarn install para a MV, roda o yarn test e no final faz a varredura das pastas)

## Resultados:

![image](https://github.com/guiosouza/HomeWork-1-CI-CD/assets/78989152/570afa0f-9c43-4d21-b686-d37eeadd7a3a)


![image](https://github.com/guiosouza/HomeWork-1-CI-CD/assets/78989152/f46c4167-f28a-427c-a1ad-53071ad7016e)


![image](https://github.com/guiosouza/HomeWork-1-CI-CD/assets/78989152/6ebec55c-1aa5-4687-8223-0b64b3b934bd)


