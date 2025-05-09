# CI

## Build - ok

- A implementar, caso desejado:

Cache?

## Tests - ok

Na esteira, melhor transformar em uma etapa da build? R: Sim.

VSTest está deprecated, tem problema? R:

## SonarQube - ok

Anotações:
Deve ter o mesmo nome: projeto do github e projeto do sonar, para poder generalizar a project key com ${{ github.event.repository.name }}
A organization key não muda, a project key muda a cada projeto.
A organtization key a nível enterprise e a nível.... (esqueci o nome)

O ${{ vars.ORGANIZATION_SONAR }} está em hardcoded, mas nesse caso não tem problema.

## Salvar os binários para CD - ok

Anotações:
Por padrão vai para /bin/Release
${{ inputs.app-directory }}/bin/Release/

# CD

## Copiar os binários do CI para um file server - ok

Pode github releases? R: Sim, e é uma ótima ideia.

- A corrigir:

Tag de versão automática