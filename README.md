# CI

## Build - ok

- A implementar, caso desejado:

Cache?

## Tests - ok

- Dúvidas:

Na esteira, melhor transformar tests em uma etapa da build? R: Sim, feito. <br>

VSTest está deprecated, tem problema? R:

- Testar:

E se não tiver testes? O que acontece? R: 


## SonarQube - ok

- Anotações:

Deve ter o mesmo nome: projeto do github e projeto do sonar, para poder generalizar a project key com ${{ github.event.repository.name }} <br>
A organization key não muda, a project key muda a cada projeto. <br>
A organtization key a nível enterprise e a nível.... (esqueci o nome) <br>

O ${{ vars.ORGANIZATION_SONAR }} está em hardcoded, mas nesse caso não tem problema.

## Salvar os binários para CD - ok

- Anotações:

Por padrão vai para /bin/Release <br>
${{ inputs.app-directory }}/bin/Release/

# CD

## Copiar os binários do CI para um file server - ok

- Dúvidas:

Pode github releases? R: Sim, e é uma ótima ideia.

- A corrigir:

Tag de versão automática