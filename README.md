# Documentação da AeroRiver Organization
<p align="center">
  <img src="https://github.com/AeroRiver/AeroRiverDocs/blob/main/docs/untitled.png" alt="AeroRiver">
</p>

## Repositórios Principais

A AeroRiver Organization visa criar um ambiente de versionamento e desenvolvimento dos códigos relacionados ao projeto AeroRiver. Temos dois repositórios principais:

1. **[ArduPilot](https://github.com/AeroRiver/ArduPilot):**
   - Repositório público que contém o trabalho realizado até agora.
   - Um fork do repositório ardupilot do [Matheus Miquelini](htts://github.com/OMiquelini/ardupilot), que, por sua vez, é um fork do código original e estável do [ArduPilot](https://github.com/ArduPilot/ardupilot).
   - Atualizado e sincronizado com base nas alterações do repositório pessoal do Matheus.
   - Contém a branch master da versão original e estável do ArduPilot para restauração e estudo do código base.

2. **[AeroRiver-ArduPilot](https://github.com/AeroRiver/AeroRiver-ArduPilot):**
   - Repositório privado para salvar e versionar alterações e códigos de voo específicos da AeroRiver.
   - Guarda versões e releases privadas.
   - Possui 2 branches principais e padrão e um fluxo de trabalho próprio.

## Branches no Repositório AeroRiver-ArduPilot

- **ground_effect:**
  - Branch principal, contém a versão estável e funcional mais atual do código de voo da AeroRiver.
  - Usada para salvar as releases de desenvolvimento.
  - Protegida para evitar pushs e merges que comprometam a integridade do código.

- **develop:**
  - Branch secundária dedicada a desenvolvimento e testes.
  - Contém a versão mais atual do código a ser submetida a testes de voo.
  - Protegida e requer revisão de outro desenvolvedor para aprovar pushs e merges.

- **gndefmode_develop, land_develop e ademais branches:**
  - Além das branches principais, outras serão criadas seguindo o fluxo de trabalho. Até o momento, há duas branches referentes aos projetos em desenvolvimento, sendo eles o projeto de criação do modo de voo de efeito solo (mantido 
  anteriormente em [gndef_mode](https://github.com/OMiquelini/ardupilot/tree/gndef_mode), e o projeto do código de pouso (mantido anteriormente em [test_land](https://github.com/OMiquelini/ardupilot/tree/test_land).

## Fluxo de Trabalho

O fluxo de trabalho na organização é baseado em branches e merges.

1. **ground_effect só deve receber merges da develop após validação:**
   - O merge deve ser realizado após os códigos elaborados terem sido testados e validados com êxito em bancada e em voo.
   - PR requer aprovação de todos os desenvolvedores.

2. **Atualização da develop:**
   - Todo o trabalho desenvolvido deve ser realizado na develop.
   - Atualizada ao final do desenvolvimento de uma nova feature, testava e validada em ambiente virtual e que passará por testes de voo.
   - O pré requisito para atualização da develop é que os códigos tenham sido testados e validados em simulação SITL e sem erros de tempo de compilação.

3. **Pipeline exemplo**
<p align="center">
  <img src="https://github.com/AeroRiver/AeroRiverDocs/blob/main/docs/pipeline.jpg" alt="Pipeline">
</p>

## Outras Considerações:
   - Padronização: Novas branches devem ser nomeadas como `<nome>_develop`.
   - Após o término do desenvolvimento e do merge, a branch pode ser deletada.
   - O principal repositório de trabalho é o AeroRiver-ArduPilot.
   - Configurações dos repositórios e da organização ainda estão em progresso. Trabalho em constante aprimoramento.
