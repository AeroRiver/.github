# Documentação da AeroRiver Organization
<center>
    ![AeroRiver](https://github.com/AeroRiver/AeroRiverDocs/blob/main/docs/untitled.png)
</center>

## Repositórios Principais

A AeroRiver Organization visa criar um ambiente de versionamento e desenvolvimento dos códigos relacionados ao projeto AeroRiver. Temos dois repositórios principais:

1. **[ArduPilot](https://github.com/AeroRiver/ArduPilot):**
   - Repositório público que contém o trabalho realizado até agora.
   - Um fork do repositório de Matheus Miquelini, que, por sua vez, é um fork do código original e estável do ArduPilot.
   - Atualizado e sincronizado com base nas alterações do repositório pessoal do Matheus.
   - Contém a branch master da versão original e estável do ArduPilot para restauração e estudo do código base.

2. **[AeroRiver-ArduPilot](https://github.com/AeroRiver/AeroRiver-ArduPilot):**
   - Repositório privado para salvar e versionar alterações e códigos de voo específicos da AeroRiver.
   - Guarda versões e releases privadas.
   - Possui 4 branches e um fluxo de trabalho próprio.

## Branches no Repositório AeroRiver-ArduPilot

- **ground_effect:**
  - Branch principal, contém a versão estável e funcional mais atual do código de voo da AeroRiver.
  - Usada nos ensaios em voo dos protótipos.
  - Protegida para evitar pushs e merges que comprometam a integridade do código.

- **develop:**
  - Branch secundária dedicada a desenvolvimento e testes.
  - Contém a versão mais atual do código a ser submetida a testes de voo.
  - Protegida e requer revisão de outro desenvolvedor para aprovar pushs e merges.

- **gndefmode_develop, land_develop e ademais branches:**
  - Branches adicionais criadas e deletadas seguindo o fluxo de trabalho.

## Fluxo de Trabalho

O fluxo de trabalho na organização é baseado em branches e merges.

1. **ground_effect só deve receber merges da develop após validação:**
   - Código deve ser validado em testes de bancada e voo.
   - Develop sofre alterações mais frequentemente a cada nova feature desenvolvida.

2. **Atualização da develop:**
   - Novo requisito estabelecido.
   - Elaboração da solução.
   - Push da solução em nova branch.
   - PR para a develop.
   - Se o novo código foi testado e validado, PR da develop para ground_effect.

3. **Outras Considerações:**
   - Padronização: Novas branches devem ser nomeadas como `<nome>_develop`.
   - Após o término do desenvolvimento e do merge, a branch pode ser deletada.
   - O principal repositório de trabalho é o AeroRiver-ArduPilot.
   - Configurações dos repositórios e da organização ainda estão em progresso.
